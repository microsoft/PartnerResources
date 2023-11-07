---
layout: page
title: Lineage Extraction with Azure SQL Database in Microsoft Purview
description: Extracting lineage -- the ability to weave together the lifecycle of data as it moves through the enterprise -- is challenging due to the complexities of many different systems. Microsoft Purview is able to extract lineage from an Azure SQL Database by examining the execution of stored procedures. This video looks at how it works, and how to set it up. Additional code snippets are here for the demos used in this session.
updated: 2022-08-23
permalink: /skilling/data-governance-academy/purview-lineage-azure-sql-db
youtubeid: BIVh_8QhMKY
tags: 
- azure
- data, analytics, and ai
- academy content
- modern analytics academy
- microsoft purview 
- sql
- lineage
- data governance
- vignettes
---

# {{ page.title }}

{{ page.description }}

{% include youtubethumb.md showlink="true" %}

## Links 

Hands-on Lab:
* [Purview Lab - (particularly module 15)](https://aka.ms/purviewlab)

Additional tools used in presentation:
* [Azure Data Studio](https://docs.microsoft.com/en-us/sql/azure-data-studio/?view=sql-server-ver16)

## Code Snippets

In addition to code in [Module 15 of the Purview Lab](https://aka.ms/purviewlab), there are a few additional examples created in this presentation. The code below expounds on the Purview Lab module by creating several additional destinatino tables, and additional stored procedures.

All table definitions:

```sql
CREATE TABLE [dbo].[SourceTest](
ID int PRIMARY KEY,
FirstName nvarchar(50),
LastName nvarchar(50)
);
GO

INSERT INTO dbo.SourceTest
(ID, FirstName, LastName)
VALUES (1, 'Bob', 'Smith');
GO

INSERT INTO dbo.SourceTest
(ID, FirstName, LastName)
VALUES (2, 'Mike', 'Jones');
GO

INSERT INTO dbo.SourceTest
(ID, FirstName, LastName)
VALUES (3, 'Becky', 'McDonald');
GO

INSERT INTO dbo.SourceTest
(ID, FirstName, LastName)
VALUES (4, 'Steve', 'Craft');
GO

CREATE TABLE [dbo].[DestinationTest](
ID INT NOT NULL IDENTITY PRIMARY KEY,
SourceId INT,
FirstName NVARCHAR(50),
LastName NVARCHAR(50),
CreateDate DATETIME
);
GO
ALTER TABLE [dbo].[DestinationTest] ADD CONSTRAINT DF_DestinationTest DEFAULT GETDATE() FOR CreateDate
GO

CREATE TABLE [dbo].[DestinationTestOdd](
ID INT NOT NULL IDENTITY PRIMARY KEY,
SourceId INT,
FirstName NVARCHAR(50),
LastName NVARCHAR(50),
CreateDate DATETIME
);
GO
ALTER TABLE [dbo].[DestinationTestOdd] ADD CONSTRAINT DF_DestinationTestOdd DEFAULT GETDATE() FOR CreateDate
GO

CREATE TABLE [dbo].[DestinationTestEven](
ID INT NOT NULL IDENTITY PRIMARY KEY,
SourceId INT,
FirstName NVARCHAR(50),
LastName NVARCHAR(50),
CreateDate DATETIME
);
GO
ALTER TABLE [dbo].[DestinationTestEven] ADD CONSTRAINT DF_DestinationTestEven DEFAULT GETDATE() FOR CreateDate
GO

CREATE TABLE [dbo].[DestinationTestCombo](
ID INT NOT NULL IDENTITY PRIMARY KEY,
SourceId INT,
WholeName NVARCHAR(100),
CreateDate DATETIME
);
GO
ALTER TABLE [dbo].[DestinationTestCombo] ADD CONSTRAINT DF_DestinationTestCombo DEFAULT GETDATE() FOR CreateDate
GO
```

Stored Procedures to create data movement to destination tables:

```sql

CREATE PROCEDURE dbo.MoveDataTest 
@UserId int
AS
INSERT INTO dbo.DestinationTest
(SourceId, FirstName, LastName)
SELECT ID, FirstName, LastName
FROM dbo.SourceTest
WHERE dbo.SourceTest.ID = @UserId
GO

CREATE PROCEDURE dbo.MoveDataTestBranch
@UserId int
AS
IF @UserId % 2 = 0
BEGIN
    INSERT INTO dbo.DestinationTestEven
    (SourceId, FirstName, LastName)
    SELECT ID, FirstName, LastName
    FROM dbo.SourceTest
    WHERE dbo.SourceTest.ID = @UserId
END
ELSE
BEGIN
    INSERT INTO dbo.DestinationTestOdd
    (SourceId, FirstName, LastName)
    SELECT ID, FirstName, LastName
    FROM dbo.SourceTest
    WHERE dbo.SourceTest.ID = @UserId
END
GO

CREATE PROCEDURE dbo.MoveDataTestCombo
@UserId int
AS
INSERT INTO dbo.DestinationTestCombo
(SourceId, WholeName)
SELECT ID, FirstName + ' ' + LastName
FROM dbo.SourceTest
WHERE dbo.SourceTest.ID = @UserId
GO
```

To execute all three stored procedures, use the following code. Note: for Azure SQL Database Lineage Extraction to detect lineage, the execution of the stored procedures must occur after the lineage scan is configured.

```sql
--insert into dbo.DestinationTest
exec MoveDataTest 1
exec MoveDataTest 2
exec MoveDataTest 3
exec MoveDataTest 4

--insert into dbo.DestinationTestOdd / Even
exec MoveDataTestBranch 1
exec MoveDataTestBranch 2
exec MoveDataTestBranch 3
exec MoveDataTestBranch 4

--insert into dbo.DestinationTestCombo
exec MoveDataTestCombo 1
exec MoveDataTestCombo 2
```