<h1 style = "center">Analyze network layer communication activity</h1>
<p>In this activity giving a example senerio in which multible clients can't reach the website www.yummyrecipesforme.com with the  error "destination port unavalible", using the anilised trafic log from TCP dump write up a incident report. TCP log: </b>
13:24:32.192571 IP 192.51.100.15.52444 > 203.0.113.2.domain: 35084+ A? yummyrecipesforme.com. (24)
13:24:36.098564 IP 203.0.113.2 > 192.51.100.15: ICMP 203.0.113.2 udp port 53 unreachable length 254
13:26:32.192571 IP 192.51.100.15.52444 > 203.0.113.2.domain: 35084+ A? yummyrecipesforme.com. (24)
13:27:15.934126 IP 203.0.113.2 > 192.51.100.15: ICMP 203.0.113.2 udp port 53 unreachable length 320
13:28:32.192571 IP 192.51.100.15.52444 > 203.0.113.2.domain: 35084+ A? yummyrecipes forme.com. (24)
13:28:50.022967 IP 203.0.113.2 > 192.51.100.15: ICMP 203.0.113.2 udp port 53 unreachable length 150
</p>
<h2 style = "center"> DNS and ICMP trafic log summary</h2>
<h2 style = "center">Incident Cause analysis</h2>
