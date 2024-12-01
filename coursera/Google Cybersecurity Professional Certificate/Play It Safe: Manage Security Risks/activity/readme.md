<h2 align= "center">Use the NIST Cybersecurity Framework to respond to a security incident:</h2>
<p>
  &emsp; In this activity I created a incident report for an example cyber security reesponse scenario using the NIST format. 
</p>

| Step        | Analysis           | 
| :-------------: |:-------------| 
| Incident Summary      | The company experienced a flood of Internet Control Message Protocol (ICMP) packets, which compromised the internal network for two hours. The cyber team found that this was caused by an attacker overwhelming the network with a distributed denial of service (DDoS) attack, and in response, blocked all non-critical network services. They have implemented several improvements, such as a new firewall rule to counter the ICMP attacks, source IP verification, network monitoring software, and an IDS/IPS system to filter out some ICMP traffic based on suspicious characteristics. | 
| Identify      | The attacker used a DDoS attack to take down the company's entire internal network system. Currently, the company's internal network system is functional. However, the network should be checked for any further vulnerabilities and ensure that it is up to date. | 
| Protect      |    In this case, the cybersecurity team implemented a new firewall rule to limit the rate of incoming ICMP packets and An IDS/IPS system to filter out some ICMP traffic based on suspicious characteristics. These rules should be reguarly updated.   | 
| Detect |    The cybersecurity team implemented source IP address verification on the firewall to check for spoofed IP addresses on incoming ICMP packets and monitoring software to detect abnormal traffic patterns.| 
| Respond      | For future DDOS events, the cybersecurity team should isolate the affected system from the network to prevent further harm. After restoring any critical affected systems, they should moniter the network logs for any suspicious activity and update firewall polocies and IDS/IPS polocies as needed. These steps should also be recorded and reported to their supirors or athorities depending on the sevarity. | 
| Recover      |   To recover from a DDoS attack from ICMP flooding, the company's network services must be restored to a normal functioning state. Depending on the situation, there may be several further steps. It is common for internet service providers (ISPs) to block networks under DDoS attacks, so you may need to contact your ISP to reconnect. Depending on your organization's size, you should have a plan for reintroducing your clients, because if all your clients try to download applications at once when you return, you may receive an unintended application layer DDoS attack. Your network Border Gateway Protocol (BGP) connections should also be securely reestablished if disconnected. Your company should also have a plan for the order in which applications should be restored, so you don't cause a sudden potential surge in traffic.| 



