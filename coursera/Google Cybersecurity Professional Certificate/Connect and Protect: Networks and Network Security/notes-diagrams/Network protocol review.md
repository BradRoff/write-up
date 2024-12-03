<h1>Network Protocol review</h1>
<p>&emsp;Network protocols are sets of rules used by two or more devices on a netwrok to describe the order of delivery and the structure of the data. These networking protocols are often divided into three common catigories.
</p>
<ol>
  <li><b>Communication protocols</b> govern the exchange of information in network transmission. This includes methods to recover data lost in transit. some examples include:</li> 
    <ul>
      <li>Transmission Control Protocol (TCP) forms a connection between devices before allowing the transmission of data. Does this by the three way hand shake SYN, SYN-ACK, ACK.</li>
      <li>User Datagram Protocol (UDP) is a connectionless protical hat does not establish a connection between devices before a transmission. Less reliable but more efficent then TCP.</li>
      <li>Hypertext Transfer Protocol (HTTP) is a application  protical that comunicates with the client and website server via port 80.</li>
      <li>Domain Name System (DNS) is used to translate the name of a website to its respective IP adress.</li>
  </ul>
  <li><b>Management Protocols</b> are used for monitering and maniging the security on the network. This includes proticols for error reporting and network efficincy optomization.</li>
    <ul>
      <li>Simple Network Management Protocol (SNMP) is a netwrok protical used for monetring and managing devices on the network.</li>
      <li>Internet Control Message Protocol (ICMP) is a netwrok protical devices use to comunicate with eachother.</li>
  </ul>
  <li><b>Security Protocols</b> ensure that the data sent and receved across the network is unchanging. Some examples would include common encrypton proticals.</li>
    <ul>
  <li>Hypertext Transfer Protocol Secure (HTTPS)</li>
      <li>Secure File Transfer Protocol (SFTP)</li>
  </ul>
</ol>
</b>
<h3 align= "center">
  There are networking proticals that are inprotant to understand as you will likely be interacting with them daily. 
</h3>
<p>&emsp;
A common networking proticol used by routers is the <b>Network Address Translation</b> (NAT) protical from a consiquence of IPv4. As we have the posibility of running out of IPv4 addresses, this protical allows the router to assign private IP adresses to the conected endpoints. When a endpoint makes a request to the internet, the router will convert that adress into the router's real Public IP asigned by the ISP or <b>Internet Assigned Numbers Authority (IANA)</b> and send the requuest, once the response is recived it will convert it and send it back to the end point. Diffrences between the IPs:</p>
<table align = "center">
<tr><th>Private IP address</th><th>Public Ip address</th></tr>
  <tr><td><ul><li>Assigned by the router</li><li>Unique only within private network</li><li>No cost to use</li><li>Address ranges:</li>
    <ul><li>10.0.0.0-10.255.255.255</li><li>172.16.0.0-172.31.255.255</li><li>192.168.0.0-192.168.255.255</li></ul></ul></td>
  <td><ul><li>Assigned by ISP and IANA</li><li>Unique address in global internet</li><li>Costs to lease a public IP address</li><li>Assignable address ranges:</li>
  <ul><li>1.0.0.0-9.255.255.255</li><li>11.0.0.0-126.255.255.255</li><li>128.0.0.0-172.15.255.255</li><li>172.32.0.0-192.167.255.255</li><li>192.169.0.0-233.255.255.255</li></ul></ul></td></tr>
</table>
<p>&emsp;
  The <b>Dynamic Host Configuration Protocol (DHCP)</b> is a network management protocol that automatically assigns IP addresses and other network configuration parameters to devices on a network. This is done using a client-server model where a DHCP server manage a pool of IP configuration infromation which are dimanicly alocated to DHCP enabled clients. DHCP servers operate on UDP port 67 while DHCP clients operate on UDP port 68. This proccess typlicly involves four steps, commonly refered to as <b>DORA</b>:
  <ul>
    <li><b>D</b>iscover: Client broadcasts a request for an IP address</li>
    <li><b>O</b>ffer: Server responds with an available IP address and configuration</li>
    <li><b>R</b>equest: Client accepts the offer</li>
    <li><b>A</b>cknowledge: Server confirms the assignment</li>
  </ul>
</p>
<p>&emsp;
  The <b>Address Resolution Protocol (ARP)</b> operates between Layer 2 and Layer 3 of the OSI model, primarily used to map IP addresses to MAC addresses within a local area network (LAN). Wehn looking at the TCP/IP model, the ARP is mainly a network access layer protocol in the TCP/IP model used to translate the IP addresses that are found in data packets into the MAC address of the hardware device.
</p>
<p>&emsp;
  <b>Telnet</b> is an application layer proticol used to conect to a remote system. Simaler to SSH, but is often less secure and uses TCP port 23.
</p>
<p>&emsp;
  <b>Secure shell protocol (SSH)</b> is a commonly used protocol to create a secure connection to a remote sestem. This application layer protocol provides an alternative for secure authentication and encrypted communication. SSH operates over the TCP port 22 and is a replacement for less secure protocols, such as Telnet.
</p>
<p>&emsp;
  <b>Post office protocol (POP)</b> is a application layer protical used to send and recive email from a mail server. POP3 is the most commonly used form of POP. 
  <ul>
    <li>Unencrypted, plaintext authentication uses TCP/UDP port 110 </li>
    <li>encrypted emails use Secure Sockets Layer/Transport Layer Security (SSL/TLS) over TCP/UDP port 995</li>
  </ul>
</p>
<p>&emsp;
Simple Mail Transfer Protocol (SMTP) is used to transmit and route email from the sender to the recipient’s address. 
  <ul>
    <li>uses port 25 for unincrypted emails</li>
    <li>uses TCP/UDP port 587 using transport layer security (TLS) for encrypted emails</li>
  </ul>
</p>
<p>&emsp;
Ports themselves are assinged by the Internet Assigned Numbers Authority (IANA). Their are thousands of assigned ports that are individualy assigned to preform spacific tasks for our daily life.  The common ones disscused here were:</p>
<table align = "center">
<tr><th>DHCP</th><td>UDP port 67 (servers) </b>UDP port 68 (clients)</th></tr>
  <tr><td>ARP</td><td>none</td></tr>
   <tr><td>Telnet</td><td>TCP port 23</td></tr>
   <tr><td>SSH</td><td>TCP port 22</td></tr>
   <tr><td>POP3</td><td>TCP/UDP port 110 (unencrypted)

TCP/UDP port 995 (encrypted, SSL/TLS)</td></tr>
   <tr><td>IMAP</td><td>TCP port 143 (unencrypted) </b>TCP port 993 (encrypted, SSL/TLS)</td></tr>
   <tr><td>SMTP</td><td>TCP/UDP Port 25 (unencrypted)</td></tr>
   <tr><td>SMTPS</td><td>TCP/UDP port 587 (encrypted, TLS)</td></tr>
</table>
  
</table>
