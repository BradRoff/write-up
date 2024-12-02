<h1 align = "center">Apply OS hardening techniques</br></h1>
<h2 align = "center">Security Incedent Report</h2>

   <p align="center"> <b>Section 1:</b> Identify the network protocol involved in the incident </br></p>

  <p>
  &emsp;The network protocol involved with this brute force attack was the Hypertext Transfer Protocol (HTTP), as the issue involves the web server for yummyrecipesforme.com. In the process of using tcpdump, when the browser initiates an HTTP request for the yummyrecipesforme.com webpage using the IP address sent by the DNS server, the browser then downloads the malware and initiates a DNS request for greatrecipesforme.com. The malicious file is shown to be transported ussing the HTTP protical along the aplication layer.
 </p>

 
   <p align="center"><b>Section 2:</b> Document the incident </br></p>
   <p> &emsp;
      Within this incident, several customers complained that the company’s website had prompted them to download a file to access free recipes. Once this file was run, it would change the title of the webpage and slow down the speed of their personal computers, which infected their systems with malware. In response, the owner tried to log into their admin panel but was unable to, being forced to contact their provider. The attacker likely changed the admin access credentials when they brute-forced the site.

The investigation was held in a sandbox environment, where the same steps the clients reported were performed, along with tcpdump. As described, downloading the prompted file and allowing it to run redirects to greatrecipesforme.com, which contains malware.

When analyzing the logs provided by tcpdump, the logs show that after initializing an HTTP request to yummyrecipesforme.com using the IP address from the server, the browser initiates the download of the malware. This then immediately changes the web traffic to greatrecipesforme.com, rerouting the user.
</p>
<p>&emsp;
The analyst then analyzed the source code of greatrecipesforme.com. Within this compromised code was added JavaScript that would prompt the user to download a file. Looking into the code of the downloaded file shows that it's a script that redirects the visitors’ browsers from yummyrecipesforme.com to greatrecipesforme.com, infecting them with malware. As the owner reported that they used the default password, it was the result of a brute-force attack.
</p>
<p align="center"><b>Section 3:</b> Recommend remediation for brute force attacks</p>
<p>&emsp;
The security team reinforces that the strongest defense against a brute force attack is to have a secure password policy. Passwords should be complex and never set to default. Some good practices include using a longer password with a mixture of characters. The password should also be changed semi-regularly. Another way to greatly increase security is by enabling two-factor authentication. This would mean having your password along with something you have, know, or are. For example, having to use a security key, the name of your first pet, or a fingerprint scanner can help improve overall security.
</p>


    
 

