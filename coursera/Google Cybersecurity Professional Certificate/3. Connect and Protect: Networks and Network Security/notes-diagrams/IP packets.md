<h1 align = "center">Contents of a IPV4 and IPV6 packet</h1>
<p>&emsp;
One of the most important functions of the network protocol is to form packets of data to be sent over the network. All data packets contain a destination IP within their header. A data packet is refferd to as an IP packet in TCP connections or a datagram for UDP connections. The most common packet formations used today are IPv4 and IPv6. Their are several diffrences between an IPV4 and IPV6 data packet. The header of a IPV4 packet can be 20-60 bytes while a IPV6 is fixed at 40 bytes. The fields contained within each data packet also differ. In this activity, I'm going to go over the structure and components of each packet.
</p>

<h2 align="center">IPV4 Packet</h2>
<table align= "center"  >
  <tr ><td colspan = "2" align="center"> <---------20 - 65,535 or 2^16 bytes ---------></td></tr>
  <tr><td colspan = "1"> <--20-60 bytes --></td></tr>
  <tr ><td >Header</td><td width = "300px" >Data</td></tr>
</table>

<h2 align="center">IPV4 Packet Header Contents</h2>
<p align="center">
<img  src = "https://imgs.search.brave.com/shQuGTnETGn-LzECs5kBfFvGd0Bwy4CMARAUWa24GYo/rs:fit:500:0:0:0/g:ce/aHR0cHM6Ly93d3cu/aXB4by5jb20vYXBw/L3VwbG9hZHMvMjAy/Mi8wOC9JUHY0LXBh/Y2tldC1oZWFkZXIu/cG5n">
</p>
<h3 align="center">IPV4 Packet Header Fields</h2>
<ul>
  <li><b>Version (VER):</b> This component tells the system what version of IPv is being used (4 bits).</li>
  <li><b>IP Header Length (HELD or IHL):</b> IHL is the packet header length, as the name suggests. This value indicates where the packet header ends and the data of the packet begins (4 bits).</li>
  <li><b>Type of Service (ToS):</b> An 8-bit field that specifies how a particular upper-level protocol would like the datagram to be handled. This allows the upper-level protocol to determine traffic based on the packet's priority.</li>
  <li><b>Total Length:</b> This field communicates the total length of the entire IP packet, including the header and data. The maximum size of an IPv4 packet is 65,535 bytes.</li>
  <li><b>Identification:</b> Most packets are divided or fragmented into smaller IP packets to move quickly through the network. The Identification field provides a unique identifier to each packet so they can be reassembled to their original form at the destination.</li>
  <li><b>Flags:</b> Provides the routing device with additional information, including whether there are more fragments of the original fragmented packet in transit.</li>
  <li><b>Fragmentation Offset:</b> Tells the routing device where the original packet belongs.</li>
  <li><b>Time to Live (TTL):</b> Prevents packets from being forwarded by routers indefinitely. This contains a counter that decreases with each hop, and if it reaches zero, the router will discard the packet and return an ICMP time-exceeded error.</li>
  <li><b>Protocol:</b> Tells the device which protocol will be used for the data section of the packet.</li>
  <li><b>Header Checksum:</b> Contains a checksum value that can be used to check for any potential corruption of the IP header in the packet. If corruption is detected, the packet is discarded.</li>
  <li><b>Source IP Address:</b> The source IP address of the sending device.</li>
  <li><b>Destination IP Address:</b> The destination IP address is the IPv4 address of the destination device.</li>
  <li><b>Options:</b> Allows for security options if the IHL value is greater than five. These options are then communicated to the routing devices.</li>
</ul>
<p>&emsp;
  As the internet rapidly grew, we began to face the inpending possibility of running out of IPv4 addresses. To solve this issue, IPv6 was developed which has 340 undecillion addresses compared to IPv4s 4.3 billion. This also increaes security and provides more efficent routing as it avoids IPv4 collision from devices colliding by attemting to use the same IP address on the same network. 
</p>
<h2 align = "center">IPV6 header</h2>

<table align= "center" >
  <tr><td>Version</td><td>Trafic class</td><td colspan = "2" align= "center">Flow Label</td></tr>
  <tr><td colspan = "2" align= "center">Payload length<td>Next Header</td><td>Hop Limit</td></tr>
  <tr > <td colspan = "4" align= "center">Source address </td></tr>
  <tr> <td colspan = "4" width = "300px" align= "center">Destination address </td></tr>
</table>

<h3 align="center">IPV4 Packet Header Fields</h2>
<li><b>Traffic Class</b>: Same as Type of Service (IPv4), position and name changed. Used for traffic classification and marking.</li>
<li><b>Flow Label:</b> 20-bit field for labeling packets in the same sequence</li>
<li><b>Payload Length</b>: Unlike IPv4, position and name changed. IPv6 only includes data length</li>
<li><b>Hop Limit (IPv6):</b> same as Time to Live (IPv4), position and name changed. Both prevent infinite packet loops</li>
<li><b>Next Header:</b>same as Protocol (IPv4)  position and name changed. Indicates the payload protocol or extension header.</li>


