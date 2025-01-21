
Data vs. Information

* Data can be any individual fact like character, text, word, number, picture, sound, or video. 
Data doesn’t carry any significanceor purpose on its own.
* Information is useful and can be understood by the human. Information enables decision making 

Limitations of a file-based system
• Data Inconsistency
• Data Duplication
• Data integrity problems
• Incompatible file format
• Security Issues – Only password security

What is a database?
• A database is a collection of logically related data.

What is a DBMS (Database Management System)
• Set of programs to access the data.
• A software package designed to create and maintain databases.
Eg: MS Access, MySQL, Microsoft SQL Server, Oracle, etc.

Advantages of database systems
• Minimize data redundancy
• Data independence
• Efficient access to data
• Data integrity is high
• High security
• Improve data quality and accuracy
• Easy data administration
• Provide concurrent access
• Easy data sharing

Data Models in DBMS
• Defines the logical design and structure of a database and defines how data will be stored, accessed and updated in a DBMS.
• There are several data models:
        - Hierarchical Model
        - Network Model
        - Entity-relationship Model
        - Relational Model (Most widely used database model)
        - Object Oriented Model

Database Architecture
3 Level ANSI-SPARC Architecture
3 Schema (3 Tier) Architecture
• It contains 3 levels/views/schemas
        - External Schema (View Level )
        - Conceptual Schema (Logical Level)
        - Physical Schema (Internal Level)
• These 3 levels are defined as levels of data abstraction.
• Information about the schemas is stored in the system catalog

People who deal with databases
End users - Uses applications written by database application programmers
Application Programmers - Develop packages that facilitates data access for end users.
Database Administrators - Undertake the task of designing and maintaining the database.

--------------------------------------------------------------------------------------------------------------------------------------

3 Phases of the Database Design

Conceptual database design
• Construct a model of the data used in a firm, independent of all physical considerations.

Logical database design
• Construct a model of the data used in a firm based on specific data organisation. (eg: relational schema)
• It is independent of DBMS & other physical considerations.

Physical database design
• Produce description of the DB implementation for DBMS
• Create base relations, file organizations and indexes
• Create any integrity constraints and security measures

Database (DB)
• Shared collection of logically related data (& description)
• Designed to meet information needs of an organization
• Database Management Systems (DBMS)
• Software enables users to define, create maintain the DB
• Provides controlled access to this DB
• Database Application
• Computer program that interacts with DB by issuing a request (SQL statement) to the DBMS.
e.g. online retailing system, booking system, stock management system, electronic medical record,
etc.  DATABASE SYSTEM = DB + DBMS + DB APPLICATIONS


6 main steps of DB Designing

1. Requirements Analysis
    - What does the user want?
2. Conceptual Database Design (Entity Relationship Diagram)
    - Defining the entities, attributes, and the relationships
3. Logical Database Design (Map ER to Relational Schema)
4. Schema Refinement (fine tune )
5. Physical Database Design
    - Implementation of the design using a Database Management System
6. Security Design
    - Implement Controls to ensure security and integrity

Conceptual Design
• The information gathered in the requirements analysis phase is used to create a high-level description of the data in a conceptual data model or semantic data model.
Eg. Entity Relationship Model
--------------------------------------------------------------------------------------------------------------------------
What is specialization ?
• Process of maximizing differences between members of an entity byidentifying their distinguishing
characteristics.
• Specialization is a top-down approach in which a higher-level entity is divided
into multiple specialized lower-level entities

What is Generalization ? 
• Process of minimizing differences between entities by identifying their common characteristics.
• Generalization is a bottom up approach in which multiple lower level entities are combined to form a single higher level entity.
• Generalization is usually used to findcommon attributes among entities to form a generalized entity.

Participation Constraints
• Determines whether every member in the superclass must participate as a member of a subclass.
• Total Specialization (Mandatory)
    – every entity in a super class must be a member of some subclass in some specialization.
• Partial Specialization (Optional)
    – allows an entity of a superclass need not belong to any of its subclasses


Disjoint Constraint
• Describes the relationship between members of the subclasses and indicates whether it is possible for a member of a superclass to be a
member of one, or more than one, subclass.
• There are two types of constraints:
    ‒ Disjoint (OR): In one sub classes
    ‒ Overlap (AND): In many sub classes

Four types of specialisation and generalisation
• Mandatory, OR
• Mandatory, AND
• Optional, OR
• Optional, AND

--------------------------------------------------------------------------------------------------------------------------------
Generalisations with {Mandatory, AND}
• Merge all entities into one table with all attributes under new table.
• Create PK of the new table as the PK of the generalised entity.
• Add flags to differentiate between records of previous specialised entities.

Generalisations with {Mandatory, OR}
• Create separate tables for each sub entity
• One table for each of the specialised entities with the attributes of the general entity also added.
• PK for the tables is the PK of original general entity.
• Each table have their own relationships with the rest of the logical schema
• The relationships that were associated to the original general entity are doubled up.
• The relationships that were associated to each specialised entities remain the same.

Generalisations with {Optional, AND}
• Create 2 tables
• One table for general entity which becomes the Parent table.
• One table for all the specialised entities merged together which becomes the Child table.
• Create ONE one-to-one relationship optional on one side between the 2 tables
• FK of the Child table references PK of the Parent table.
• PK of the Child table is the same as the PK of Parent table.
• Add flags to differentiate between records of previous specialised entities.

Generalisations with {Optional, OR}
• Create many tables
• One table for general entity which becomes the Parent table.
• One table for each of the specialised entities, which becomes the Child table respectively.
• Create TWO one-to-one relationships optional on one side between the Parent table and the respective Child tables.
• FK of each Child table references PK of the Parent table.
• PK of each Child table is the same as the PK of Parent table.

Types of Integrity Rules
• Domain Integrity
• Key Integrity
• Entity Integrity
• Referential Integrity

Enforce Referential Integrity
• It is possible for an attribute NOT to have a corresponding value, but it will be impossible to have an invalid entry.
• The enforcement of the referential integrity rule makes it impossible to update or delete a row in a table whose primary key has mandatory matching foreign key values in the another table.
• DELETE CASCADE - Automatically deletes the matching records in the child table when the corresponding parent record is deleted.
• UPDATE CASCADE - Automatically updates the matching records in the child table when the corresponding parent record is updated.



--------------------------------------------------------------------------------------------------------------
