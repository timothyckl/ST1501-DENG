# Topic 1: Introduction to Data Engineering

1. [What is Data?](#what-is-data)
2. [How is Data generated?](#how-is-data-generated)
3. [Data Processing Systems](#data-processing-systems)
4. [Data Formats](#data-formats)
    - Structured Data
    - Unstructured Data 
    - Semi-structured Data

### What is Data?

- Data is information such as text, stream, audio, video and metadata. 
- Data can be structured unstructured or aggregated.
- Structured databases have a __defined schema__ (e.g. Azure SQL DB, Azure SQL Data Warehouse)
- Unstructured (NoSQL) databases can have different schemas for each data element at query time. 

### DIKW Model

![](https://i.imgur.com/LCMoaRp.png)

Each step up the pyramid answers questions about the initial data and adds value to it. The more questions we answer, the higher we move up the pyramid. In other words, the more we enrich our data with meaning and context, the more knowledge and insights we get out of it. At the top of the pyramid, we have turned the knowledge and insights into a learning experience that guides our actions.

### How is Data generated?

1) Human-Generated Data
    - New data is created whenever we make online purchases (transaction), post on social media, text our friends and make phone calls.
2) Machine-Generated Data
    - Data such as web crawlers, RFID readings and IoT data is automatically generated as a result of a process, application, other mechanism __without the active intervention of a person.__

### Data Processing Systems

Within the data science field, there are two types of data processing systems: online analytical processing (OLAP) and online transaction processing (OLTP). 

The main difference is that one uses data to gain valuable insights, while the other is purely operational. However, there are meaningful ways to use both systems to solve data problems.

![](https://i.imgur.com/mGuiOOn.png)

### What is OLTP?

Online transactional processing (OLTP) enables the real-time execution of large numbers of database transactions by large numbers of people, typically over the Internet. OLTP systems are behind many of our everyday transactions, from ATMs to in-store purchases to hotel reservations. OLTP can also drive non-financial transactions, including password changes and text messages.

### What is OLAP?

Online analytical processing (OLAP) is a system for performing multi-dimensional analysis at high speeds on large volumes of data. Typically, this data is from a data warehouse, data mart or some other centralized data store. OLAP is ideal for data mining, business intelligence and complex analytical calculations, as well as business reporting functions like financial analysis, budgeting and sales forecasting.

![](https://i.imgur.com/3yIVZY6.png)

### OLAP and OLTP Comparison

The main distinction between the two systems is in their names: analytical vs. transactional. Each system is optimized for that type of processing.

- OLTP is optimized for **processing a massive number of transactions.**
- OLTP systems are designed for **use by frontline workers** (e.g. cashiers, bank tellers) or for **customer self-service applications** (e.g. online banking, e-commerce).
- OLAP is optimized for **conducting complex data analysis** for smarter decision-making.
- OLAP systems are designed for **use by data scientists, business analysts and knowledge workers**, and they support business intelligence (BI), data mining and other decision support applications.

### Data Formats

![](https://i.imgur.com/9mTgpcx.png)

1) __Structured Data__ 
    - Structured data is data whose elements are **addressable for effective analysis**. It has been **organized into a formatted repository** (fixed fields) that is typically a database. It **concerns all data which can be stored in database SQL** in a table with **rows and columns**. 
    - Data are most processed and **simplest way to manage information** (e.g. Relational data).
 
2) __Semi-structured Data__ 
    - Semi-structured data is information that does not reside in a relational database (no fixed fields) but has **some organizational properties** that make it easier to analyze. With some processes, you can store them in the relation database, but **Semi-structured exist to ease space** (e.g. XML, JSON data). 

3) __Unstructured Data__ 
    - Unstructured data is **not organized in a predefined manner/does not have a predefined schema**, thus it is not a good fit for a mainstream relational database. There are alternative platforms for storing and managing such data, it is increasingly prevalent in IT systems and is used by organizations in a variety of business intelligence and analytics applications (e.g. Word, PDF, Text, Media logs).










