## Topic 2: Relational Data Model

1) [Database Concepts](#database-concepts)
2) [Terminologies](#terminologies)
3) [Relation Properties](#relation-properties)
4) [Entity Integrity Rules](#entity-integrity-rules)
5) [Referential Integrity Rules](#referential-integrity-rules)
6) [Entity Relationship Diagram(ERD)](#entity-relationship-diagram)
    - ERD to Database
7) [Normalization](#normalization)

### Database Concepts

- **Database** - A collection of **inter-related data**.
- **Inter-related data** - This implies that **data are linked** by some mechanism.
- **Database Management System** (DBMS) - A collection of programs to **manage** *(update, insert, delete, select)*, **protect and control access to databases**.

### Terminologies

- **Relation** 

    - A relation is a 2D table 
    - A cell is the intersection between a row and column.

- **Record/Tuple**

    - Each row in a table in a record which represent an individual objection in a relation.
    - A record of a table is called a tuple.

- **Attributes** 

    - Attributes are column names in a table that define characteristics of an object.

- **Attribute Values** 

    - Attribute values describe the members of the entity.
    - Concept of NULL attribute value

        - NULL is a special value allowed in relational databases.
        - NULL implies that a value is either unkown/not applicable.

- **Attribute Domain** 

    - Attribute domain is a set of values allowed in an attribute (e.g. Mr, Ms).
    - Possible values could be physical/semantic in nature.

- **Attribute/SQL Data Type** 

![](https://i.imgur.com/bY8Ukkf.png)
>**Note**:Not all data types are supported by every relational database management systems. 

- **Relational Database** 
    - A relational database is a collection of data items that stores and provides access to data points that are related to one another.


### Relation Properties

A table **MUST** satisfy the <u>**SIX properties of a relation.**</u>

1) Name of relation must be unique within a database
2) Every cell must be single-valued
3) Attribute names within a relation must be unique
4) Values of an attribute are from the same domain
5) Order of tuples or attributes in a relation does not matter
6) Each tuple (record/row) in a relation must be unique 

### Entity Integrity Rules

1) Make sure that each tuple in a table is unique.
2) Every table mush has a primary key, for example, Student_ID for a Student table.
3) Every entity is unique.
4) The relations Primary Key must have unique values for each row.
5) Primary Key cannot have NULL value and must be unique.
6) Example can be an Employee_ID cannot be null in an Employee table.

### Referential Integrity Rules

**Key Definitions**
- Candidate Key 
    - A set of attributes that uniquely identify tuples in a table. 
- Primary Keys 
    - A column/group of attributes in a table that uniquely identify every row in that table.
- Foreign Keys 
    - Uniquely <u>**IDENTIFIES**</u> a tuple in a relation
    - A column that creates a relationship between two tables. 
    - The purpose of Foreign keys is to maintain data integrity and allow navigation between two different instances of an entity.
- Composite Keys
    - A combination of two or more columns that uniquely identify rows in a table. 
    - The combination of columns guarantees uniqueness, though individual uniqueness is not guaranteed.

Referential Integrity Rule in DBMS is based on Primary and Foreign Key. The rule defines that **a foreign key have a matching primary key**. 

![](https://i.imgur.com/EAKfPdG.png)

### Entity Relationship Diagram

### Normalization

