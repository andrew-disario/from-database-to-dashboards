<h1>From Database to Dashboards</h1>
<p align="center">
<img src="https://github.com/andrew-disario/pizza-database-and-dashboards/blob/main/pizza-database-and-dashboards.png?raw=true" height="100%" width="100%" alt="pizza-database-and-dashboards"/>
</br> Build and design a MySQL database and create interactive dashboards to model revenue and inventory data.
  
<h2>PART I - Design and Build a Relational Database</h2>

<b>Design a Database with Quick Database Diagrams (Optional)</b>

1. Go to [quickdatabasediagrams.com](https://www.quickdatabasediagrams.com/).
2. Select **Try The App**.
	- Login or create an account if you do not already have one. (Recommended)
3. Use the interface to design your database.
	- Input the text from [pizza-quickdbd.txt file](https://github.com/andrew-disario/pizza-database-and-dashboards/blob/main/pizza-quickdbd.txt). (optional)
<p align="center">
<img src="https://github.com/andrew-disario/pizza-database-and-dashboards/blob/main/pizza-quickdbd-layout.png?raw=true" height="80%" width="80%" alt="pizza-quickdbd-layout"/>
</br>

4. Select **Export** and choose **MySQL/MariaDB**.

<b>Build a Database in MySQL Workbench</b>

1. Open **MySQL Workbench**.
2. Run SQL query ```CREATE DATABASE pizza_db;```.
	- Select **Refresh** to see **pizza_db** in the Navigator pane
[pizza-db-refresh.png]
1. Select **Open a SQL script file in a new query tab**
2. Select **QuickDBD-pizza_db.sql** (or your file name).
3. Replace the commented section with ```USE pizza_db;```
4. Highlight the entire SQL query and select **Execute**
5. For each table, select **Table Data Import Wizard** to import .csv files. (Not provided)
6. select **Server** and choose **Data Export** to export a dump file.
7. Choose **pizza_db**, **Export to Self-Contained File** and select **Start Export**.

<h2>PART II - Build Interactive Dashboards</h2>

<b>Set Up Google Cloud Instance</b>
1. Go to [cloud.google.com](https://console.cloud.google.com/) and set up an account. (Limited free trial)
4. In the navigation pane, select **Cloud Storage** and choose **Buckets**.
5. Create a bucket, navigate to it, select **Upload Files** and choose the dump file created in Step 1.
6. In the navigation pane, select **SQL** and navigate to **Databases**.
7. Select **Create Database** and enter a name for the database (ie pizza_db).
8. In the navigation pane, select **Overview**, create an instance and in that instance select **Import**.
9. Under **Source** navigate to the dump file you uploaded, specify the database and select **Import**.

<b>Create a Data Source in Google Cloud Instance</b>

1. Go to [lookerstudio.google.com](https://lookerstudio.google.com/)
2. Select **Create** and choose **Data Source**.
	- Complete account setup if prompted.
3. Choose **Cloud SQL for MySQL** and select **Authorize**.
4. Provide Google Cloud instance information to set up database connection and select **Authenticate**.
5. Choose **Custom Query**, input SQL query and select **Connect**.
6. Look over data types and make any necessary changes.
7. Rename the data source. (Recommended)
8. Select **Create Report** or navigate to an existing report.

<b>Orders Dashboard</b>

Dashboard must show total orders, total sales, total items, average order value, sales by category, top selling items, orders by hour, sales by hour, orders by address and orders by delivery / pick up.
1. Use the SQL query in [orders_query.txt](https://github.com/andrew-disario/pizza-database-and-dashboards/blob/main/orders_query.txt) to create a data source.
2. Create a new report or create a new page in an existing report.
3. Use the data source you created to design and build you dashboard according to the prompt.
4. When finished, select **File**, **Download** and choose**PDF**.
<p align="center">
<img src="https://github.com/andrew-disario/pizza-database-and-dashboards/blob/main/orders-dashboard.png?raw=true" height="80%" width="80%" alt="orders-dashboard"/>
</br>

<b>Inventory & Items Dashboard</b>

We need to calculate how much inventory we're using and then identify inventory that needs reordering. We also want to calculate how much each pizza costs to make based on the cost of the ingredients so we can keep an eye on pricing and P/L. Dashboard must show total quantity by ingredient, total cost of ingredients, calculated cost of pizza and the percentage stock remaining by ingredient.
1. Use the SQL queries in [stock_query1.txt](https://github.com/andrew-disario/pizza-database-and-dashboards/blob/main/stock_query1.txt) and [stock_query2.txt](https://github.com/andrew-disario/pizza-database-and-dashboards/blob/main/stock_query2.txt) to create two data sources.
2. Create a new report or create a new page in an existing report.
3. Use the data sources you created to design and build a dashboard according to the prompt.
4. When finished, select **File**, **Download** and choose**PDF**.
<p align="center">
<img src="https://github.com/andrew-disario/pizza-database-and-dashboards/blob/main/inventory-items-dashboard.png?raw=true" height="80%" width="80%" alt="items-inventory-dashboard"/>
</br>
