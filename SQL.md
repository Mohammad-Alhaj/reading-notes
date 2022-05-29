## SQL statment Fundemantals
 ##SELECT statment 
 
 `SELECT * FROM nmae tabel`

 *=> to select all column 
 of could mention the column name 

 ##Queries with constraints .
  
 
  `SELECT name column FROM name table
    WHERE condition AND/OR could put another condition  

  `
  I cna use the operator like 

| Operator      | 
| ----------- | 
| =, !=, < <=, >, >=| 
| BETWEEN … AND …   |   
| NOT BETWEEN … AND |      
| IN (…)            |      
|                   | 
| NOT IN (…)        |        
|  LIKE             | 
|  NOT LIKE         |
|  %                |
|  _                |

## ORDER BY

`SELECT name column …
FROM name tabel
WHERE condition(s)
ORDER BY column ASC/DESC;`
**ASC** order column A_Z or 1- 100... ext..
**DESC** oredr column Z-A or 100... -1 ext...

##LIMIT 
use to cut or reduce the rows 
##OFFSET 
us to select where LIMET reduce or specific where begin the rows
`LIMIT 5 OFFSET 10`

## INNER JOIN
this statement to join the tabel if we have two tabel we can marge them wth this statment

`SELECT * FROM name table 1
INNER JOIN name table 2
ON tabel1.column name = tabel2.name column`

## INSERT ROWS

`INSERT INTO table name (column ,another column)

VALUES (value of column , value of another column)
 `

 ## Updating rows

 ` 
 UPDATE name tabel
 SET column name = the value , column name2=the value
 
 `
 could use WHRER to specific conditions

 ## DELETE ROWS
 `
 DELETE FROM name tabel
 WHERE condition s
 `
 use to delete some of rows and could add the coditions to delete specific rows

 ## CREATE TABLE


`CREATE TABLE name table (

Id integer 
name TEXT 
Phone number varchar(here could choose the specific number of char)


);`


there are mant of the data type you can see the sheet 
**Table constraints**
the each column it can be addetional table constraints 


## Altering tables

`
ALTER name table
ADDCOLUMN name column otional to add datat type and you can add defult value


ALTER name table 
RENAME to new name table 



ALTER name table 
DROP column name column 

`

## Dropping tables


`
DROP TABLE name table 

DROP TABLE IF EXISTS name tabel  


`
WE use the `IF EXISTS` to avoid the error


[exercises 1-6](./exercise%201-6)

[exercises 13-18](./exercise%20%2013-18)