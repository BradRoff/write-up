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
<table align= "center"  >
  <tr ><td  align="center">VER 4 bits</td ><td  align="center">Service 8 bits</td><td  align="center"> VER 4 bits</td><td  align="center" colspan = "2" >Total Length: 16 bits</td><td  align="center"> Option Feilds 20 bits</td></tr>
  <tr><td colspan = "2" align="center">Identification 16 bits</td>><td  align="center"> Flags 3 bits</td>><td  align="center"> Fragmentation Offset 4 bits</td></tr>
   <tr><td colspan = "1.5" align="center">Time to live 8 bits</td><td colspan = "1.5" align="center">Protocol 8 bits</td><td colspan = "2" align="center">Header Checksum 16 bits</td></tr>
  <tr ><td >Header</td><td width = "300px" >Data</td></tr>
</table>
<h3 align = "center">Packet Feilds</h3>
