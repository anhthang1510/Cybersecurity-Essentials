# Quiz - Firewall Concepts

## Question 1
**Which statement is a characteristic of a packet filtering firewall?**

- They have a high impact on network performance.
- **They are susceptible to IP spoofing.**
- They examine each packet in the context of the state of a connection.
- They filter fragmented packets.

**Answer:** They are susceptible to IP spoofing.

---

## Question 2
**What is one benefit of using a next-generation firewall rather than a stateful firewall?**

- support of TCP-based packet filtering
- **integrated use of an intrusion prevention system (IPS)**
- support of logging
- reactive protection against Internet threats

**Answer:** integrated use of an intrusion prevention system (IPS)

---

## Question 3
**What are two characteristics of an application gateway firewall? (Choose two.)**

- **Performs most filtering and firewall control in software.**
- Uses connection information maintained in a state table and analyzes traffic at OSI Layers 3, 4, and 5.
- Uses a simple policy table look-up to filter traffic based on Layer 3 and Layer 4 information.
- **Analyzes traffic at Layers 3, 4, 5 and 7 of the OSI model.**
- Provides an integrated intrusion prevention and detection feature.

**Answers:**
- Performs most filtering and firewall control in software.
- Analyzes traffic at Layers 3, 4, 5 and 7 of the OSI model.

---

## Question 4
**What are two benefits of implementing a firewall in a network? (Choose two.)**

- A firewall will provide accessibility of applications and sensitive resources to external untrusted users.
- A firewall will inspect network traffic and forward traffic based solely on the Layer 2 Ethernet MAC address.
- **A firewall will sanitize protocol flow.**
- **A firewall will reduce security management complexity.**
- A firewall will prevent unauthorized traffic from being tunneled or hidden as legitimate traffic through an enterprise network.

**Answers:**
- A firewall will sanitize protocol flow.
- A firewall will reduce security management complexity.

---

## Question 5
**Which type of firewall is commonly part of a router firewall and allows or blocks traffic based on Layer 3 or 4 information?**

- **packet filtering firewall**
- next generation firewall
- proxy firewall
- stateful firewall

**Answer:** packet filtering firewall

---

## Question 6
**Which three layers of the OSI model include information that is commonly inspected by a stateful firewall? (Choose three.)**

- Layer 1
- **Layer 3**
- **Layer 4**
- **Layer 5**
- Layer 7
- Layer 2

**Answers:**
- Layer 3
- Layer 4
- Layer 5

---

## Question 7
**Which type of firewall is supported by most routers and is the easiest to implement?**

- stateful firewall
- application gateway firewall
- next generation firewall
- **packet filtering firewall**

**Answer:** packet filtering firewall

---

## Question 8
**Which type of firewall generally has a low impact on network performance?**

- stateful firewall
- next generation firewall
- **stateless firewall**
- application gateway firewall

**Answer:** stateless firewall

---

## Question 9
**Which two protocols are stateless and do not generate connection information needed to build a state table? (Choose two.)**

- HTTP
- **ICMP**
- **UDP**
- FTP
- TCP

**Answers:**
- ICMP
- UDP

---

## Question 10
**Which type of traffic is usually blocked when implementing a demilitarized zone?**

- **traffic originating from the DMZ network and traveling to the private network**
- traffic originating from the private network and traveling to the DMZ network
- traffic that is returning from the public network and traveling to the DMZ network
- traffic that is returning from the DMZ network and traveling to the private network

**Answer:** traffic originating from the DMZ network and traveling to the private network

---

## Question 11
**How does a firewall handle traffic that is originating from the DMZ network and traveling to a private network?**

- Traffic is usually allowed when it is originating from the DMZ network and traveling to a private network.
- Traffic is usually not filtered using firewall rules when it is originating from the DMZ network and traveling to a private network.
- **Traffic is usually blocked when it is originating from the DMZ network and traveling to a private network.**
- Traffic is allowed when it is originating from the private network, but the response traffic from the DMZ network will be blocked.

**Answer:** Traffic is usually blocked when it is originating from the DMZ network and traveling to a private network.

---

## Question 12
**When implementing a ZPF, which statement describes a zone?**

- A zone is a group of hardened computers known as bastion hosts.
- A zone is a group of one or more devices that provide backup and disaster recovery mechanisms.
- **A zone is a group of one or more interfaces that have similar functions or features.**
- A zone is a group of administrative devices that protect against rogue access point installations.

**Answer:** A zone is a group of one or more interfaces that have similar functions or features.