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
A common networking proticol used by routers is the <b>Network Address Translation</b> (NAT) protical from a consiquence of IPv4. As we have the posibility of running out of IPv4 addresses, this protical allows the router to assign private IP adresses to the conected endpoints. When a endpoint makes a request to the internet, the router will convert that adress into the router's real Public IP asigned by the internet and send the requuest, once the response is recived it will convert it and send it back to the end point. Diffrences between the IPs:</p>
<table align = "center">
<tr><th>Private IP address</th><th>Public Ip address</th></tr>
  <tr><td><ul><li>Assigned by the router</li><li>Unique only within private network</li><li>No cost to use</li><li>Address ranges:</li>
    <ul><li>10.0.0.0-10.255.255.255</li><li>172.16.0.0-172.31.255.255</li><li>192.168.0.0-192.168.255.255</li></ul></ul></td>
  <td><ul><li>Assigned by ISP and IANA</li><li>Unique address in global internet</li><li>Costs to lease a public IP address</li><li>Assignable address ranges:</li>
  <ul><li>1.0.0.0-9.255.255.255</li><li>11.0.0.0-126.255.255.255</li><li>128.0.0.0-172.15.255.255</li><li>172.32.0.0-192.167.255.255</li><li>192.169.0.0-233.255.255.255</li></ul></ul></td></tr>
</table>
