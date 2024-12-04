<h1>Apply flters to SQL queries</h1>

<h3>Project description<h3></
In this scenario, my orginizaton is investigating various seccurity issues to help keep the system more secure. We decide to investigate further into the data table employees and log_in_attempts by using SQL queries. We will use and record the results of diffrent filters on the data to find potential points for inprovment in our security.

<h3 align = "center">Retriving after hours failed login attempts</h3>
<p>&esmp;
  A potential security incident has been discoverd that had occurred after business hours (after 18:00). To investigate this, we will query log_in_attempts by using the following code:</p>
<img  align = "center" src = 'https://github.com/BradRoff/write-up/blob/4e44001fbd1ee89744a40a9165ae1587719d4933/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/1.PNG'>
<p>&esmp;
  The first part of this screen shot is my SQL querry. This querry sellects all infromation from log_in_attempts where the login time is past 18:00  and failed. As success in the table is calculated by a bulian value, 1 is equal to truth and 0 is equal to false. We find that their are 19 entries of faild log in attempts preformed after normal work hours (18:00).
</p>
<h3>Retrieveing login aempts on specic dates</h3>
Our team discovered a suspicus event has occured on 2022-05-09. For security our team decided to querry the table for any login activity that occured this day or the day before. 
<img  align = "center" src =https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/2.PNG>
<img align = "center" src =https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/3.PNG>
<p>&esmp;This query uses the WHERE and OR opperater to find login events on either 2022-05-09 or 2022-05-09. The 75 rows in this table occured on either 2022-05-09 or 2022-05-09.
</p>
<h3 align = "center">Retrieving login aempts outside of Mexico</h3>
<p>&esmp;Upon further investigation on the suspisus login activity, our team decided that this activity didn't originate in Mexico. Our next course of action is to investigate the login attempts occuring outside of Mexico. To do this we use a query with the NOT and LIKE operater to show any loggin attempts that county of origin are NOT LIKE 'MEX%', where % is a wildcard. This is used becuase the table has entrees of MEX and MEXICO for Mexico. The result was that there were 144 login attempts from outside of Mexico.</p>
<img align = "center" src =https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/4.PNG>
<img align = "center" src =https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/5.PNG>

<h3 align = "center">Retrieving employees in Marketing</h3>
<p>&esmp;
After our investigation, our team decided to deploy updates on spacific machines in the markiting department. This would include any member of the marking department within the East Office building. To discover who in the markiting department needs the update, we use a SQL querey as follows:
  </p>
  <img align = "center" src =https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/6.PNG>
  <img align = "center" src =https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/67.PNG>
  <p>&esmp;
    Looking at this querry command I am sellecting all from employees where department is equal to markiting and office is like 'East%'. This will show entries that only contains markiting employies from the East building, nomater what room nuber because of the wildcard '%'.
</p>
<h3 align = "center">Retrieve employees in Finance or Sales</h3>
<p>&esmp;
  Our security team now needs to apply a diffrent security update on employees in the Sales or Finance department. The following query selects all infromation from the employees table where the department collom equals 'Sales' or the department table = 'Finance'. This returns both employees from only the Sales department and employees from the Finance department.
</p>
<img align = "center" src =https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/8.PNG>
<h3 align = "center">Retriving all employees not in IT</h3>
<p>&esmp;
  Our security team also needs to apply a general update to the entire company. Upon further inspection, the Information Technology department has already recived this update. We will use the Where and NOT operation ti select all employees not in the IT dedpartment.  
</p>
<img align = "center" src =https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/9.PNG>
<h3 align = "center">Retrieve all employees not in IT</h3>
<p>&esmp;
  In this project I applied SQL queries to get specific infromation on login attemps and employee machines, using the tables log_in_attempts and employees. I used the AND, NOT, and OR operators to filter out for more specific information while using the LIKE and wildcard % to search for patterns.
</p>
