<h1>System Administration Consultation</h1>
<p>&esmp;
In this project I will be working on systems administration for three diffrent companies in three diffrent scenarios. For each scenario, I will present improvements to processes based on the company’s needs and current restrictions. Please click any dropdown for the scenario or my respective response.</p>
<details><summary>Network Funtime Company, Software Company</summary>
<p>Network Funtime Company is a small company that builds open-source software. The company is made up software engineers, a few designers, one person in Human Resources (HR), and a small sales team. Altogether, there are 100 employees. They recently hired you as a system administrator to come in and become their IT department.<br>

When a new person is hired on, the HR person purchases a laptop for them to do their work. The HR representative is unfamiliar with what type of hardware is out there; if a new employee requests a laptop, the HR person will purchase the cheapest option for a laptop online. Because of this, almost everyone has a different laptop model. The company doesn’t have too much revenue to spend, so they don’t order laptops until someone gets hired at the company. This leads to a few days of wait time from when someone starts to when they can actually work on a laptop.<br>

The company doesn’t label their computers with anything, so if a computer is missing or stolen, there’s no way to audit it. There’s no inventory system to keep track of what’s currently in the fleet.<br>

Once a computer is purchased, the HR person hands it to the new employee to set up. Software engineers that use Linux have to find a USB drive and add their preferred distribution to the laptop. Anytime someone needs something from HR -- whether it’s office related or tech related -- they email the HR representative directly.<br>

When a new employee gets a machine, they’re given logins to use cloud services. They get a personal orientation with HR to make sure they can login. This requires the HR person to block off a few hours for every new employee. If an employee forgets the login to their machine, they have no way to retrieve a password and they have to reimagine their machine. Employees don’t have a strict password requirement to set for their computers.<br>

The company currently has many of their services in the cloud, such as email, word processors, spreadsheet applications, etc. They also use the application, Slack, for instant communication.<br>
</p>
</details>

<details><summary>Improving NFC</summary>
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
<br>
<details>
  <summary>W.D. Widgets, Sales Company</summary>
  W.D. Widgets is a small company that sells widgets. They’re mostly made up of salespeople who work with lots of clients. You’ve taken over as the sole IT person for this company of 80-100 people.<br>

When HR tells you to provision a machine for a new employee, you order the hardware directly from a business vendor. You keep one or two machines in stock, in case of emergency. The users receive a username that you generate for them. You then give them an orientation on how to login when they start. You currently manage all of your machines using Windows Active Directory. The company uses only Windows computers. When a new computer is provisioned, you have to install lots of sales-specific applications manually onto every machine. This takes a few hours of your time for each machine. When someone has an IT-related request, they email you directly to help them.<br>

Almost all software is kept in-house, meaning that you’re responsible for the email server, local machine software, and instant messenger. None of the company’s services are kept on the cloud.<br>

Customer data is stored on a single file server. When a new salesperson starts, you also map this file server onto their local machine, so that they can access it like a directory. Whoever creates a folder on this server owns that folder and everything in it. There are no backups to this critical customer data. If a user deletes something, it may be lost for everyone.<br>

The company generates a lot of revenue and is rapidly growing. They’re expecting to hire hundreds of new employees in the next year or so, and you may not be able to scale your operations at the pace you’re working.<br>


</details>
<details>
  <summary>Inproving W.D. Widgets</summary>
  There are several things that W.D. Widgets can implement to increase their security and productivity.<br>

Provision of laptops can be automated to reduce the time needed to set up each machine. This can be accomplished by creating several machine images with the software an employee needs, using tools like the Microsoft Deployment Toolkit. The company should also look into creating a cloud-based backup system for their data. This will help prevent data loss and increase the speed of recovery. Services such as email should be moved to a cloud service to reduce on-premises infrastructure and allow for easier scaling as the company rapidly grows.<br>

The file server also needs better access controls to prevent loss or unauthorized access. Using a file management system, you can edit an employee's permissions to only what is necessary for their position. There is no reason someone in sales should be able to access data meant for IT or all customer data, especially passwords.<br>

As the company is growing rapidly, it would be wise to establish connections with trusted vendors for discounts on bulk machine purchases, and the number of backup machines may need to scale with the number of employees hired.<br>

In this description, there was no detailed data recovery plan in case of an emergency, whether it be software-related or an environmental disaster. A plan should be implemented for such disasters.<br>

Multi-factor authentication should also be implemented for employees to help protect sensitive customer data. Common patches should be automated and tested, preferably implemented during non-business hours or weekends. This can be done using several tools like the Windows Server Update Services. A backup should also be secured in case an update introduces an unexpected issue.<br>
</details>

<br>
<details>
  <summary>Dewgood, Non-profit Company</summary>
  Dewgood is a small, local non-profit company of 50 employees. They hired you as the sole IT person in the company. The HR person tells you when they need a new computer for an employee. Currently, computers are purchased directly in a physical store on the day that an employee is hired. This is due to budget reasons, as they can’t keep extra stock in the store.<br>

The company has a single server with multiple services on it, a file server, and email. They don’t currently have a messaging system in place. When a new employee is hired, you have to do an orientation with them for login. You’re also responsible for installing all the software they need on their machine, and mapping the file server to their computer. The computers are managed through Windows Active Directory. When an employee leaves, they’re currently not disabled in the directory service.<br>

The company uses an open-source ticketing system to handle all internal requests as well as external non-profit requests. But the ticketing system is confusing and difficult to use, so lots of the employees reach out to you directly to figure out how to do things. In fact, so many things are difficult to find that employees typically ask around when they have a question.<br>

There are nightly backups in place of the file server. You store this information on a disk backup and take it home with you everyday to keep it safe in case something happens onsite. There’s also a small company website that’s hosted on the single server at the company. This website is a single html page that explains the mission of the company and provides contact information. The website has gone down many times, and no one knows what to do when it happens.<br>
</details>
<details>
  <summary>Improving Dewgood</summary>
  There are several procedures that can be implemented to increase Dewgood's security and efficiency. While the company is low on funds, it may save costs in the long run to establish a bulk purchase of hardware for a discount from a supplier. This will also standardize the employees' hardware, allowing for easier auditing. It would be wise to keep a few extra pieces of hardware for easier onboarding and in case a computer breaks.<br>

The servers can be migrated to a cloud service such as Google Workspace to increase reliability and reduce potential stress on the singular server. This can also allow for an automated backup system to improve overall security and data recovery.<br>

The ticketing system needs to be updated or replaced with a less confusing system. If employees don't understand how to use the system, it is a waste of company time and money to maintain.<br>

When an employee leaves the company, their account must be disabled or revoked. Keeping it enabled after an employee's departure leads to a serious but easily avoidable security risk from a hacker or an upset employee.<br>

A website should also be implemented for employees to see common IT issues and how they can be fixed. For the company’s HTML page, there should be several IP addresses for the site. This could include a hot page that is ready for deployment in case of an issue with the original and a cold page that includes only the bare essentials for the page.<br>
</details>
