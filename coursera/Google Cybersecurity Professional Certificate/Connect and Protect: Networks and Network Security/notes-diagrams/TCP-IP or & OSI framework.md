<h1 align = "center">Play It Safe: Manage Security Risks short Review</h1>
<h2 align = "center">
  In this section, we dive depper into network vulnerabilities and how to secure networks. 
</h2>
<p>&emsp;
  Two models are commonly used as frameworks for understanding network communication: the Transmission Control Protocol/Internet Protocol (TCP/IP) model and the Open Systems Interconnection (OSI) model. The TCP/IP model is more commonly used due to its simplicity and practical application in real-world networking. In contrast, the OSI model is used more for theoretical purposes and to understand networking concepts at a more granular level.
</p>
<h3 align = "center">The TCP model:</h3>
<table align= "center">
  <tr><th>Application Layer</th>           <th>HTTP | HHTPS | SSH | FTP | SMTP</th>      </tr>
  <tr><td>Transport Layer</td>   <td>TCP | UDP</td>       </tr>
  <tr><td>Internet Layer</td>        <td>Ip address: IPV4 | IPV6</td>       </tr>
  <tr><td>Network Access Layer</td>   <td>Ethernet | Wirless Lan</td></tr>
</table>

<ul>
  <li>
    The <b><u>Application Layer</u></b> is responsible for making network requests or responding to requests. It defines which internet services and applications the user may access. Protocols like HTTP in this layer directly define how data packets will interact with receiving devices.
  </li>
    <li>
    <b>u>Transport Layer</u></b> is responsible for sending data between two systems or networks by using protocols to control the flow of traffic. TCP and UDP are commonly used in this layer.

<ul> <li> The Transmission Control Protocol (TCP) is an internet communication protocol that allows two devices to form a connection and stream data. TCP contains the port of the packet's destination within the TCP header of a TCP/IP packet. </li> <li> The User Datagram Protocol (UDP) is a connectionless protocol that does not form a connection between devices before transferring data. UDP doesn't track the information it is sending to its destination, making it potentially less secure but much faster. It is commonly used in several instances where large amounts of data must be transferred quickly and don't need to be transferred in perfect condition, such as with video streaming. </li> </ul>
  </li>
    <li>
    The <b><u>Internet Layer</u></b> ensures the delivery of the packet to its destination host, often residing on a different network. This layer assigns the Internet Protocol (IP) address to each data packet to note its sender and destination. It also determines which protocol to use in delivering data packets to their destination host. An example is the Internet Control Message Protocol (ICMP), which shares error information and updates on data packets. This protocol is often used in troubleshooting network errors, such as packets being redirected to a different host.
  </li>
    <li>
    The <b><u>Network Access Layer</u></b> (also known as the Data-Link Layer) deals with the creation of data packets and their transmission across the network. This layer encompasses all physical aspects of your network, such as endpoints (laptops, phones, etc.), routers, and hubs. It also includes the Address Resolution Protocol (ARP), as it is needed to map IP addresses to MAC addresses for local network communication.
  </li>
 
</or>

<h3 align = "center">The OSI model:</h3>
<table align= "center">
  <tr><th>Application Layer</th>           <th>End user apps, HTTP | SSH | FTP </th>      </tr>
  <tr><th>Presentation Layer</th>           <th>Syntex layer, data encryption, decryption</th>      </tr>
  <tr><td>Session Layer</td>   <td>App Session Start up, corodination, termination</td>       </tr>
  <tr><td>Transport Layer</td>        <td>End-to-End Data transmission via TCP/IP</td>       </tr>
  <tr><td>Network Layer</td>        <td>Packet fowarding, routing, subnet use</td>       </tr>
  <tr><td>Data Link Layer</td>   <td>Node-to-Node data transfer, error corection</td></tr>
  <tr><td>Pysical Layer</td>   <td>Physical structures, cables, hubs</td></tr>
</table>
<p>&emsp;
 The <b><u>OSI</u></b> framewok is ordered in decreasing levels of layers showing their ranks of complexity from greatest to least. The OSI model itself is much more detailed then the TCP/IP model splitting the Application layer into three layers and the network access layer into two diffrent layers.
</p>
<ol reverse>
  <li>Layer 7: The <b><u>Application Layer</u></b> includes all processes that directly involve the user. This layer encompasses all networking protocols that software applications use to connect users to the internet. The central feature of the Application Layer is connecting the user to the internet. For example, when using an internet browser application, the application will initiate an HTTPS protocol to connect the user to the website. This layer also includes using a Domain Name System (DNS) to search for a website on a DNS server and connect directly to it.
  </li>
  <li>
    Layer 6: The <b><u>Presentation Layer</u></b> performs data translation and encryption for the network. This layer transforms data formats so that they can be understood by applications from the seventh layer (the Application Layer) on both sending and receiving systems. This ensures that the data is in a format that is readable by the user. The Presentation Layer can also handle encryption to secure the data, such as using Secure Sockets Layer (SSL) certificates or Transport Layer Security (TLS) certificates. These technologies encrypt data between web servers and browsers using HTTPS, also referred to as HTTP over SSL and HTTP over TLS, respectively.
  </li>
  <li>
    Layer 5: The <b><u>Session</u></b> Layer protocols maintain sessions while data is being transferred and terminate the session once complete. A session can be defined as a connection between two devices. When opened, it allows the devices to communicate with each other. The Session Layer is also responsible for activities directly related to a session, such as authorization and reconnection. Sessions include a request and response between applications. Functions in the Session Layer respond to service requests from processes in the Presentation Layer (Layer 6) and send service requests to the Transport Layer (Layer 4).
  </li>
  <li>
    Layer 4: The Transport Layer is responsible for delivering data between devices. This layer also controls the flow and speed of data by breaking down large data chunks into smaller segments, making them easier to transport. After breaking the data into smaller chunks for transport, they are then reassembled at their destination into their original form so they can be processed by the Session Layer (Layer 5). This layer is also where TCP and UDP are implemented.
  </li>
  <li>
    
  </li>
</ol>
<p>&emsp;
  
</p>
<p>&emsp;
</p>
<p>&emsp;
</p>
<p>&emsp;
</p>
<p>&emsp;
</p>
<p>&emsp;
</p>
