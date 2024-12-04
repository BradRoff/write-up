<h1>Apply flters to SQL queries</h1>

<h3>Project description<h3></
In this scenario, my orginizaton is investigating various seccurity issues to help keep the system more secure. We decide to investigate further into the data table employees and log_in_attempts by using SQL queries. We will use and record the results of diffrent filters on the data to find potential points for inprovment in our security.

<h3>Retriving after hours failed login attempts</h3>
<p>&esmp;A potential security incident has been discoverd that had occurred after business hours (after 18:00). To investigate this, we will query log_in_attempts by using the following code:</p>
<img src = 'https://github.com/BradRoff/write-up/blob/4e44001fbd1ee89744a40a9165ae1587719d4933/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/1.PNG'>
<p>
  The first part of this screen shot is my SQL querry. This querry sellects all infromation from log_in_attempts where the login time is past 18:00  and failed. As success in the table is calculated by a bulian value, 1 is equal to truth and 0 is equal to false. We find that their are 19 entries of faild log in attempts preformed after normal work hours (18:00).
</p>
<h3>Retrieveing login aempts on specic dates</h3>
Our team discovered a suspicus event has occured on 2022-05-09. For security our team decided to querry the table for any login activity that occured this day or the day before.
<img src =https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/2.PNG>
<img src =https://github.com/BradRoff/write-up/blob/main/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/Apply%20filters%20to%20SQL%20queries/img/3.PNG>

[Add content here.]
Retrieve login a

empts outside of Mexico

[Add content here.]
Retrieve employees in Marketing
[Add content here.]
Retrieve employees in Finance or Sales
[Add content here.]
Retrieve all employees not in IT
[Add content here.]
Summary
[Add content here.]
