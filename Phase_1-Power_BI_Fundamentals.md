# Phase 1: Power BI Fundamentals


Welcome to your journey into **Power BI**! This phase lays the groundwork for everything you will build. We will start from the **absolute basics** and gradually introduce more advanced concepts, always tying them to **real‑world business scenarios**. Each lesson follows a consistent structure to ensure you not only learn how but also why – so you can apply these skills immediately.

By the end of this phase, you will be comfortable with the Power BI ecosystem, able to connect to data, understand the two main data connection modes, and navigate the workflow from data to dashboard.

---

## Lesson 1.1 – Introduction to Power BI

### Concept Explanation

**Power BI** is a suite of business analytics tools from Microsoft that allows you to connect to hundreds of data sources, transform and clean data, build interactive reports and dashboards, and share insights across your organization. It consists of:

* **Power BI Desktop** – a free Windows application for building reports (the primary tool we will use).

* **Power BI Service** – a cloud-based SaaS (Software as a Service) for sharing, collaborating, and accessing reports online.

* **Power BI Mobile** – apps for iOS, Android, and Windows to view reports on the go.

At its core, **Power BI turns raw data into visual stories** that help **decision‑makers spot trends**, **monitor KPIs**, and **make data‑driven decisions**.

---

### Importance and Real‑World Use Cases

* **Why it matters**: In today’s data‑driven world, organisations generate massive amounts of data. Power BI democratises data analytics – it empowers everyone, from analysts to executives, to explore data without deep programming skills.

* **Common use cases**:

    * **Sales Performance Dashboard** – track revenue, pipeline, and sales rep performance.

    * **Financial Reporting** – consolidate P&L statements from multiple ERP systems.

    * **Marketing Campaign Analytics** – measure ROI, conversion rates, and customer acquisition costs.

    * **Supply Chain Monitoring** – visualise inventory levels, order fulfilment times, and supplier performance.

    * **HR Analytics** – monitor headcount, turnover, and diversity metrics.

---

### Step‑by‑Step Demonstration

We will install Power BI Desktop later. For now, let’s open the application and take a first look:

1. Launch Power BI Desktop (you will see the start screen with options to get data, recent sources, and helpful links).

2. Click “**Get Data**” – this opens a window with dozens of connectors (Excel, SQL Server, Web, etc.).

3. Choose an **Excel workbook** or a **sample dataset** (e.g., “Financial Sample” provided by Microsoft).

4. Load the data – you will see the **Fields** pane on the right, showing tables and columns.

5. Drag a numeric field (e.g., `Sales`) to the **Report Canvas** – a visual appears automatically.

6. Change the visual type to a **bar chart**, a **line chart**, or a **map** – just by selecting from the Visualizations pane.

This simple walkthrough shows how quickly you can go from data to insight.

---

### Syntax and Rules (if applicable)

No syntax at this introductory stage – we are focusing on concepts. In later lessons, we will cover **DAX** (**Data Analysis Expressions**) and **M** (**Power Query**) languages.

---

### Practical Examples

* **Example 1**: You are a retail manager. You connect to a CSV file containing daily sales. You create a simple column chart showing sales by product category.

* **Example 2**: You are a HR analyst. You connect to an Excel file with employee data. You create a card visual showing total headcount, and a pie chart showing gender distribution.

---

### Hands‑on Exercises

1. Open Power BI Desktop and explore the interface: identify the **Report**, **Data**, and **Model views** (icons on the left sidebar).


2. Use the built‑in sample data (go to File → Open sample → select “Financial Sample”).

3. Create three visuals:

    * A **clustered column chart** showing `Sales` by `Country`.

    * A **slicer** for `Year` to filter the data.

    * A **card** showing total `Profit`.

4. Save your report as `MyFirstReport.pbix`.

---

### Mini Quiz

1. What are the three main components of Power BI?

2. What is the difference between Power BI Desktop and Power BI Service?

3. Name two real‑world scenarios where you would use Power BI.

4. Which pane in Power BI Desktop shows you all available tables and columns?

5. How can you change the type of a visual after it is created?

> _(Answers are provided at the end of this document.)_

---

### Common Mistakes and Best Practices

| Common Mistakes | Best Practices |
| :--- | :--- |
| Skipping data preparation – loading raw, messy data directly. | Always spend time cleaning and shaping data in Power Query before building visuals. |
| Using too many visuals on a single page – creates clutter. | Focus on 3–5 key visuals per page; use bookmarks and drill-through for depth. |
| Not giving meaningful names to visuals and fields. | Rename fields (e.g., “Sales Amount” instead of “Sum of Sales”) for clarity. |
| Forgetting to save frequently. | Save your .pbix file regularly – Power BI can crash on large datasets. |

---

### Interview Questions

1. What is Power BI and how does it differ from Excel?

    **Answer**: Power BI is designed for interactive visualisation and sharing, handles larger datasets, and supports live connections. Excel is more for ad‑hoc analysis and individual use.

    ---

2. Can Power BI handle big data?
    
    **Answer**: Yes, through DirectQuery, live connections to big data platforms (e.g., Azure SQL Data Warehouse), and the ability to use incremental refresh.

    ---

3. What are the pricing models for Power BI?
        
    **Answer**: Power BI Desktop is free. Power BI Pro (per user/month) and Premium (capacity‑based) are the paid service tiers for sharing and advanced features.

---

### Assignment and Dashboard Projects

#### Assignment 1 – Build a simple “Executive Dashboard” using the Financial Sample dataset:

* Include:

    * Total Revenue (card)

    * Revenue by Product (bar chart)

    * Revenue by Country (map)

    * Revenue trend over time (line chart)

    * Slicers for Year and Product

* Save your report and be ready to present it (to yourself or a peer).

**Dashboard Project (end of phase)** : We will combine all lessons to build a comprehensive sales dashboard with KPIs, drill‑through, and interactive filtering.

---

### Summary and Revision Notes

* Power BI is a complete BI tool: Desktop (authoring), Service (sharing), and Mobile (access).

* It connects to diverse data sources and creates interactive visuals.

* The workflow: **Get Data** → **Transform** → **Model** → **Visualise** → **Share**.

* Key interface areas: **Report** (canvas), **Data** (table view), **Model** (relationships), **Visualizations pane**, **Fields pane**, and **Filters pane**.

---
## Lesson 1.2 – Business Intelligence Concepts

### Concept Explanation

**Business Intelligence (BI)** is the process of **collecting**, **storing**, **analysing**, and **presenting data** to **support better decision‑making**. It encompasses technologies, applications, and practices. Power BI is a BI tool – but understanding the underlying concepts will help you use it more effectively.

Key BI terms:

* **ETL**: Extract, Transform, Load – the process of pulling data, cleaning it, and loading it into a data model.

* **Data Warehouse**: A centralised repository that stores integrated data from multiple sources, optimised for querying and analysis.

* **OLAP vs OLTP**: Online Analytical Processing (for reporting, aggregations) vs Online Transaction Processing (for daily transactions).

* **Star Schema**: A common data modelling design with a central fact table (events/transactions) and surrounding dimension tables (descriptive attributes).

* **KPIs (Key Performance Indicators)** : Quantifiable measures used to track performance against objectives (e.g., Revenue Growth, Customer Churn).

---

### Importance and Real‑World Use Cases

**Why it matters**: **BI transforms raw data into actionable insights**. Without BI, organisations rely on intuition or gut feeling – which can be risky. BI provides evidence‑based answers to questions like: “Which product lines are underperforming?” or “Which marketing channel gives the best ROI?”

**Use cases:**

* **Financial consolidation**: Combine data from subsidiaries to produce group‑level reports.

* **Customer 360**: Understand customer behaviour, lifetime value, and segmentation.

* **Operational efficiency**: Monitor production line downtime and quality defects.

* **Competitive analysis**: Benchmark your performance against industry averages.

---

### Step‑by‑Step Demonstration (Conceptual)

We will illustrate a simple BI workflow:

1. **Extract**: Pull sales data from an SQL database and product data from an Excel file.

2. **Transform**: Clean product names, convert currencies, remove duplicate orders.

3. **Load**: Import into Power BI’s data model.

4. **Model**: Create relationships between Sales and Product tables.

5. **Visualise**: Build a dashboard that shows sales by product category and region.

6. **Share**: Publish to Power BI Service so that managers can access it on their tablets.

We will execute these steps practically in later lessons.


---

### Syntax and Rules (if applicable)

No code syntax in this lesson. **We will cover DAX and M later.**

---

### Practical Examples

* **Example**: A retail chain wants to know which stores are underperforming. They use BI to compare sales, footfall, and conversion rates across all stores, then drill down to individual store performance.

---

### Hands‑on Exercises

1. Think about a business question you would like to answer (e.g., “Are our online sales growing faster than in‑store?”).

2. Identify at least two data sources you would need to answer that question.

3. Draw a simple star schema on paper (one fact table, two dimension tables) for a sales scenario.

---

### Mini Quiz

1. What does ETL stand for?

2. What is the difference between a fact table and a dimension table?

3. Name three KPIs that a sales manager might monitor.

4. What is a data warehouse?

5. Why is BI important for decision‑making?

---

### Common Mistakes and Best Practices

| Common Mistakes | Best Practices |
| :--- | :--- |
| Building reports without a clear business question – you end up with "chart junk". | Always start with a specific question or hypothesis. |
| Using data that hasn't been verified for accuracy. | Validate data quality early; involve business users to confirm definitions. |
| Over-complicating the data model with unnecessary tables. | Keep the model as simple as possible; use calculated columns and measures sparingly. |

---

### Interview Questions

1. **What is the difference between BI and data analytics?**

    **Answer:** 
    
    BI is the broader umbrella that includes the entire process from data collection to reporting; analytics is more focused on statistical analysis and predictive modelling.

    ---

2. **How do you ensure that your BI reports drive action?**

    **Answer:** 
    
    By aligning KPIs with business strategy, presenting data in a clear narrative, and providing drill‑down capabilities to investigate root causes.

    ---

3. **What is a star schema and why is it used in BI?**

    **Answer:** 
    
    It is a dimensional model that optimises query performance and ease of understanding; it has a central fact table with measures and surrounding dimension tables with descriptive attributes.

---

### Assignment and Dashboard Projects

#### Assignment 2 – Write a one‑page business case for a dashboard you would like to build. Describe:

* The business problem.

* The KPIs you will track.

* The data sources required.

* The expected users and how they will interact with the dashboard.

---

### Summary and Revision Notes

* BI is about turning data into actionable insights.

* Key concepts: ETL, data warehouses, star schemas, KPIs.

* Power BI is a tool that implements the entire BI workflow from data prep to sharing.

* Always start with a business question.

---

## Lesson 1.3 – Installing and Setting Up Power BI Desktop

### Concept Explanation

Power BI Desktop is the primary authoring tool. It is free and available for download from the Microsoft website. It runs only on Windows (64‑bit recommended). It includes everything you need to connect, transform, model, and visualise data.

### Importance and Real‑World Use Cases

* **Why it matters**: Without the correct installation, you cannot start building reports. Also, understanding system requirements and update policies ensures smooth performance.

* **Use cases**: Installation is the first step for any new Power BI user. Also, in enterprise settings, IT may need to deploy it across many machines; knowing the options (e.g., MSI installer) is valuable.

---

### Step‑by‑Step Demonstration

1. **Check system requirements:**

    * Windows 10/11 (or Windows Server 2016+).

    * .NET Framework 4.6.2 or later.

    * At least 2 GB RAM (4+ GB recommended), and sufficient disk space.

2. **Download:**

    * Go to powerbi.microsoft.com/downloads.

    * Click “Download” under “Power BI Desktop”.

    * Choose the 64‑bit version (the default) unless you have specific 32‑bit requirements.

3. **Install:**

    * Run the installer (.exe file).

    * Accept the license terms.

    * Choose an installation location (default is fine).

    * Click “Install”.

4. **Launch:**

    * After installation, find “Power BI Desktop” in the Start menu.

    * When you launch it for the first time, you may be prompted to sign in (optional; you can skip).

    * The start screen appears.

**Option for enterprise**: Microsoft also provides an MSI installer for mass deployment via group policy.

---

### Syntax and Rules (if applicable)

**No syntax**; just installation steps.

---

### Practical Examples

* **Example**: You are a consultant setting up Power BI on a client’s laptop. You check that the system is Windows 10 Pro, has 8 GB RAM, and install the 64‑bit version. You also ensure that the client has the appropriate permissions to install software.

---

### Hands‑on Exercises

1. Download and install Power BI Desktop on your machine.

2. Launch it and explore the start screen.

3. Check the version: go to **File → About** and note the version number (so you know when updates are available).

4. Sign in with your work or personal Microsoft account (optional) to enable sharing features.

---

### Mini Quiz

1. What are the minimum RAM requirements for Power BI Desktop?

2. Where can you download Power BI Desktop?

3. What is the difference between the .exe and .msi installers?

4. What should you check before installing Power BI Desktop?

---

# Common Mistakes and Best Practices

| Common Mistakes | Best Practices |
| :--- | :--- |
| Installing the 32-bit version on a 64-bit system – limits memory usage. | Always install the 64-bit version unless you have legacy dependencies. |
| Installing on a machine with insufficient RAM – leads to slow performance. | Ensure at least 4 GB RAM for moderate datasets. |
| Forgetting to enable automatic updates. | Go to [File](#) → [Options](#) → [Global](#) → [Update](#) and enable “Update automatically” (or check for updates regularly). |

---

### Interview Questions

1. **How do you update Power BI Desktop?**

    **Answer:** 
    
    The app prompts when a new version is available; you can also download the latest installer from the official site. Updates are monthly.

    ---

2. **Can you install Power BI Desktop on a Mac?**

    **Answer:** 
    
    Not natively; you need to run Windows via Boot Camp or a virtual machine (Parallels, VMware).

    ---

3. **What is the purpose of signing in to Power BI Desktop?**

    **Answer:** 
    
    To connect to Power BI Service for publishing, to access shared datasets, and to enable certain features like dataflow connections.

---

### Assignment and Dashboard Projects

* **Assignment 3** – Write a short step‑by‑step guide (with screenshots or descriptions) for installing Power BI Desktop on a fresh Windows machine. Include troubleshooting tips (e.g., admin rights, firewall).

---
### Summary and Revision Notes

* Download from Microsoft official site.

* Choose 64‑bit for better performance.

* Installation is straightforward; sign‑in is optional but recommended for cloud integration.

* Keep the tool updated to access latest features.

---

## Lesson 1.4 – Understanding the Power BI Interface

### Concept Explanation

Power BI Desktop has three main views (tabs on the left sidebar):

* **Report** – the canvas where you build visuals, add slicers, and design interactive pages.

* **Data** – a spreadsheet‑like view of your loaded tables, where you can inspect data, create calculated columns, and format columns.

* **Model** – a diagram view showing your tables and the relationships between them; you can create and edit relationships here.

Other key UI elements:

* **Ribbon (top)** – contains tabs like Home, Insert, Modeling, View, Help.

* **Visualizations pane** – shows all available chart types and allows formatting.

* **Fields pane** – lists all tables and columns; you drag fields from here onto visuals.

* **Filters pane** – allows you to apply filters at visual, page, or report level.

* **Pages** – at the bottom, you can add new report pages, rename, duplicate, or reorder them.

* **Bookmarks and Selection panes** – advanced features for storytelling.

---

### Importance and Real‑World Use Cases

* **Why it matters**: Knowing your way around the interface drastically speeds up report development. You will spend most of your time in the Report view, but data modelling and data preparation are equally important.

* **Use cases**: When you are building a dashboard, you will switch between views: checking raw data in Data view, setting relationships in Model view, and designing visuals in Report view.

---

### Step‑by‑Step Demonstration

* **Navigate views**: Click each icon on the left (Report, Data, Model) – note how the panes change.

* **Explore the ribbon**: On the Home tab, find “Get Data”, “Refresh”, and “Publish”. On the Modeling tab, you can create new measures and columns.

* **Work with fields**: In Report view, drag Sales from the Fields pane to the canvas – a column chart appears. Click on the visual, then on the paint roller icon in the Visualizations pane to format colours, labels, etc.

* **Add a new page**: Click the “+” at the bottom to create Page 2.

* **Use slicers**: Drag a categorical field (e.g., Product Category) to the canvas and choose Slicer from the visualisation list – this creates an interactive filter.

---

### Syntax and Rules (if applicable)

**No syntax** – but note that the interface may change slightly with monthly updates; the concepts remain the same.

---

### Practical Examples

* **Example**: You are building a sales report. You use the Data view to check for null values in the `Country` column, the Model view to join `Sales` with `Product` on `ProductID`, and the Report view to create a map visual.

---

### Hands‑on Exercises

1. Load the Financial Sample dataset (File → Open sample → Financial Sample).

2. Switch to Data view and inspect the table – note the number of rows and columns.

3. Switch to Model view – see the table on the canvas (no relationships yet, since it’s a single table).

4. Return to Report view and create:

    * A line chart showing `Sales` over `Date`.

    * A slicer for `Segment`.

5. Apply the slicer and see the line chart update.

6. Duplicate the page (right‑click page tab → Duplicate) and change the visual to a bar chart.

---

### Mini Quiz

1. Which view would you use to create relationships between tables?

2. Which pane contains all the visualisation types?

3. How do you add a new report page?

4. What is the purpose of the Filters pane?

5. Where can you format a visual’s colours and labels?

---

### Common Mistakes and Best Practices

| Common Mistakes | Best Practices |
| :--- | :--- |
| Staying only in Report view and ignoring Data/Model views. | Regularly check Data view to understand data quality; use Model view to ensure correct relationships. |
| Overlooking the Filters pane – applying filters only via slicers. | Use page-level and report-level filters for global constraints (e.g., “Current Year Only”). |
| Not renaming pages or visuals – causes confusion in large reports. | Give descriptive names to each page (e.g., “Sales Overview”, “Product Detail”) and to visuals. |

---

### Interview Questions

1. **What is the difference between a slicer and a filter?**

    **Answer:** 
    
    A slicer is a visual that allows users to filter the report interactively; a filter is applied in the Filters pane and can be set at visual, page, or report level.

    ---

2. **How do you create a calculated column?**

    **Answer:** 
    
    In the Data view, click on “New Column” in the Modeling tab and write a DAX expression.

    ---

3. **What are bookmarks used for?**

    **Answer:** 
    
    Bookmarks capture the current state of a page (filters, visuals, slicers) to allow users to navigate between different “views” or stories.

---

### Assignment and Dashboard Projects

**Assignment 4** – Open a new Power BI Desktop file, load any dataset (e.g., Excel file with sales data). Create a 3‑page report:

* **Page 1:** Summary with cards and a line chart.

* **Page 2:** Detailed table with slicers.

* **Page 3:** Geographic map (if you have location data).

* Rename each page appropriately. Save the file.

---

### Summary and Revision Notes

* **Three views**: Report (design), Data (inspect), Model (relationships).

* **Key panes**: Visualizations, Fields, Filters.

* Use pages to organise content; use slicers for interactivity.

* Familiarity with the interface saves time and reduces errors.

---

## Lesson 1.5 – Data Sources and Data Connections

### Concept Explanation

Power BI can connect to a vast array of data sources:

* **Files**: Excel (.xlsx, .xls), CSV, XML, JSON, PDF, etc.

* **Databases**: SQL Server, Oracle, MySQL, PostgreSQL, IBM DB2, etc.

* **Cloud services**: Azure SQL Database, Azure Data Lake, Google BigQuery, Amazon Redshift, Salesforce, Dynamics 365, etc.

* **Online services**: SharePoint Online, Google Analytics, Facebook, etc.

* **Other**: OData feeds, Web APIs (REST), Active Directory, etc.

**Connections can be made via:**

* **Get Data** button on the Home ribbon.

* **Recent sources** for quick reuse.

* **Power Query** (the query editor) for advanced transformations before loading.

---

### Importance and Real‑World Use Cases

* **Why it matters**: The ability to connect to multiple sources allows you to build comprehensive reports that combine data from different departments. For example, merging sales from SQL with budget data from Excel.

* **Use cases**:

    * A CFO consolidates financial data from an on‑premise SQL Server and a cloud‑based ERP.

    * A marketing analyst pulls campaign data from Google Analytics and Salesforce.

    * A supply chain manager connects to an Azure Data Lake for logistics data.

---

### Step‑by‑Step Demonstration

####  1. Connect to Excel:

* Click **Get Data → Excel**.

* Browse and select your .xlsx file.

* In the Navigator window, check the sheets/tables you want to load.

* Click **Load** (direct load) or **Transform Data** (to clean in Power Query).

#### Connect to SQL Server:

* Click **Get Data** → **SQL Server**.

* Enter the Server name and Database (optional).

* Choose Import or DirectQuery (we cover this in the next lesson).

* Provide credentials (Windows or SQL authentication).

* Select tables/views and load.

#### Connect to Web:

* Click **Get Data → Web**.

* Enter a URL that returns data (e.g., a CSV file hosted online or an OData feed).

* Provide any necessary authentication.

* Preview and load.

---

### Syntax and Rules (if applicable)

* No syntax, but note that when connecting to databases, you may need to write SQL queries (e.g., `SELECT * FROM Sales`). Power BI allows you to enter native SQL queries in the Advanced options.

* For web APIs, you may need to provide parameters (e.g., API keys) in the URL or via headers – this is handled in Power Query.

---

### Practical Examples

* **Example 1:** You have monthly sales reports in CSV files. You use Power BI’s Folder connector to combine all CSV files in a folder, automatically appending them.

* **Example 2:** You connect to a SQL Server view that already pre‑aggregates daily sales; you load that directly.

---

### Hands‑on Exercises

1. Download a sample Excel file from the internet (e.g., from Kaggle) and connect to it.

2. Connect to a public web data source (e.g., a CSV from data.gov).

3. In the Navigator, select only specific columns (using the “Transform Data” option) before loading.

4. Load both data sources into the same Power BI file (they will appear as separate tables).

5. In Model view, try to create a relationship between them (if they share a common key).

---

### Mini Quiz

1. List three types of data sources Power BI can connect to.

2. What is the Navigator window used for?

3. How do you combine multiple Excel files from a folder?

4. What is the difference between “Load” and “Transform Data” when getting data?

5. Can you connect to an Oracle database? If so, what additional software might you need?

---

### Common Mistakes and Best Practices

| Common Mistakes | Best Practices |
| :--- | :--- |
| Loading entire tables instead of selecting only necessary columns – increases memory usage. | Use "Transform Data" to remove unnecessary columns before loading. |
| Using default credentials when connecting to sensitive data sources – may cause permission errors. | Always configure proper authentication (e.g., use Windows Authentication, OAuth, or stored credentials). |
| Not using parameters for changing file paths or server names. | Use Power Query parameters to make reports portable (e.g., for development vs. production). |

---

### Interview Questions


1. **What are the most common data sources used in Power BI in an enterprise environment?**

    **Answer:** SQL Server, Azure SQL, Excel, SharePoint, and often cloud data warehouses like Snowflake or BigQuery.

    ---

2. **How do you handle large data volumes when connecting to a database?**

    **Answer:** Use DirectQuery (to avoid importing all data), or filter data at the source using SQL queries, or use incremental refresh.

    ---

3. **Can you connect to an on‑premise data source from Power BI Service?**

    **Answer:** Yes, using a Data Gateway (on‑premises data gateway) to bridge cloud and on‑premise environments.

---

### Assignment and Dashboard Projects

**Assignment 5** – Create a report that combines two different sources:

* **Source 1**: Excel file with product information.

* **Source 2**: CSV file with sales transactions.

* Load both, establish a relationship (e.g., `ProductID`), and create a visual showing total sales by product category.

---

### Summary and Revision Notes

* Power BI supports a wide variety of data sources – files, databases, cloud services, and web APIs.

* Use **Get Data** to connect; use Navigator to select tables and preview.

* Always consider which columns you really need to reduce load.

* Use Transform Data to open Power Query Editor for cleaning and shaping.

---

## Lesson 1.6 – Import Mode vs DirectQuery

#### Concept Explanation

When you connect to a data source, you have two primary storage modes:

* #### Import Mode:

    * Data is loaded into Power BI’s in‑memory engine (VertiPaq) and stored in the .pbix file.

    * All queries run against the cached data – extremely fast performance.

    * You can use all DAX functions and complex calculations.

    * Data is static until you refresh (manually or scheduled).

* #### DirectQuery:

    * Data is not imported; instead, Power BI sends queries directly to the underlying source (e.g., SQL Server) every time you interact with a visual.

    * Data is always up‑to‑date (no refresh needed).

    * Performance depends on the source’s response time and network latency.

    * Some DAX functions are not supported, and certain modelling features are limited.

There is also **Composite Model** – a hybrid where some tables are Imported and others are DirectQuery, allowing you to combine both approaches.

---

### Importance and Real‑World Use Cases

* **Why it matters**: Choosing the right mode is critical for report performance and data freshness. If you need real‑time data, DirectQuery is attractive; if you need complex calculations and fast visuals, Import is better.

* **Use cases**:

    * **Import** for historical analysis (e.g., monthly sales reports) where data does not change frequently.

    * **DirectQuery** for operational dashboards that must reflect the latest transactions (e.g., live inventory levels).

    * **Composite** for scenarios where you have a large fact table (DirectQuery) and small dimension tables (Import) to balance performance.


---

### Step‑by‑Step Demonstration

1. **Connect to SQL Server** – In the Get Data dialog, after entering server and database, you will see a Data Connectivity mode dropdown:

    * Choose Import or DirectQuery.

2. **Select tables** – For DirectQuery, you cannot perform complex transformations in Power Query (many steps are limited). You will see a warning.

3. **Build a visual** – In Import mode, changing a slicer is instantaneous. In DirectQuery, each slicer change sends a new query to the database – you may notice a slight delay.

4. **Check the model** – In DirectQuery, certain features like calculated tables, calculated columns with time intelligence, and some DAX functions (e.g., `RANKX` over aggregated data) are disabled or have performance implications.

---

### Syntax and Rules (if applicable)

* No specific syntax, but understanding the limitations is key:

    * In DirectQuery, DAX measures that aggregate large datasets can be slow; it’s better to push aggregations to the source.

    * You cannot use M (Power Query) transformations that are not supported by the source (e.g., merging tables across different sources may not be allowed).

* **Best practice**: Use Import for all but the largest datasets, or when real‑time is a strict requirement.

---

### Practical Examples

* **Example 1**: You are building a dashboard for a retail chain to monitor hourly sales. You use DirectQuery to an Azure SQL Database so that store managers see live data.


* **Example 2**: You are building a year‑over‑year trend report for the board. You use Import mode because the data is static (only refreshed monthly) and you need complex DAX time intelligence.

---

### Hands‑on Exercises

1. Connect to the Financial Sample (which is loaded as Import by default). Note the performance.

2. Try to connect to a SQL Server (if you have access) using DirectQuery, or simulate by using a large CSV (though CSV is always imported).

3. If you have a SQL Server, create a DirectQuery report and compare the response time with a similar Import report.

4. Create a measure in Import mode that uses `CALCULATE` and time intelligence. Then try to create the same measure in DirectQuery mode – note the differences (some functions may not work).

---

### Mini Quiz

1. What is the main advantage of Import mode?

2. When would you choose DirectQuery?

3. Can you use calculated columns in DirectQuery?

4. What is a Composite model?

5. How does DirectQuery affect performance?

---

### Common Mistakes and Best Practices

| Common Mistakes | Best Practices |
| :--- | :--- |
| Using DirectQuery for every report because it "feels" real-time – but causing slow performance. | Reserve DirectQuery only when real-time is required and the source is optimised for query performance. |
| Applying heavy transformations in Power Query when using DirectQuery – these are pushed to the source and may be slow. | Perform transformations in the source (e.g., create views) or use Import mode for complex shapes. |
| Not using Aggregations in DirectQuery to improve performance (e.g., creating pre-aggregated tables). | Consider using aggregations or a composite model to cache high-level summaries. |

---

### Interview Questions

1. **What is the difference between Import and DirectQuery in terms of data refresh?**

    **Answer**: Import requires a manual or scheduled refresh to update data; DirectQuery always shows the latest data from the source without refresh.

    ---

2. **How do you decide which mode to use?**

    **Answer**: Consider dataset size, required data freshness, complexity of DAX, and source performance. Use Import for smaller to medium datasets and complex calculations; use DirectQuery for large datasets that need real‑time updates.

    ---

3. **What are the limitations of DirectQuery?**

    **Answer**: Limited DAX functions, no calculated tables (except via views), slower performance with many visuals, and limited transform capabilities in Power Query.

---

### Assignment and Dashboard Projects

**Assignment 6** – Write a report comparing the performance of Import vs DirectQuery. Use a large public dataset (e.g., from `data.gov`). If you don’t have a database, simulate by using a large CSV (import) and note the load time. For DirectQuery, try connecting to a sample Azure SQL database (free tier) and measure response times for visuals. Document your findings and recommendations.

---

### Summary and Revision Notes

* Import mode: fast, offline, but needs refresh.

* DirectQuery: real‑time, but slower and limited DAX.

* Composite mode: best of both worlds.

* Choose based on data volume, freshness needs, and performance requirements.

---

## Lesson 1.7 – Understanding the Power BI Workflow

### Concept Explanation

The typical workflow in Power BI can be broken down into six steps:

* **Get Data** – Connect to one or more data sources (files, databases, web).

* **Transform Data** – Clean, reshape, and enrich data using Power Query Editor (remove columns, change data types, merge/append tables, add custom columns, etc.).

* **Model Data** – Define relationships between tables, create calculated columns and measures (using DAX), and organise tables into a star schema.

* **Visualise Data** – Drag fields onto the report canvas, choose visuals, apply filters, and arrange layouts.

* **Share Reports** – Publish to Power BI Service, create dashboards, set up scheduled refresh, and manage permissions.

* **Consume and Iterate** – End‑users view reports/dashboards; they provide feedback; you refine the report.

This workflow is iterative – you often go back to earlier steps as new requirements emerge.

---

### Importance and Real‑World Use Cases

* **Why it matters**: Understanding the workflow ensures you don’t skip critical steps (like data modelling) that could lead to inaccurate reports. It also helps you collaborate with others (e.g., data engineers who prepare the data, business users who define KPIs).

* **Use cases**: A typical project: Business users ask for a sales dashboard. You connect to the data warehouse, clean the data, build relationships, create measures (e.g., `Total Sales`, `% Growth`), design visuals, publish, and then adjust based on user feedback.

---

### Step‑by‑Step Demonstration (End‑to‑End)

We will walk through a mini‑project:

1. **Get Data**: Connect to the “Financial Sample” (built‑in) or an Excel file.

2. **Transform**: Open Power Query Editor (by clicking “Transform Data”). Notice the data. Change the `Date` column type to Date. Remove any columns you don’t need (e.g., `Units Sold`? We’ll keep it).

3. **Model**: In Model view, create a calculated column: `Year` = YEAR([Date]). Create a measure: `Total Sales` = SUM(Financials[Sales]).

4. **Visualise**: Build a report page with:

    * Card: `Total Sales`.

    * Clustered bar chart: Sales by Product.

    * Line chart: Sales over time.

    * Slicer: Year.

* **Share**: Publish to Power BI Service (requires a Pro license). Set up a scheduled refresh (if data source supports it).

* **Iterate**: After sharing, a user asks for a breakdown by country. You go back to step 2, add a country field, update the model, and republish.

This demonstrates the iterative nature.

---

### Syntax and Rules (if applicable)

* We will cover DAX in later phases, but for now, note that you can create measures using simple aggregation functions like `SUM`, `AVERAGE`, `COUNT`.

* Power Query M syntax will be covered in Phase 2; for now, we use the UI.

---

### Practical Examples

* **Example**: A project to build a customer churn dashboard. Workflow:

1. Connect to CRM database and usage logs.

2. Transform: clean missing values, merge datasets.

3. Model: define relationships, create measures for churn rate, active customers.

4. Visualise: show churn trend, segmentation by plan type.

5. Share: publish to the customer success team.

6. Iterate: add a “predicted churn” column based on a simple rule.

---

### Hands‑on Exercises

1. Open Power BI Desktop and start a new file.

2. Load the Financial Sample.

3. In Power Query Editor, do the following:

    *   Change the data type of `Date` to Date.

    *   Add a new column using “Add Column” → “Custom Column” with formula: `[Sales] * 0.8` to simulate cost. Name it `Cost`.

    *   Remove the `Segment` column (if you think it’s unnecessary).

    *   Close & Apply.

4. In Report view, create:

    * A measure `Total Profit` = SUM(Financials[Sales]) - SUM(Financials[Cost]).

    * A visual showing Profit by Country.

5. Save and publish (if you have a Power BI Service account) – or just save the .pbix.


---

### Mini Quiz

1. List the six steps of the Power BI workflow.

2. What is the purpose of the Power Query Editor?

3. Why is data modelling important?

4. How do you share a report with others?

5. What does “iteration” mean in this context?


---

### Common Mistakes and Best Practices

| Common Mistakes | Best Practices |
| :--- | :--- |
| Skipping data transformation – leads to wrong numbers and slow performance. | Always inspect data in Power Query; clean it before loading. |
| Not using measures for calculations – instead creating calculated columns that increase file size. | Use measures for aggregations; use calculated columns only for row-level calculations (e.g., concatenation, flags). |
| Publishing without testing – broken visuals or wrong data. | Test thoroughly in Desktop; use the “Analyze in Excel” feature to check accuracy. |
| Forgetting to set up refresh for imported data. | Configure scheduled refresh in Power BI Service after publishing. |

---

### Interview Questions

1. **Walk me through the process of building a Power BI report from scratch.**

    **Answer**: 
    
    (Summarise the six steps, highlighting the importance of each.)

    ---

2. **How do you handle changes to the data source (e.g., a new column added)?**

    **Answer**: 
    
    Go to Power Query Editor, refresh the preview, then adjust transformations accordingly; then update the model and visuals.

    ---

3. **What is the difference between a measure and a calculated column?**

    **Answer**: 
    
    A calculated column is computed row‑by‑row during data load and stored; a measure is computed dynamically during visualisation based on the current context.

---

### Assignment and Dashboard Projects

**Assignment 7** (Final Project for Phase 1) – Build a complete dashboard from start to finish using a dataset of your choice (or use the Adventure Works sample). Follow the entire workflow:

* Connect to at least two data sources (e.g., Excel + CSV).

* Transform data (clean, merge/append, add a custom column).

* Model relationships and create at least two measures.

* Create a multi‑page report with:

    *   **Page 1**: Summary KPIs and trends.

    *   **Page 2**: Detailed breakdown by dimension (e.g., product, region).

    *   **Page 3**: Drill‑through details (optional).

* Add slicers and interactivity.

* Save your .pbix file and (if possible) publish to Power BI Service.

* Write a one‑page reflection on your choices (why you chose certain visuals, challenges you faced).

---

### Summary and Revision Notes

* The workflow is cyclical: Get Data → Transform → Model → Visualise → Share → Iterate.

* Power Query is your data preparation powerhouse.

* Modelling (relationships and DAX) is the backbone of accurate reporting.

* Visualisation is about telling a story, not just showing numbers.

* Sharing and iteration ensure the report remains valuable over time.

---

## Final Phase 1 Assessment

Now that you have completed all lessons, it’s time to consolidate your knowledge.

### Self‑Evaluation Checklist

* I can explain what Power BI is and its components.

* I understand the basic BI concepts (ETL, star schema, KPIs).

* I have installed Power BI Desktop and am familiar with its interface.

* I can connect to various data sources (Excel, CSV, databases).

* I understand the differences between Import and DirectQuery.

* I can perform basic data transformations in Power Query Editor.

* I can create simple relationships in the Model view.

* I can create basic measures (SUM, AVERAGE).

* I can build interactive reports with visuals, slicers, and filters.

* I know how to publish a report to Power BI Service.

* If you checked all, you are ready for Phase 2: Data Transformation and Modelling.

---

### Answers to Mini Quizzes

#### Lesson 1.1:

1. Desktop, Service, Mobile.

2. Desktop is for authoring, Service is for sharing and collaboration.

3. Sales performance, financial reporting, marketing analytics (any two).

4. Fields pane.

5. Select the visual and choose a different icon from the Visualizations pane.

    ---

#### Lesson 1.2:

1. Extract, Transform, Load.

2. Fact table contains quantitative measures; dimension tables contain descriptive attributes.

3. Revenue, profit margin, customer acquisition cost (any three).

4. A centralised repository of integrated data from multiple sources.

5. It provides evidence‑based insights for better decision‑making.

    ---

#### Lesson 1.3:

1. 2 GB (4 GB recommended).

2. powerbi.microsoft.com/downloads.

3. .exe is for individual installation; .msi is for enterprise deployment via group policy.

4. OS version, .NET Framework, available RAM.

    ---

#### Lesson 1.4:

1. Model view.

2. Visualizations pane.

3. Click the “+” at the bottom of the page tabs.

4. To apply filters at visual, page, or report level.

5. In the Visualizations pane, under the Format (paint roller) icon.

    ---

#### Lesson 1.5:

1. Excel, SQL Server, Web (any three).

2. It previews the data and lets you select which tables/columns to load.

3. Use the Folder connector and combine binaries.

4. Load imports immediately; Transform Data opens Power Query Editor for cleaning.

5. Yes, you may need to install Oracle client drivers.

    ---

#### Lesson 1.6:

1. Fast performance and full DAX functionality.

2. When you need real‑time data and have a high‑performance source.

3. Yes, but with limitations (some DAX functions not supported).

4. A model that combines Import and DirectQuery tables.

5. Each interaction sends a query to the source, which can be slower and put load on the source.

    ---

#### Lesson 1.7:

1. Get Data, Transform, Model, Visualise, Share, Iterate.

2. To clean, reshape, and combine data before loading.

3. To ensure correct relationships and calculations for accurate reports.

4. Publish to Power BI Service and share with users via workspace permissions.

5. Repeatedly refining the report based on user feedback and new requirements.

---

**Congratulations**! 🎉 You have completed Phase 1. You now have a solid foundation in Power BI. Keep practising and building your own dashboards – the best way to learn is by doing.

----

<br/><br/><br/>
<center> <b>Happy Learning! 😊</b> </center>