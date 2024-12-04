<h1>Apply Filters to SQL Queries</h1>

<h3>Project Description</h3>
<p>&emsp;In this scenario, my organization is investigating various security issues to help keep the system more secure. We decided to investigate further into the data tables "employees" and "log_in_attempts" by using SQL queries. We will use and record the results of different filters on the data to find potential points for improvement in our security.</p>

<h3 align="center">Retrieving After-Hours Failed Login Attempts</h3>
<p>&emsp;A potential security incident has been discovered that occurred after business hours (after 18:00). To investigate this, we will query the "log_in_attempts" table by using the following code:</p>
<img align="center" src="https://github.com/BradRoff/write-up/blob/4e44001fbd1ee89744a40a9165ae1587719d4933/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/1.PNG">
<p>&emsp;The first part of this screenshot is my SQL query. This query selects all information from "log_in_attempts" where the login time is past 18:00 and the login attempt failed. Since success in the table is calculated by a boolean value, 1 is equal to true and 0 is equal to false. We find that there are 19 entries of failed login attempts performed after normal working hours (18:00).</p>

<h3>Retrieving Login Attempts on Specific Dates</h3>
<p>&emsp;Our team discovered a suspicious event that occurred on 2022-05-09. For security, our team decided to query the table for any login activity that occurred on this day or the day before.</p>
<img align="center" src="https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/2.PNG">
<img align="center" src="https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/3.PNG">
<p>&emsp;This query uses the WHERE and OR operators to find login events on either 2022-05-09 or 2022-05-08. The 75 rows in this table occurred on either 2022-05-09 or 2022-05-08.</p>

<h3 align="center">Retrieving Login Attempts Outside of Mexico</h3>
<p>&emsp;Upon further investigation of the suspicious login activity, our team decided that this activity didn't originate in Mexico. Our next course of action was to investigate the login attempts occurring outside of Mexico. To do this, we use a query with the NOT and LIKE operators to show any login attempts where the country of origin is NOT LIKE 'MEX%', where "%" is a wildcard. This is used because the table has entries for both "MEX" and "MEXICO" for Mexico. The result was that there were 144 login attempts from outside of Mexico.</p>
<img align="center" src="https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/4.PNG">
<img align="center" src="https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/5.PNG">

<h3 align="center">Retrieving Employees in Marketing</h3>
<p>&emsp;After our investigation, our team decided to deploy updates on specific machines in the marketing department. This would include any member of the marketing department within the East Office building. To discover who in the marketing department needs the update, we use a SQL query as follows:</p>
<img align="center" src="https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/6.PNG">
<img align="center" src="https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/7.PNG">
<p>&emsp;Looking at this query command, I am selecting all entries from "employees" where the department is equal to "marketing" and the office is like 'East%'. This will show entries for marketing employees from the East building, no matter what room number, because of the wildcard "%".</p>

<h3 align="center">Retrieve Employees in Finance or Sales</h3>
<p>&emsp;Our security team now needs to apply a different security update to employees in the Sales or Finance department. The following query selects all information from the "employees" table where the department column equals 'Sales' or the department column equals 'Finance'. This returns employees from both the Sales department and the Finance department.</p>
<img align="center" src="https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/8.PNG">

<h3 align="center">Retrieving All Employees Not in IT</h3>
<p>&emsp;Our security team also needs to apply a general update to the entire company. Upon further inspection, the Information Technology department has already received this update. We will use the WHERE and NOT operators to select all employees not in the IT department.</p>
<img align="center" src="https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/9.PNG">

<h3 align="center">Retrieve All Employees Not in IT</h3>
<p>&emsp;In this project, I applied SQL queries to get specific information on login attempts and employee machines, using the tables "log_in_attempts" and "employees". I used the AND, NOT, and OR operators to filter for more specific information while using the LIKE operator and wildcard "%" to search for patterns.</p>
