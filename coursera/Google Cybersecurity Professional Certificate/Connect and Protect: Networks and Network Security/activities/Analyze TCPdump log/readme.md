<h1 align="center">Analyze Network Layer Communication Activity</h1> 
<p>
  In this activity, I will provide an example scenario in which multiple clients can't reach the website <a>www.yummyrecipesforme.com</a> and encounter the error "destination port unavailable." Using the analyzed traffic log from a TCP dump, I will write up an incident report.
</p> 
<h2 align="center">DNS and ICMP Traffic Log Summary</h2> 
<p>
  
As part of the <b>Domain Name Server</b> (DNS) protocol, the DNS server tries to receive the Internet Protocol (IP) address from the domain name yummyrecipesforme.com. The User Datagram Protocol (UDP) packet is unsuccessful and instead receives an error message from the Internet Control Message Protocol (ICMP), indicating issues with the DNS server. This error response is shown on the fourth line stating "UDP port 53 unreachable." Port 53 is crucial for DNS communication, meaning there must be an issue with the DNS server. This can be further deduced from the flags included in the third line, "203.0.113.2.domain: 35084+ A?", where 35084 is the query identification number, and "A?" shows that DNS was attempting to request an A record to map the domain name to an IP address. 
</p>
<h2 align="center">Incident Cause Analysis</h2> 
<p>
  According to the timestamp "13:24:32.192571," this incident occurred at *:24 PM. The IT team became aware of the incident when customers reported being unable to access the website <a>www.yummyrecipesforme.com</a>, seeing the error message “destination port unreachable” after waiting for the page to load.
The cause of the incident is likely incorrect firewall configurations on the DNS server side, blocking traffic on port 53. It is also possible that a Denial of Service (DoS) attack has shut down the DNS server on port 53. Depending on whether the DNS server was shut down or attacked by malicious actors, the service may need to be temporarily shut down for repairs. The next step in this process should be to determine the condition of the DNS server itself.
</p>
