<h1 align="center">Analyze Network Attacks</h1>
<p>&emsp;In this activity, I will provide an incident report for a given scenario. In this report, I will explain what type of attack occurred and how it caused the site to malfunction.</p>

<h3 align="center">What Was the Attack?</h3>
<p>&emsp;In this scenario, the cause of the error was likely due to a Denial of Service (DoS) attack, specifically a SYN flood. The server stops responding after an overwhelming amount of Transport Control Protocol (TCP) SYN packets flood the server. The issue is temporarily alleviated after configuring the firewall to block the IP address the packets were coming from. Since the attack originated from a single IP, this is not considered a DDoS attack. However, this solution won't last long, as the attacker can easily change their IP once they realize they are being blocked.</p>

<h3 align="center">How Is This Attack Impacting the Site?</h3>
<p>&emsp;When a website user tries to establish a connection with the server, they perform a TCP three-way handshake. As the name implies, this handshake consists of three steps, often referred to as SYN, SYN-ACK, and ACK.</p>

<ol>
  <li><b>SYN</b>: A SYN packet is sent from the source (client) to the destination (server), requesting to connect.</li>   
  <li><b>SYN-ACK</b>: The destination responds to the source with a SYN-ACK packet to accept the request. The destination will then reserve the necessary resources for the source to connect.</li>   
  <li><b>ACK</b>: A final ACK packet is sent from the source to the destination, acknowledging permission to connect.</li>
</ol>

<p>&emsp;In a SYN flood attack, the attacker overwhelms the server with SYN packets, consuming all its resources. This prevents the server from reserving resources for legitimate connections, making it impossible for normal clients to connect. As a result, the web server loses its ability to respond to the abnormally large number of SYN requests.</p>

<p>&emsp;The solution to DDoS attacks is typically stronger, better-configured firewalls.</p>
