Download Link: https://assignmentchef.com/product/solved-dbst651-project-design-and-implement-a-relational-database
<br>
Relational databases are the foundations of the majority of information systems and represent one of the most pervasive technologies today. This project covers fundamental concepts necessary for the design, use, and implementation of relational database systems. Through the hands-on activities you will have a better understanding of database modeling and design, the languages and facilities provided by database management systems, and techniques for implementing relational database systems.

In this project, you are the lead of the company’s Database Design Team. A new database system is needed to support critical business functions. Your task is to plan, design and implement a relational database system for a domain specific application of your choice that meets the given requirements.

Your project will be completed in four stages: initialization, preparation and planning; system analysis and requirement definition; database design; and database implementation. We will divide those stages into individual activities and in this learning demonstration you will conduct those activities sequentially: first you will need to create a formal business document called Statement of Work (SOW) to define your objectives, tasks, deliverables, and constraints. Once the management approves your SOW, you can start to analyze your business domain and define the requirements. After all requirements have been articulated clearly, you can start to design your database by modeling. The most common relationship database model is Entity Relationship Diagram (ERD). Next you will follow your ERD and implement your database by creating database objects such as tables, indexes, views, and triggers using Data Definition Language (DDL). Once the database structure is ready, you can populate your tables with business data using Data Manipulation Language (DML). And finally, you will solve business problems and provide critical insight by querying your data using Structured Query Language (SQL) statements.




<strong>Learning Demonstration</strong>

Throughout this learning demonstration, a very simple Human Resource (HR) database is being used as an example. The database keeps track of information about employees and departments.




<ol>

 <li>Before you can start your project, you need to define what exactly you want to do by creating a Statement of Work. It is a formal document and must be agreed upon by all parties and stakeholders.</li>

 <li>First, point to your browser to the ProjectMinds website <a href="http://www.projectminds.com/Article11.html">http://www.projectminds.com/Article11.html</a> and read a concise introduction on how to write a SOW.</li>

 <li>Once you understand the basic components of a SOW, write a 1-2 pages document to describe the need to create, design and implement the database that you propose. I also provided a sample SOW that is specifically written for a database project. Please check Course Content for the sample and notice that it is a barebone example and only provides a highlight of the basic components of a SOW. Please use it as reference only and add more contents to your SOW. The following should be addressed in your SOW:</li>

 <li>What is the business need and business problem?</li>

 <li>What is the purpose of the project?</li>

</ol>

<ul>

 <li>What is the scope of the work?</li>

</ul>

<ol>

 <li>What will be achieved by implementing this database?</li>

 <li>What benefits does the new database offer?</li>

</ol>




<ol>

 <li>The SOW should have one paragraph of overview for executive summary, a section captures the purpose and objectives of the database, and a detailed description on related technologies to be used in the project such as diagram and design tools, DBMS system, hardware, software, DDL and DML (How you will use these in your project).</li>

</ol>




<ol start="2">

 <li>Once the SOW gets the approval from management, it will serve as the general guideline for your remaining project. Now you can start to analyze the business problem you want to solve, and put the results into a requirement definition document. The document describes business rules by identifying what business data you want to keep track of and how those data are related to each other.</li>

 <li>First visit <a href="http://www.tdan.com/view-articles/5174/">http://www.tdan.com/view-articles/5174/</a> and learn what data related business rules are. Business rules are precisely written and unambiguous statements that are derived from a detailed description of an organization’s operations. It includes entities, relationships, attributes, connectivity, cardinalities, and constraints.</li>

 <li>Now create narrative/description to document business rules related to your business domain.

  <ol>

   <li>Describe each entity and its main attributes. For example:</li>

  </ol></li>

</ol>

<em>Entity Name: EMPLOYEE</em>

<em>Entity Description: employees who work in an organization</em>

<em>Main attributes of EMPLOYEE: </em>

<em>Attribute Name: L_NAME</em>

<em>Attribute Description: last name.</em>

<em>Attribute Name: F_NAME</em>

<em>Attribute Description: first name.</em>

<em>Attribute Name: DOB</em>

<em>Attribute Description: date of birth.</em>

<ol>

 <li>Describe each relationships and the cardinality from both directions of the relationship. For example:</li>

</ol>

<em>Relationship: works between EMPLOYEE and DEPARTMENT</em>

<em>Cardinality/Business rule: a department can have zero to many employees; an employee works for one and only one department</em>

<ul>

 <li>Describe any other assumptions and special considerations you may have.</li>

</ul>




<ol start="3">

 <li>Now that you have clarified your business requirements and business rules, you now start to design your database by creating the Entity Relationship Diagram (ERD).</li>

 <li>First review some basic entity relationship modeling concepts and techniques by visiting <a href="https://www.youtube.com/watch?feature=player_embedded&amp;v=mQ4D0drMrYI">https://www.youtube.com/watch?feature=player_embedded&amp;v=mQ4D0drMrYI</a> , <a href="https://www.youtube.com/watch?v=-fQ-bRllhXc%20">https://www.youtube.com/watch?v=-fQ-bRllhXc</a> , and <a href="http://www.databaseanswers.org/tutorial4_data_modelling/index.htm">http://www.databaseanswers.org/tutorial4_data_modelling/index.htm</a>.</li>

 <li>Now create your initial conceptual level ERD which mainly captures and represents your business rules (business domain entities and their relationships) specified in step 2.</li>

 <li>Then refine your model and create design level ERD by <a href="http://www.troubleshooters.com/littstip/ltnorm.html">normalization</a> and resolving all many-to-many relationships.

  <ol>

   <li>The ERD should consist of a minimum of 5, but no more than 6, entities. Each entity should have a minimum of 5 attributes. Draw appropriate relationships to connect related entities.</li>

   <li>The crow’s feet notation is required.</li>

  </ol></li>

</ol>

<ul>

 <li>ER Assistant, Visio, or SQL Developer Data Modeler is the suggested diagramming tool for this course. Use of another tool is acceptable as long as the final product is submitted in a common format (such as PDF or JPG) that can be read, evaluated and graded.</li>

</ul>




<ol start="4">

 <li>Create DDL: tables, columns, keys, indexes</li>

</ol>

Once the design model is completed and the ERD is approved, the next step is to create the physical database objects (tables, columns, keys, etc.) that implement the logical objects (entities, attributes, relationships, etc.) defined in your ERD. You use SQL Data Definition Language (DDL) to create your database schema and table structure which will include the following:

<ol>

 <li>Drop statements for all objects in the lab project (drop existing objects first so that you can rerun your script multiple times without error). Please make sure this is the first part of your entire DDL script. For example:</li>

</ol>

<em>DROP TABLE EMPLOYEE CASCADE CONSTRAINTS;</em>

<em>DROP TABLE DEPARTMENT CASCADE CONSTRAINTS;</em>

<em> </em>

<em>DROP SEQUENCE seq_dept_id;</em>

<em>DROP SEQUENCE seq_emp_id;</em>

<em> </em>

<ol>

 <li>Now add DDL Create statements for all tables and associated objects.

  <ol>

   <li>Review <a href="https://www.w3schools.com/sql/sql_create_table.asp">SQL CREATE TABLE statement</a> and add your tables and columns including column name, size, type, constraint (such as NOT NULL).</li>

   <li>Review <a href="https://www.w3schools.com/sql/sql_primarykey.asp">SQL Primary key constraint</a> and <a href="https://www.w3schools.com/sql/sql_foreignkey.asp">foreign key constraint</a>. Add keys to your table definition.</li>

  </ol></li>

</ol>

<ul>

 <li>Make sure to create parent base tables first, and then child tables. For example:</li>

</ul>

<em>CREATE TABLE DEPARTMENT</em>

<em>( DEPT_ID       NUMBER(10) PRIMARY KEY,</em>

<em>  DEPT_NAME     VARCHAR2(50) NOT NULL,</em>

<em>  DEPT_LOCATION VARCHAR2(50) NOT NULL</em>

<em>);</em>

<em>CREATE TABLE EMPLOYEE</em>

<em>( EMP_ID   NUMBER(10) PRIMARY KEY,</em>

<em>  EMP_NAME VARCHAR2(50) NOT NULL,</em>

<em>  EMP_DOB  DATE,</em>

<em>  DEPT_ID  NUMBER(10),</em>

<em>  CONSTRAINT EMP_DEPT_ID_FK FOREIGN KEY (DEPT_ID) REFERENCES DEPARTMENT(DEPT_ID)</em>

<em>);</em>

<ol>

 <li>Now that your tables have been created, you can add indexes to certain columns to speed up queries.

  <ol>

   <li>Create unique index on natural key columns. For example:</li>

  </ol></li>

</ol>

<em>CREATE UNIQUE INDEX DEPT_DEPT_NAME_UX ON DEPARTMENT(DEPT_NAME);</em>

<ol>

 <li>Create index on foreign key columns. For example:</li>

</ol>

<em>CREATE INDEX EMP_DEPT_ID_FK ON EMPLOYEE(DEPT_ID);</em>

<ul>

 <li>Create index on other columns that will be frequently used as query filters (i.e., Columns in the “WHERE” clause). For example:</li>

</ul>

<em>CREATE INDEX EMP_EMP_NAME_IDX ON EMPLOYEE(EMP_NAME);</em>




<ol start="5">

 <li>Now you basic table structure has been created. The second part of the DDL is to add additional database objects (sequences, views, triggers) to facilitate your data entries and queries.

  <ol>

   <li>First modify your table structure to add some audit columns so that you can keep track of who adds/changes a record and when. Use <a href="https://www.w3schools.com/sql/sql_alter.asp">DDL ALTER TABLE statement</a>. For example:</li>

  </ol></li>

</ol>

<em>ALTER TABLE DEPARTMENT ADD</em>

<em>( CREATED_BY    VARCHAR2(30),</em>

<em>  DATE_CREATED  DATE,</em>

<em>  MODIFIED_BY   VARCHAR2(30),</em>

<em>  DATE_MODIFIED DATE</em>

<em>);</em>

<em> </em>

<em>ALTER TABLE EMPLOYEE ADD</em>

<em>( CREATED_BY    VARCHAR2(30),</em>

<em>  DATE_CREATED  DATE,</em>

<em>  MODIFIED_BY   VARCHAR2(30),</em>

<em>  DATE_MODIFIED DATE</em>

<em>);</em>

<ol>

 <li>Then read about <a href="https://www.w3schools.com/sql/sql_view.asp">SQL views</a> and create a view for each table so that only business columns are included but not audit columns. For example:</li>

</ol>

<em>— This view shows basic department information including id, name and location (without audit columns)</em>

<em>CREATE OR REPLACE VIEW VW_DEPT AS</em>

<em>    SELECT DEPT_ID, DEPT_NAME, DEPT_LOCATION FROM DEPARTMENT;</em>

<em>— This view show basic employee information including id, name, DOB and department id (without audit info)</em>

<em>CREATE OR REPLACE VIEW VW_EMP AS</em>

<em>    SELECT EMP_ID, EMP_NAME, EMP_DOB, DEPT_ID FROM EMPLOYEE;</em>

<ol>

 <li>It is a good practice to use surrogate key vs. natural key (business key) as primary key. To do so, you will need to create a <a href="https://www.w3schools.com/sql/sql_autoincrement.asp">sequence</a> for each table’s primary key column. For example:</li>

</ol>

<em>CREATE SEQUENCE seq_dept_id;</em>

<em>CREATE SEQUENCE seq_emp_id;</em>

<ol>

 <li>To automatically generate values for primary key columns, you will need a special database object called trigger. Please review table triggers by visiting <a href="http://psoug.org/reference/table_trigger.html">http://psoug.org/reference/table_trigger.html</a>. Now create a row level trigger for each table so that you can populate surrogate key and audit columns with appropriate values. For example:</li>

</ol>

<em>–This trigger populates surrogate key and audit columns with appropriate values</em>

<em>CREATE OR REPLACE TRIGGER BIUR_DEPT_TRG</em>

<em>  BEFORE INSERT OR UPDATE ON DEPARTMENT</em>

<em>  FOR EACH ROW</em>

<em>BEGIN</em>

<em>  — use surrogate key</em>

<em>  IF :NEW.dept_id IS NULL THEN</em>

<em>    :NEW.dept_id := seq_dept_id.NEXTVAL;</em>

<em>  END IF;  </em>

<em>  IF INSERTING THEN</em>

<em>    IF :NEW.created_by IS NULL THEN :NEW.created_by := USER; END IF;</em>

<em>    IF :NEW.date_created IS NULL THEN :NEW.date_created := SYSDATE; END IF;</em>

<em>  END IF;  </em>

<em>  IF INSERTING OR UPDATING THEN</em>

<em>    IF :NEW.modified_by IS NULL THEN :NEW.modified_by := USER; END IF;</em>

<em>    IF :NEW.date_modified IS NULL THEN :NEW.date_modified := SYSDATE; END IF;</em>

<em>  END IF;</em>

<em>END;</em>

<em>/</em>

<em> </em>

<em>–This trigger populates surrogate key and audit columns with appropriate values</em>

<em>CREATE OR REPLACE TRIGGER BIUR_EMP_TRG</em>

<em>  BEFORE INSERT OR UPDATE ON EMPLOYEE</em>

<em>  FOR EACH ROW</em>

<em>BEGIN</em>

<em>  — use surrogate key</em>

<em>  IF :NEW.emp_id IS NULL THEN</em>

<em>    :NEW.emp_id := seq_emp_id.NEXTVAL;</em>

<em>  END IF;  </em>

<em>  IF INSERTING THEN</em>

<em>    IF :NEW.created_by IS NULL THEN :NEW.created_by := USER; END IF;</em>

<em>    IF :NEW.date_created IS NULL THEN :NEW.date_created := SYSDATE; END IF;</em>

<em>  END IF;  </em>

<em>  IF INSERTING OR UPDATING THEN</em>

<em>    IF :NEW.modified_by IS NULL THEN :NEW.modified_by := USER; END IF;</em>

<em>    IF :NEW.date_modified IS NULL THEN :NEW.date_modified := SYSDATE; END IF;</em>

<em>  END IF;</em>

<em>END;</em>

<em>/ </em>

<ol>

 <li>Now check the DBMS data dictionary to make sure all your objects have been created successfully. For example:</li>

</ol>

<em>SELECT TABLE_NAME FROM USER_TABLES;  </em>

<em>SELECT OBJECT_NAME, STATUS, CREATED, LAST_DDL_TIME FROM USER_OBJECTS;</em>

<ol start="6">

 <li>Now you have completed the definition part of your database schema. The next step is to enter data into your tables and then query your data.

  <ol>

   <li>Once all objects have been created in the database, create <a href="https://www.w3schools.com/sql/sql_insert.asp">SQL INSERT statements</a> (DML) to populate each table with sample data. Each table should have a minimum of 10 rows unless you have specific business rules that prevent it from having that many records. Make sure your sequences and triggers are valid and enabled so that surrogate keys and audit columns can be populated automatically. For example:</li>

  </ol></li>

</ol>

<em>INSERT INTO DEPARTMENT(DEPT_NAME, DEPT_LOCATION)</em>

<em>  VALUES(‘HR’, ‘Adelphi, MD’);</em>

<em>INSERT INTO DEPARTMENT(DEPT_NAME, DEPT_LOCATION)</em>

<em>  VALUES(‘Sales’, ‘College Park, MD’);</em>

<em>COMMIT;</em>

<ol>

 <li>After entering sample data into each table, develop <a href="https://www.w3schools.com/sql/sql_select.asp">SQL SELECT statements</a> to query your tables. You should have a minimum of 20 SQL select statements. Query 1 to 12 are basic queries, plus at least 8 advanced queries. Each query should have comment/description to explain its business purpose, as well as which requirement item you are satisfying (i.e., –1. Select all columns and all rows from one table). Please submit both query statements and query results.

  <ol>

   <li>Select all columns and all rows from one table. For example:</li>

  </ol></li>

</ol>

<em>— Query 1: select all columns and all rows from one table</em>

<em>— Business purpose: this query selects all information about all departments    </em>

<em>SELECT * FROM DEPARTMENT;</em>

<ol>

 <li>Select 5 columns and all rows from one table.</li>

</ol>

<ul>

 <li>Select all columns and all rows from one view.</li>

</ul>

<ol>

 <li>Using a join on 2 tables, select all columns and all rows from the tables without the use of a Cartesian product.</li>

 <li>Select and order data retrieved from one table.</li>

 <li>Using a join on 3 tables, select 5 columns from the 3 tables. Use syntax that would limit the output to 10 rows.</li>

</ol>

<ul>

 <li>Select distinct rows using joins on 3 tables.</li>

 <li>Use group by &amp; having in a select statement using one or more tables.</li>

</ul>

<ol>

 <li>Use IN clause to select data from one or more tables.</li>

 <li>Select Length of one column from one table (use Length function)</li>

 <li>Use the <a href="https://www.w3schools.com/sql/sql_delete.asp">SQL DELETE statement</a> to delete one record from one table. Add select statements to demonstrate the table contents before and after the DELETE statement. Make sure to use ROLLBACK afterwards so that the data will not be physically removed. For example:</li>

</ol>

<em>— Query 11: use the SLQ DELETE statement to delete one record from one table</em>

<em>— Business purpose: delete the HR department</em>

<em>DELETE FROM DEPARTMENT WHERE DEPT_NAME = ‘HR’; </em>

<em>— revert the change</em>

<em>ROLLBACK;</em>

<ul>

 <li>Use the <a href="https://www.w3schools.com/sql/sql_update.asp">SQL UPDATE statement</a> to change some data. Add select statements to demonstrate the table contents before and after the UPDATE statement. You can either COMMIT or ROLLBACK afterwards. For example:</li>

</ul>

<em>— Query 12: use the SQL UPDATE statement to change some data</em>

<em>— Business purpose: change the location of HR department to Largo, MD </em>

<em>UPDATE DEPARTMENT SET DEPT_LOCATION = ‘Largo, MD’ WHERE DEPT_NAME = ‘HR’;</em>

<em>— revert the change</em>

<em>ROLLBACK;</em>

<ul>

 <li>Perform 8 additional advanced (multiple table joins, sub-queries, aggregate, etc.) SQL statements.</li>

</ul>




<strong>Helpful Hints</strong>




<ul>

 <li>Keep your project simple and limited to five entities. Keep in mind two entities with a M:N relationship between them will be converted into three entities.</li>

 <li>Come up with a M:N relationship early on so that your final ERD will have three tables related to each other (for example the Enroll relationship between STUDENT AND COURSE will be translated into three tables – STUDENT links to ENROLLMENT which links to COURSE). When writing advanced queries, you can easily develop ones with 3 table joins.</li>

 <li>Decide on your database project and plan not to revise your ERD midway, although you are free to do it. From past experiences students had difficulties when they did this because of time constraints.</li>

 <li>Format your deliverable as if you are submitting it professionally in a work environment (comments, structured output, etc.). Assume the reviewer is not an IT professional.</li>

</ul>





