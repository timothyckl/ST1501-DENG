## Topic 2: Relational Data Model

1) [Database Concepts](#database-concepts)
2) [Terminologies](#terminologies)
3) [Relation Properties](#relation-properties)
4) [Entity Integrity Rules](#entity-integrity-rules)
5) [Referential Integrity Rules](#referential-integrity-rules)
6) [Entity Relationship Diagram(ERD)](#entity-relationship-diagram)
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

---

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

---

### Entity Relationship Diagram

**Conceptual Data Model**

A conceptual schema is a high-level description of informational needs (i.e. the associated retrieval and update transactions.) underlying the design of a database. 

A conceptual model is independent of any type of DBMS software.

![](https://i.imgur.com/709BeGG.png)

ERD example:

![](https://i.imgur.com/c1RIhVZ.png)

**Entity Type** - Defined as a collection of entities that has common properties and and are of interest to an organization

![](https://i.imgur.com/NqwUHHM.png)

Each entity is identified by a name and a list of attributes.

**Attribute Definitions**

- Simple Attribute
    - An attribute composed of a single component. 
- Composite Attribute
    - An attribute composed of multiple components. 
- Derived Attribute
    - An attribute that derives from a set of attributes.

**Relationships (Single & Multiple)**

**Single**

- Relationship is the association between 2 entities.
- Each relationship has a verb-based name.

**Multiple**

- Multiple relationships can be created when the two entities are associated through two distinct relationships.
    - A cart must contain one or many products.
    - A cart may be queuing for one or more products that are out-of stock.

---

### Structural Constraints

Cardinality Ratios and Participation Constraints taken together are called Structural Constraints. The name constraints refer to the fact that such limitations must be imposed on the data, for the DBMS system to be consistent with the requirements.

**Cardinality Ratio Constraints**

> The entities are denoted by rectangle and relationships by diamond.

![](https://i.imgur.com/haJ1rrl.png)

There are numbers (represented by M and N) written above the lines which connect relationships and entities. 
These are called cardinality ratios and represent the <u>maximum number of entities</u> that can be associated with each other through relationship, R.

**Types of Cardinality:**

1) One-to-one (1:1)
    - When one entity in each entity set takes part at most once in the relationship, its cardinality is one-to-one.
2) One-to-many (1:N)
    - If entities in the first entity set take part in the relationship set at most once and entities in the second entity set take part many times (at least twice), the cardinality is said to be one-to-many.
3) Many-to-one (N:1) 
    - If entities in the first entity set take part in the relationship set many times (at least twice), while entities in the second entity set take part at most once, the cardinality is said to be many-to-one.
4) Many-to-Many (N:N)
    - The cardinality is said to be many to many if entities in both the entity sets take part many times (at least twice) in the relationship set.

**Participation Constraints**

Participation Constraints tell us that that the participation in a relationship can either be total or partial.

![](https://i.imgur.com/uFM3hJS.png)

When each entity in an entity set participates in a relation, it is called Total Participation. However, when all entities in the given entity set do not participate in a relation, it is called Partial Participation.

Extras:

![](https://i.imgur.com/Nvn1PFz.png)

---

### Normalization

Normalization is the process of organizing data in a database. This includes creating tables and establishing relationships between those tables according to rules designed both to protect the data and to make the database more flexible by eliminating redundancy and inconsistent dependency.

Playlist of video explainations: [Database Concepts - Normalization Process](https://youtube.com/playlist?list=PLGQi2wV1jb3-FDXkgPg-MIC_YWzvTlDzt)

Normalization Summary:

![](https://i.imgur.com/V6TfH2U.png)

![](https://i.imgur.com/qwOgfGo.png)

- Normalisation process splits the information across several relations
- Aims to establish relations that are more efficient when we perform insert, update and delete records operations on the relation
- A process of grouping attributes into <u>**well-structured relations**</u> that allow users to <u>**insert, delete and modify**</u> rows in these relations <u>**without errors or inconsistencies**</u> resulting from these operations.

Anomalies Summary:

![](https://i.imgur.com/xk5O9kQ.png)

**Functional Dependency**

- A functional dependency is a constraint that specifies the relationship between two sets of attributes where one set can accurately determine the value of other sets. 

- It is denoted as *X → Y*, where *X* is a set of attributes that is capable of determining the value of *Y*. 

- The attribute set on the left side of the arrow, *X* is called Determinant, while on the right side, *Y* is called the Dependent. 

- Occurs when the value of an attribute is fully dependent upon another attribute' value.

- A relation is said to be in 2NF if all non-key attributes are fully dependent on whole of its primary key.

**Transitive Functional Dependency**

- Dependent is indirectly dependent on determinant.
>i.e. If a → b & b → c, then according to axiom of transitivity, a → c. 

- This functional dependency is between two (or more) non-key attributes in a relation.
- A relation is said to be in 3NF if there is <u>**no functional dependencies among non-key attributes**</u>.
