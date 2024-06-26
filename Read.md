**Database Normal forms First Normal Form (1NF):** This is the most basic level of normalization. In 1NF, each table cell should contain only a single value, and each column should have a unique name. The first normal form helps to eliminate duplicate data and simplify queries.
**Second Normal Form (2NF)**: 2NF eliminates redundant data by requiring that each non-key attribute be dependent on the primary key. This means that each column should be directly related to the primary key, and not to other columns. 
**Third Normal Form (3NF)**: 3NF builds on 2NF by requiring that all non-key attributes are independent of each other. This means that each column should be directly related to the primary key, and not to any other columns in the same table.
**Boyce-Codd Normal Form (BCNF)**:BCNF is a stricter form of 3NF that ensures that each determinant in a table is a candidate key. In other words, BCNF ensures that each non-key attribute is dependent only on the candidate key. 
**Fourth Normal Form (4NF)**: 4NF is a further refinement of BCNF that ensures that a table does not contain any multi-valued dependencies. 
**Fifth Normal Form (5NF)**: 5NF is the highest level of normalization and involves decomposing a table into smaller tables to remove data redundancy and improve data integrity.

**Difference Between Snowflake Schema and Star Schema**
**Star Schema**  The fact tables and dimension tables are both contained in the star schema. The star schema is a top-down model. The star schema takes up more space. Queries are executed in less time. Normalization is not employed in the star schema. It has a very simple design. Star schema has a low query complexity. It contains fewer foreign keys. It has a high level of data redundancy.
**Snowflake Schema**   The fact tables, dimension tables, and sub dimension tables are all contained in the snowflake schema. While it is a bottom-up model. While it takes up less space. Here query execution takes longer than with the star schema. Both normalisation and denormalization are employed in this. While its design is complex. Snowflake schema has a higher query complexity than star schema. It has a larger number of foreign keys. While it has a minimal level of data redundancy.

**OLAP and OLTP**
**OLTP**  An OLTP (Online Transactional Processing) database contains detailed and up-to-date data, as well as a large volume of typically small data transactions. Can handle large numbers of small online transactions Simple queries, such as Insert, Delete, and Update information. The OLTP iteself and respective transactions correspond to the sources of data. 
**OLAP**  online analytical processing often necessitates complex and aggregated queries with a small number of transactions. Handles large volumes of data. Complex queries which require aggregations. The various OLTP databases become the data sources for OLAP.

**Dimension Table**:

A dimension table contains descriptive attributes used for analyzing the data stored in a data warehouse. It typically consists of textual or categorical data that provides context to the numerical data stored in fact tables. Dimension tables are often relatively small compared to fact tables. Examples of dimension tables include customer, product, time, geography, etc. Each dimension table usually has a primary key that uniquely identifies each record in the table.

**Fact Table**:

A fact table contains quantitative data, also known as metrics or measures, that represent the business process being analyzed. Fact tables typically contain numerical data such as sales revenue, quantity sold, profit, etc. Fact tables are usually large compared to dimension tables. Fact tables have foreign keys that reference the primary keys of associated dimension tables, establishing relationships between dimensions and measures.

**Types of Dimensions**:
Conformed Dimension 
Degenerate Dimension 
Junk Dimension 
Role-Playing Dimension 
Slowly Changing Dimension 
There are different types of SCDs: Type 1 (overwrite), Type 2 (add new row), and Type 3 (add new attribute). Type 1 SCDs overwrite existing data with new values, Type 2 SCDs add new rows for each change, preserving historical data, and Type 3 SCDs add new attributes to existing rows, keeping track of both old and new values
