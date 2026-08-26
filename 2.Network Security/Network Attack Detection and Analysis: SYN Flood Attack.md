# Case Study
This case study focuses on the detection and analysis of a Denial-of-Service (DoS) attack, specifically a TCP SYN Flood attack, affecting a travel agency's web server.

The incident was identified after an automated monitoring alert indicated that the web server was experiencing abnormal network activity. When employees attempted to access the company website, they received a connection timeout.

Network traffic analysis revealed an unusually large number of TCP SYN requests originating from an unfamiliar IP address. The high volume of connection requests caused the web server to consume its available resources while waiting for connection confirmations, preventing legitimate users from establishing new connections.

The investigation uses network traffic monitoring to identify the attack pattern, understand how the TCP connection process was affected, and determine the impact on the web server and legitimate users.

# Objective

The objectives of this case study are to:

* Identify the type of network attack affecting the web server.
* Analyze abnormal TCP SYN traffic associated with the incident.
* Understand how a SYN Flood attack affects the TCP connection process.
* Analyze the impact of excessive connection requests on server resources.
* Identify how the attack affects legitimate website users and employees.
* Support incident response and mitigation activities.
* Develop appropriate recommendations to reduce the risk of similar attacks in the future.

## TCP Three-Way Handshake

TCP uses a three-way handshake to establish a connection between a client and a server.

Step	TCP Flag	Description
1	SYN	The client sends a SYN packet to the server to request a TCP connection.
2	SYN/ACK	The server responds with a SYN/ACK packet, acknowledging the request and indicating that it is ready to establish the connection.
3	ACK	The client sends an ACK packet to confirm the connection. The TCP connection is then established.

The normal communication flow is:

Client → SYN → Server
Client ← SYN/ACK ← Server
Client → ACK → Server

After the three-way handshake is completed, the client and server can exchange application data.

# Recommended Mitigation

To reduce the risk of similar attacks, the following measures can be considered:

* Implement network-level DoS/DDoS protection.
* Configure firewall rules to detect and mitigate abnormal SYN traffic.
* Apply appropriate connection rate limiting.
* Monitor abnormal increases in TCP SYN requests.
* Use IDS/IPS capabilities to detect network attack patterns.
* Establish automated alerting for abnormal traffic spikes.
* Consider upstream DDoS protection to filter malicious traffic before it reaches the web server.
* Continuously monitor network traffic and server resource utilization.

# Conclusion

The network interruption was caused by an abnormal volume of TCP SYN requests, indicating a potential SYN Flood attack, a form of Denial-of-Service attack.

The attack overwhelms the web server with a large number of connection requests and causes excessive consumption of connection resources. As a result, the server becomes unable to process legitimate connection attempts, causing employees and website visitors to experience connection timeout errors.

The incident demonstrates the importance of network traffic monitoring, protocol analysis, and timely incident response. While blocking the identified source IP can provide temporary containment, additional controls such as rate limiting, IDS/IPS, and DoS/DDoS protection should be implemented to provide stronger and more sustainable protection against similar attacks.
