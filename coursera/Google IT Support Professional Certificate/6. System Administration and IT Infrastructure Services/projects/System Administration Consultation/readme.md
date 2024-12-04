<h1>System Administration Consultation</h1>
<p>&esmp;
In this project I will be working on systems administration for three diffrent companies in three diffrent scenarios. For each scenario, I will present improvements to processes based on the company’s needs and current restrictions. Please click any dropdown for the scenario or my respective response.</p>
<details>
<h3><summary>Network Funtime Company</summary></h3>
<p>Network Funtime Company is a small company that builds open-source software. The company is made up software engineers, a few designers, one person in Human Resources (HR), and a small sales team. Altogether, there are 100 employees. They recently hired you as a system administrator to come in and become their IT department.<br>

When a new person is hired on, the HR person purchases a laptop for them to do their work. The HR representative is unfamiliar with what type of hardware is out there; if a new employee requests a laptop, the HR person will purchase the cheapest option for a laptop online. Because of this, almost everyone has a different laptop model. The company doesn’t have too much revenue to spend, so they don’t order laptops until someone gets hired at the company. This leads to a few days of wait time from when someone starts to when they can actually work on a laptop.<br>

The company doesn’t label their computers with anything, so if a computer is missing or stolen, there’s no way to audit it. There’s no inventory system to keep track of what’s currently in the fleet.<br>

Once a computer is purchased, the HR person hands it to the new employee to set up. Software engineers that use Linux have to find a USB drive and add their preferred distribution to the laptop. Anytime someone needs something from HR -- whether it’s office related or tech related -- they email the HR representative directly.<br>

When a new employee gets a machine, they’re given logins to use cloud services. They get a personal orientation with HR to make sure they can login. This requires the HR person to block off a few hours for every new employee. If an employee forgets the login to their machine, they have no way to retrieve a password and they have to reimagine their machine. Employees don’t have a strict password requirement to set for their computers.<br>

The company currently has many of their services in the cloud, such as email, word processors, spreadsheet applications, etc. They also use the application, Slack, for instant communication.<br>
</p>
</details>

<details><h3><summary>Improving NFC</summary></h3>
  <p>
Hardware Management Issues:<br>
Laptop purchases for new employees should be more standardized. For example, there should be three pre-approved laptop brands/models for users that will be sufficient for their respective roles. This will increase productivity, as issues that have occurred before can likely be fixed more easily if they happen on the same model. Depending on the expected employee size, this also allows the company to buy in bulk, receiving a sizable discount. When buying in bulk, it would be wise to purchase spare hardware in case a user's laptop breaks or a new hire needs a laptop, avoiding several days of waiting. These computers can be preinstalled with the required software and BIOS for the employees' needs. The company also needs an accurate hardware inventory that contains information on each computer. This inventory can include the purchase date, an assigned ID number, model, and the ID of the assigned employee. This will greatly reduce potential theft, as each employee will be responsible for an assigned computer. It will also improve overall security management and auditing.<br>

Software and Security:<br>
To reduce an employee's setup time, create standardized OS images as needed for Windows or Linux systems that can be deployed via network boot or implemented using a USB drive. There should also be a password policy as well as a password management system. This will help prevent guessed passwords and brute-force attacks on the system. Through the password management system, IT can recover forgotten passwords or assign a temporary password to be changed at the next login. Depending on the type of data an employee is expected to handle, it would be wise to implement two-factor authentication via biometrics or a key, adding another protective layer to our data.<br>

IT Support and Communication Issues:<br>
It would be wise to implement an IT ticketing system, such as FreshService or osTicket, depending on the needs of the company. This will streamline support, reduce the need to contact HR, decrease required response times, and allow for more efficient tracking of related IT issues. It would also be beneficial to create a portal or manual for common issues that appear and how they can be fixed, to reduce the overall workload on IT staff for easily solvable problems. Onboarding can also be automated using different applications to set up user accounts.<br>

Lacking Security Testing:<br>
The company needs to implement regularly scheduled security tests on their system. This could help identify potential vulnerabilities before they are exploited. Employees should also receive regular training on common IT principles, such as identifying scam emails.<br>

If these examples are implemented NFC can greatly inprove it's IT infrastructure, enhance data security, and reduce the potential workload on the IT department.
</details>
