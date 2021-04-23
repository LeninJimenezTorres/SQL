# ALL ABOUT SQL

[editor on GitHub](https://github.com/LeninJimenezTorres/SQL/edit/gh-pages/index.md)

In this webbside you can find a brief but concise abstract about the context of SQL language.

## 1. IDENTIFIERS

### A) BEGIN WITH:

The name or identifier should begin with:

- A letter
- Underscore ( _ )
- At sign ( @ ), used for variables on TransactSQL.
- Number sign or Hash ( # ), used for objects tempdb.
 
 The two last are considered like special characters to other target, because this it is prefered not used them, but thay are allowed.

### B) SUBSEQUENT CHARACTERS:

They are allowed:

- Letters
- Numbers
- @, _, #, $

### C) NOT ALLOWED

- Not with "DATABASE"
- Not with "TABLE"
- Not with "SCHEMA"
- Not with "COLUMN"
- Not spaces
- Not another special characters

### D) MAXIMUM LENGTH

The identifiers should have less of 128 characters.

### E) ADVICES

Use:

- CamelCase, for instance: LordMortem
- Underscore separate, for instance: my_table
- Hybrid with the both two last, for instance: My_Table

Avoid:

- Avoid use delimited identifiers, for instance: [My table]



## 2. DATA TYPES

### A) CHARACTERS

#### a.1) Char 
```markdown
Command: `char(n)`
```
Details: 
           - [1-8000] bytes
           - Fixed length
           - Non Unicode

#### a.2) Varchar 
```markdown
Command: `varchar(n)`
```
Details: 
           - [1-8000] bytes
           - Variable length
           - Non Unicode

#### a.3) Nchar 
```markdown
Command: `nchar(n)`
```
Details: 
           - [1-4000] bytes
           - Fixed length
           - Unicode

#### a.4) Nvarchar 
```markdown
Command: `nvarchar(n)`
```
Details: 
           - [1-4000] bytes
           - Variable length
           - Unicode



### B) INTEGERS

#### b.1) Tiny integer 
```markdown
Command: `TINYINT`
```
Details: 
           - 1 bytes
           - 0-255

#### b.2) Small integer
```markdown
Command: `SMALLINT`
```
Details: 
           - 2 bytes
           - [-2^15 to 2^15 -1]
           - [-32k to 32k]

#### b.3) Integer 
```markdown
Command: `INT`
```
Details: 
           - 4 bytes
           - [-2^31 to 2^31 -1]
           - [+- 2,1 billons]
          
#### b.4) Big integer
```markdown
Command: `BIGINT`
```
Details: 
           - 8 bytes
           - [-2^63 to 2^63 -1]
           - [+- 9,2 billon]
           - max 19 digits integers or decimals



### C) DECIMAL

#### c.1) Decimal/Numeric 
```markdown
Command: `DECIMAL[(p),(s)] 
          NUMERIC[(p),(s)]`
          
          p: precision, is all numbers both integer and decimal parts 
          s: scalae, is only the decimal part
```
Details: 
           - [5-17] bytes

#### c.2) Money
```markdown
Command: `MONEY`
```
Details: 
           - 8 bytes
           - 8 decimals

#### c.3) Small money 
```markdown
Command: `SMALLMONEY`
```
Details: 
           - 4 bytes
           - 4 decimals


### D) TIME

#### d.1) Data 
```markdown
Command: `DATA`
```
Details: 
           - 3 bytes
           - [0001-01-01 to 9999-12-31]


#### d.2) Time
```markdown
Command: `TIME[(n)]`

        n: fractional seconds - 7 default
```
Details: 
           - 5 bytes


#### d.3) Data time 
```markdown
Command: `DATATIME`
```
Details: 
           - 8 bytes
           - [January 1, 1753 to Dec 31, 9999]
 
 
#### d.4) Small data 
```markdown
Command: `SMALLDATA`
```
Details: 
           - 4 bytes
           - [Jan 1, 1990 to Jan 6, 2079]
           - Non fractional seconds
           
           
#### d.5) Data time 2 
```markdown
Command: `DATATIME2(n)`
```
Details: 
           - [2 - 6] bytes
           - [0001-01-01 to 9999-12-31]
           

## 3. CREATE DATABASE
```markdown
              `CREATE DATABASE __________;`
```


## 4. SET DATABASE
```markdown
              `USE __________;`
```


## 5. CREATE TABLE

Here you have to define the columns of the table and the 

```markdown
              ` CREATE TABLE _______
              (idIdentifier1 INTEGER PRIMARY KEY, 
              Column2 CHAR(40),
              Column3 FLOAT                      
              ); `
```

## 6. MODIFY PRIMARY KEY

First off, you have to delete the constaint:
```markdown
             ALTER TABLE ________ DROP CONSTRAINT _______(Primary Kay into Keys Folder)_______ 
```
After this, you can modify the primary kay with the next comand


## 7. MODIFY ATTRIBUTES OF A COLUMN

Here you can use any attribute option with the next command:
```markdown
             ALTER TABLE ________
             ALTER COLUMN ________ ________ (attribute options)
             
             For instance:
                            ALTER TABLE Doctors
                            ALTER COLUMN Id_Doctores INTEGER NOT NULL
```

## 8. ADD A COLUMN

```markdown
             ALTER TABLE ________ ADD _______  _________ (attribute options)
             
             For instance:
                            ALTER TABLE Doctor ADD Id_Doctores PRIMARY KEY NOT NULL
```


# Autor:
Lenin Jiménez Torres

### Support or Contact
[LinkedIn](https://www.linkedin.com/in/lenin-jim%C3%A9nez-ba9251134/)
