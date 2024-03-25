# 










FACT TABLE


“Seethalaksmi achi college for women”
NM ID
  NAME
61E8D9FF90E82D980A24CF7A24F7E439
R.Sangeetha


Trainer name : R.Umamaheswari

Master Trainer name : R.Umamaheswari


 ABSTRACT
              
           In the realm of business intelligence (BI), the fact table serves as the cornerstone for analytical insights by storing quantitative data related to business processes. This project aims to design and implement a robust fact table suitable for BI applications, leveraging principles of data warehousing and dimensional modeling.
           The project begins with an in-depth analysis of the organization's data requirements and business processes to identify key performance indicators (KPIs) and metrics to be incorporated into the fact table. Following this, dimensional modeling techniques such as star schema or snowflake schema are employed to structure the fact table along with associated dimension tables, ensuring efficient querying and analysis.
           To validate the effectiveness of the designed fact table, a series of tests and performance evaluations are conducted, measuring query performance, data retrieval speed, and overall system scalability. Additionally, user feedback and stakeholder input are gathered to refine the fact table design and ensure alignment with business objectives.








INDEX




S. No.
Table of Contents
1
Chapter 1: Introduction
2
Chapter 2: Services and Tools Required 
3
Chapter 3: Project Architecture
4
Chapter 4: Modeling and Result
5
Conclusion
6
Future Scope
7
Links



				CHAPTER 1
INTRODUCTION
1.1 Problem Statement
In data warehousing, a fact table typically contains numerical measures or metrics that represent the business transactions or events being analyzed. The problem statement in a fact table describes the specific business questions or analytical requirements that the fact table is designed to address. It outlines what kind of data is being measured, at what granularity, and what dimensions (such as time, geography, or product) are associated with the measures. This statement serves as a guide for designing the fact table's structure and populating it with relevant data.
1.2 Proposed Solution
Proposed solutions for problems in fact tables depend on the specific issues encountered, but here are some common solutions:
1. Granularity Mismatch :     If the granularity of the fact table does not match the granularity required for analysis, you can aggregate or disaggregate the data to align with the desired level of detail.
 2. Missing or Incomplete Data :   If there are gaps in the data or missing values, you may need to fill them in using estimation techniques, imputation, or retrieving data from alternative sources. 
3. Inconsistent Data :    Address any inconsistencies in data by cleaning and standardizing it. This may involve correcting errors, removing duplicates, and ensuring data integrity.
 4. Performance Issues :    Optimize query performance by indexing frequently queried columns, partitioning the table, or using summary tables to pre-aggregate data for faster retrieval. 
5. Dimensional Integrity :     Ensure that relationships between the fact table and dimensioon tables are maintained. This can involve enforcing referential integrity constraints and properly handling dimension updates.
1.3 Features
The features in a fact table typically include:
 1. Foreign Keys :    These are references to dimension tables, linking the fact table to the relevant dimensions such as time, product, location, etc.
 2. Measure Columns: These are numerical values representing the metrics or measures of interest, such as sales revenue, quantity sold, profit margin, etc.
 3. Aggregated Measures :  Some fact tables may contain pre-aggregated measures for faster querying, especially in large datasets. These aggregates can include sums, averages, counts, etc.
 4. Surrogate Keys :  Sometimes, instead of using natural keys from dimension tables, surrogate keys are used in the fact table for better performance and easier maintenance.
 5. Date/Time Stamp :   A timestamp column indicating the date and time of the event or transaction being recorded in the fact table. 
6. Additional Attributes :  These are additional descriptive attributes related to the facts being recorded, such as transaction ..

1.4 Advantages
Fact tables offer several advantages in data warehousing and analytics:
 Efficient Data Analysis :   Fact tables are designed for efficient querying and analysis of business metrics and measures. They provide a centralized location for storing numerical data, making it easier to perform calculations, aggregations, and comparisons.
 Scalability :   Fact tables can handle large volumes of data, making them suitable for storing transactional or event-based data over time. They can scale horizontally by adding more records or vertically by adding more columns or measures. 
Flexibility :   Fact tables are flexible and can accommodate changes in business requirements. New measures or dimensions can be added to the fact table without affecting its overall structure, allowing for agile analytics.
Performance :  Fact tables are optimized for performance, especially when properly indexed and partitioned. This ensures fast query execution even on large datasets, enabling real-time or near-real-time analytics.
Dimensional Modeling :   Fact tables are a key component of dimensional modeling, which is a widely-used approach for organizing data in data warehousing. Dimensional modeling simplifies complex data structures and enhances query performance by organizing data into fact and dimension tables.
 Data Integration :   Fact tables facilitate data integration by consolidating data from multiple sources into a single, unified view. This enables analysts to perform comprehensive analysis and gain insights across various aspects of the business.
1.5 Scope
In data warehousing, the fact table contains the quantitative data that represents a business process or activity. The scope of a fact table typically includes: 
Measurements :  Numerical data representing the metrics of interest, such as sales revenue, quantity sold, or profit margin. 
Foreign keys :   References to dimension tables that provide context to the measurements, such as date, product, customer, etc. 
 Granularity :   The level of detail captured by each row, which could be transaction-level or aggregated over a certain period.
 Aggregated data :   Depending on the design, fact tables may contain pre-aggregated data to improve query performance for common analysis scenarios. 
 Temporal aspects :   Some fact tables may include timestamps or effective dates to track changes over time. 

CHAPTER 2
SERVICES AND TOOLS REQUIRED
2.1 Services Used
Data Collection and Storage Services :   Banks need to collect and store customer data in real-time. This could be achieved through services like Azure Data Factory, Azure Event Hubs, or AWS Kinesis for real-time data collection, and Azure SQL Database or AWS RDS for data storage. 
Data Processing Services :   Services like Azure Stream Analytics or AWS Kinesis Data Analytics can be used to process the real-time data. 
 Machine Learning Services :   Azure Machine Learning or AWS SageMaker can be used to build predictive models based on historical data. 2.2 Tools and Software used Tools: 
2.2 Tools and Software used
Tools :
PowerBI :  The main tool for this project is PowerBI, which will be used to create interactive dashboards for real-time data visualization.
 Power Query :   This is a data connection technology that enables you to discover, connect, combine, and refine data across a wide variety of sources. 

Software Requirements:
PowerBI Desktop :   This is a Windows application that you can use to create reports and publish them to PowerBI. 
PowerBI Service :   This is an online SaaS (Software as a Service) service that you use to publish reports, create new dashboards, and share insights. 
PowerBI Mobile :   This is a mobile application that you can use to access your reports and dashboards on the go.





CHAPTER 3 
PROJECT ARCHITECTURE
3.1 Architecture
         USER			       FRONTEND			BACKEND

HTML 5


NODEJS 14.0


Database


Primary Key:     A fact table usually has a composite primary key consisting of foreign keys from the dimension tables that it is associated with. These foreign keys are used to establish relationships with the dimension tables.

Foreign Keys:     Foreign keys are columns in the fact table that reference the primary keys of the associated dimension tables. These foreign keys are used to link the fact table to the various dimensions, providing context for the measures.

Measure Columns:   Measure columns, also known as facts, contain the numerical data that represents the business metrics being analyzed. These measures are usually additive, meaning they can be aggregated (e.g., summed up) across different dimensions.

Degenerate Dimensions:   Sometimes, a fact table may include attributes that do not belong to any dimension table but are still relevant to the analysis. These attributes are referred to as degenerate dimensions and are stored directly within the fact table.

Fact Grain:   The fact grain defines the level of detail at which the measures are recorded in the fact table. For example, a fact table in a sales database might record sales at the level of individual transactions (transactional grain) or aggregated at the daily, weekly, or monthly level (periodic grain).

Aggregate Columns:    In some cases, pre-aggregated or derived measures may be included in the fact table to improve query performance. These aggregates are typically calculated during the ETL (Extract, Transform, Load) process and stored alongside the raw measures.

Indexes:   Indexes may be created on the fact table to optimize query performance, especially for frequently accessed columns or combinations of columns.

Partitioning:   Fact tables can be partitioned based on certain criteria such as date ranges to improve query performance and manage data efficiently, especially in large-scale data warehousing environments.


				
			


				CHAPTER 4
 MODELING AND RESULT


Manage relationship




![Screenshot (21)](https://github.com/Sangeetharavi2003/Facttable1/assets/148191348/24c0cf79-c1e5-4b8b-8002-b6a2fc3320af)





















Dashboard

![Screenshot (18)](https://github.com/Sangeetharavi2003/Facttable1/assets/148191348/8657bf8a-da4b-4659-b4ef-03b033a661ad)
![Screenshot (19)](https://github.com/Sangeetharavi2003/Facttable1/assets/148191348/7ff0a189-ccde-42b1-94d5-ee2c74d07246)



				CONCLUSION

                     In conclusion, designing and implementing a fact table for a data warehousing critical aspect of building a robust and efficient analytical system. The fact table serves as the backbone of the data model, capturing the quantitative measures or "facts" of the business process being analyzed. Through proper architecture and design considerations, a well-constructed fact table facilitates insightful analysis and reporting by providing a structured framework for aggregating and correlating data across various dimensions.









FUTURE SCOPE


The future scope of fact tables lies in their evolution to meet the growing demands of increasingly complex data analytics and business intelligence needs. Here are several areas where fact tables are likely to evolve and expand their capabilities:
Advanced Analytics Integration:   Fact tables will increasingly incorporate advanced analytics techniques such as machine learning, predictive modeling, and natural language processing. This integration will enable organizations to derive deeper insights from their data, uncover hidden patterns, and make more accurate predictions.

Real-time Data Processing:   As businesses strive to make faster and more informed decisions, fact tables will evolve to support real-time data processing and analysis. This will involve the integration of streaming data sources and the development of techniques for processing and updating fact table data in near real-time.

Integration with Big Data Technologies:   Fact tables will leverage big data technologies such as Hadoop, Spark, and NoSQL databases to handle large volumes of data efficiently. This integration will enable organizations to store and analyze diverse data types, including unstructured and semi-structured data, alongside traditional structured data. 


Enhanced Data Visualization:   Fact tables will incorporate advanced data visualization capabilities to enable users to explore and interact with data more intuitively. This may include the integration of interactive dashboards, geospatial visualization, and augmented reality interfaces.

Semantic Data Modeling:   Fact tables will evolve to support semantic data modeling techniques, enabling organizations to establish richer relationships between data entities and derive more contextually relevant insights. This may involve the adoption of ontologies, knowledge graphs, and semantic web standards.

Blockchain Integration:   With the increasing focus on data security and integrity, fact tables may integrate blockchain technology to ensure the immutability and traceability of data transactions. Blockchain-enabled fact tables can provide enhanced data provenance and auditability, particularly in industries such as finance, healthcare, and supply chain management.

Automated Data Governance and Compliance:   Fact tables will incorporate automated data governance and compliance mechanisms to ensure adherence to regulatory requirements such as GDPR, HIPAA, and CCPA. This may involve the implementation of data lineage tracking, access control policies, and data anonymization techniques.


Edge Computing Integration:  With the proliferation of edge computing devices and IoT (Internet of Things) sensors, fact tables will evolve to support edge analytics and distributed data processing. This will enable organizations to analyze data closer to the source, reducing latency and bandwidth requirements.

                     Overall, the future of fact tables lies in their ability to adapt to evolving data analytics trends and technologies, enabling organizations to extract maximum value from their data assets and drive innovation in their respective industries.

















LINK





https://app.powerbi.com/groups/me/reports/94f2122e-7439-4929-948c-34780fe98ea7/ReportSection5d0a7d1bf69fabc101dd?experience=power-bi
