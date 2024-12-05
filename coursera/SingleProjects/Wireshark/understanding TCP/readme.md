<h align="center"1>TCP/IP Protocol Fundamentals</h1>
<p>&emsp;In this project, I intend to show the fundamentals of the TCP/IP protocol using Wireshark. For a short review of the TCP/IP stack layers:</p>
<table align="center">
  <tr>
    <th>Application Layer</th>
    <th>HTTP | HTTPS | SSH | FTP | SMTP</th>
  </tr>
  <tr>
    <td>Transport Layer</td>
    <td>TCP | UDP</td>
  </tr>
  <tr>
    <td>Internet Layer</td>
    <td>IP address: IPv4 | IPv6</td>
  </tr>
  <tr>
    <td>Network Access Layer</td>
    <td>Ethernet | Wireless LAN | Physical</td>
  </tr>
</table>

<p>&emsp;For this example, I will be analyzing the traffic over eth0 when I visit the website 'www.cygwin.com'. After starting the packet capture and visiting the website, I quickly stopped Wireshark's capture and filtered by 'tcp.port == 80'. Port 80 is the default port used in HTTP requests, so using this filter I find the IP address of the website by looking at the destination IP during the Transport Layer Security (TLS) client hello phase.</p>
<img src="https://github.com/BradRoff/write-up/blob/f9188e8ac16d0220e24ffa92babf6c1d659a06df/coursera/SingleProjects/Wireshark/img/1.PNG">

<p>&emsp;Next, I filtered the traffic by the IP address of 'www.cygwin.com', using 'ip.addr == 8.43.85.97'. Looking at the following screenshot, we can go step by step through the TCP/IP process. In the first three lines, we see the well-known SYN, SYN-ACK, ACK handshake. Looking at the source and destination IPs, you can see that our host SYNs to Cygwin, which then SYN-ACKs the host. The host then ends the handshake with an ACK back to Cygwin. The client says hello, and the server acknowledges and says hello back. The server then sends its certificate, and the client exchanges its key as part of TLSv1.2. Finally, a new session is opened, and the two IPs start sharing data.</p>
<img src="https://github.com/BradRoff/write-up/blob/f9188e8ac16d0220e24ffa92babf6c1d659a06df/coursera/SingleProjects/Wireshark/img/2.PNG">

<p>&emsp;For another example, when using the IP address of 'duckduckgo.com', '52.149.246.39', the result is slightly different. We can see that DuckDuckGo uses TLSv3, which, unlike TLSv2, does not require two round trips to complete. As you can see, this output requires fewer ACK packets, and the cipher keys are exchanged along with the server and client hellos. This allows the applications to share data faster.</p>
<img src="https://github.com/BradRoff/write-up/blob/f9188e8ac16d0220e24ffa92babf6c1d659a06df/coursera/SingleProjects/Wireshark/img/3.PNG">
