# Quiz: ACLs, Firewalls, and Cloud Security

## Question 1

Refer to the exhibit.

```text
Router(config)# ip access-list extended SECURE
Router(config-ext-nacl)# permit tcp any 192.168.254.0 0.0.1.255 established
Router(config-ext-nacl)# end
Router#
```

What is the result of adding the `established` argument to the end of the ACE?

- [ ] Any IP traffic is allowed to reach the 192.168.254.0 255.255.254.0 network as long as it is in response to an originated request.
- [x] Any TCP traffic is allowed to reach the 192.168.254.0 255.255.254.0 network if it is in response to an originated request.
- [ ] 192.168.254.0 /23 traffic is allowed to reach any network.
- [ ] Any traffic is allowed to reach the 192.168.254.0 255.255.254.0 network.

**Answer:** Any TCP traffic is allowed to reach the 192.168.254.0 255.255.254.0 network if it is in response to an originated request.

---

## Question 2

Which type of packet is unable to be filtered by an outbound ACL?

- [x] router-generated packet
- [ ] ICMP packet
- [ ] multicast packet
- [ ] broadcast packet

**Answer:** router-generated packet

---

## Question 3

When an inbound Internet-traffic ACL is being implemented, what should be included to prevent the spoofing of internal networks?

- [x] ACEs to prevent traffic from private address spaces
- [ ] ACEs to prevent ICMP traffic
- [ ] ACEs to prevent broadcast address traffic
- [ ] ACEs to prevent HTTP traffic
- [ ] ACEs to prevent SNMP traffic

**Answer:** ACEs to prevent traffic from private address spaces

---

## Question 4

Refer to the exhibit.

```text
Router(config)# access-list 1 deny 172.16.0.1
% Access rule can't be configured at higher sequence num
as it is part of the existing rule at sequence num 10
Router(config)# exit
Router# show access-lists 1
Standard IP access list 1
    10 permit 172.16.0.0, wildcard bits 0.0.255.255
```

A router has an existing ACL that permits all traffic from the 172.16.0.0 network. The administrator attempts to add a new statement to the ACL that denies packets from host 172.16.0.1 and receives the error message shown. What action can the administrator take to block packets from host 172.16.0.1 while still permitting all other traffic from the 172.16.0.0 network?

- [x] Manually add the new deny statement with a sequence number of 5.
- [ ] Create a second access list denying the host and apply it to the same interface.
- [ ] Manually add the new deny statement with a sequence number of 15.
- [ ] Add a deny any any statement to access-list 1.

**Answer:** Manually add the new deny statement with a sequence number of 5.

---

## Question 5

What single access list statement matches all of the following networks?

```text
192.168.16.0
192.168.17.0
192.168.18.0
192.168.19.0
```

- [x] access-list 10 permit 192.168.16.0 0.0.3.255
- [ ] access-list 10 permit 192.168.0.0 0.0.15.255
- [ ] access-list 10 permit 192.168.16.0 0.0.15.255
- [ ] access-list 10 permit 192.168.16.0 0.0.0.255

**Answer:** access-list 10 permit 192.168.16.0 0.0.3.255

---

## Question 6

What are two characteristics of a stateful firewall? (Choose two.)

- [ ] uses complex ACLs which can be difficult to configure
- [ ] uses static packet filtering techniques
- [x] uses connection information maintained in a state table
- [ ] prevents Layer 7 attacks
- [x] analyzes traffic at Layers 3, 4, and 5 of the OSI model

**Answer:**

- uses connection information maintained in a state table
- analyzes traffic at Layers 3, 4, and 5 of the OSI model

---

## Question 7

Which type of firewall is commonly part of a router firewall and allows or blocks traffic based on Layer 3 and Layer 4 information?

- [ ] stateful firewall
- [ ] application gateway firewall
- [x] stateless firewall
- [ ] proxy firewall

**Answer:** stateless firewall

---

## Question 8

How does a firewall handle traffic when it is originating from the public network and traveling to the DMZ network?

- [x] Traffic that is originating from the public network is inspected and selectively permitted when traveling to the DMZ network.
- [ ] Traffic that is originating from the public network is usually forwarded without inspection when traveling to the DMZ network.
- [ ] Traffic that is originating from the public network is usually permitted with little or no restriction when traveling to the DMZ network.
- [ ] Traffic that is originating from the public network is usually blocked when traveling to the DMZ network.

**Answer:** Traffic that is originating from the public network is inspected and selectively permitted when traveling to the DMZ network.

---

## Question 9

What is one limitation of a stateful firewall?

- [ ] poor log information
- [ ] weak user authentication
- [ ] cannot filter unnecessary traffic
- [x] not as effective with UDP- or ICMP-based traffic

**Answer:** not as effective with UDP- or ICMP-based traffic

---

## Question 10

How does a firewall handle traffic when it is originating from the private network and traveling to the DMZ network?

- [ ] The traffic is usually blocked.
- [ ] The traffic is selectively permitted and inspected.
- [ ] The traffic is selectively denied based on service requirements.
- [x] The traffic is usually permitted with little or no restrictions.

**Answer:** The traffic is usually permitted with little or no restrictions.

---

## Question 11

Which zone-based policy firewall zone is system-defined and applies to traffic destined for the router or originating from the router?

- [x] self zone
- [ ] system zone
- [ ] inside zone
- [ ] local zone
- [ ] outside zone

**Answer:** self zone

---

## Question 12

Which two statements describe the two configuration models for Cisco IOS firewalls? (Choose two.)

- [ ] IOS Classic Firewalls must be enabled in the router configuration before enabling ZPF.
- [x] IOS Classic Firewalls and ZPF models can be enabled on a router concurrently.
- [x] The IOS Classic Firewall and ZPF cannot be combined on a single interface.
- [ ] ZPF must be enabled in the router configuration before enabling an IOS Classic Firewall.
- [ ] Both IOS Classic Firewall and ZPF models require ACLs to define traffic filtering policies.

**Answer:**

- IOS Classic Firewalls and ZPF models can be enabled on a router concurrently.
- The IOS Classic Firewall and ZPF cannot be combined on a single interface.

---

## Question 13

When using Cisco IOS zone-based policy firewall, where is the inspection policy applied?

- [ ] to an interface
- [ ] to a global service policy
- [ ] to a zone
- [x] to a zone pair

**Answer:** to a zone pair

---

## Question 14

What are two benefits of using a ZPF rather than a Classic Firewall? (Choose two.)

- [ ] With ZPF, the router will allow packets unless they are explicitly blocked.
- [ ] ZPF allows interfaces to be placed into zones for IP inspection.
- [ ] Multiple inspection actions are used with ZPF.
- [x] The ZPF is not dependent on ACLs.
- [x] ZPF policies are easy to read and troubleshoot.

**Answer:**

- The ZPF is not dependent on ACLs.
- ZPF policies are easy to read and troubleshoot.

---

## Question 15

When a Cisco IOS zone-based policy firewall is being configured, which three actions can be applied to a traffic class? (Choose three.)

- [ ] shape
- [x] drop
- [x] inspect
- [x] pass
- [ ] reroute
- [ ] queue

**Answer:**

- drop
- inspect
- pass

---

## Question 16

Which technique can be used to leverage virtual network topologies to run smaller and more isolated networks without incurring additional hardware costs?

- [ ] shadow IT
- [ ] edge computing
- [x] microsegmentation
- [ ] fog computing

**Answer:** microsegmentation

---

## Question 17

Which cloud security domain covers cloud-specific aspects of infrastructure security and foundations for operating securely in the cloud?

- [ ] Application Security
- [ ] Data Security and Encryption
- [x] Infrastructure Security
- [ ] Management Plane and Business Continuity

**Answer:** Infrastructure Security

---

## Question 18

Which algorithm is used with symmetric encryption to provide confidentiality?

- [x] AES
- [ ] ECC
- [ ] RSA
- [ ] MD5

**Answer:** AES

---

## Question 19

In which phase of application development is new software verified to run under the required security settings?

- [ ] provisioning
- [x] testing
- [ ] staging
- [ ] developing

**Answer:** testing

---

## Question 20

Match the threats to cloud computing to the description.

| Category | Description | Correct option |
|---|---|---|
| A | occurs when a cloud customer employee, contractor, or business partner maliciously or unintentionally compromises the cloud service | Inside Threat |
| B | occurs when the cloud computing resource is set up incorrectly, making it vulnerable to attacks | Cloud Misconfiguration |
| C | occurs when the cloud customer does not have full visibility into the cloud service, making the identification of safe or malicious files more difficult | Limited Cloud Usage Visibility |
| D | occurs when user accounts or access privileges are not properly secured and are hijacked by threat actors | Compromised Account Credentials |
| E | occurs when the shared security responsibilities between a cloud customer and cloud provider are not implemented correctly | Poor Cloud Security Architecture Strategy |

**Answer:**

- A → Inside Threat
- B → Cloud Misconfiguration
- C → Limited Cloud Usage Visibility
- D → Compromised Account Credentials
- E → Poor Cloud Security Architecture Strategy

---

## Question 21

What technology has a function of using trusted third-party protocols to issue credentials that are accepted as an authoritative identity?

- [ ] symmetric keys
- [x] PKI certificates
- [ ] hashing algorithms
- [ ] digital signatures

**Answer:** PKI certificates

---

## Question 22

Match the description with the correct term.

| Category | Description | Correct option |
|---|---|---|
| A | discovering that hidden information exists within a graphic file | steganalysis |
| B | creating a message that says one thing but means something else to a specific audience | social steganography |
| C | hiding data within an audio file | steganography |
| D | making a message confusing so it is harder to understand | obfuscation |

**Answer:**

- A → steganalysis
- B → social steganography
- C → steganography
- D → obfuscation

---

## Question 23

An IT enterprise is recommending the use of PKI applications to securely exchange information between the employees. In which two cases might an organization use PKI applications to securely exchange information between users? (Choose two.)

- [ ] local NTP server
- [ ] file and directory access permission
- [ ] FTP transfers
- [x] 802.1x authentication
- [x] HTTPS web service

**Answer:**

- 802.1x authentication
- HTTPS web service

---

## Question 24

Which method tries all possible passwords until a match is found?

- [ ] birthday
- [ ] rainbow tables
- [ ] cryptographic
- [ ] cloud
- [x] brute force
- [ ] dictionary

**Answer:** brute force

---

## Question 25

Which measure can a security analyst take to perform effective security monitoring against network traffic encrypted by SSL technology?

- [ ] Deploy a Cisco ASA.
- [x] Deploy a Cisco SSL Appliance.
- [ ] Use a Syslog server to capture network traffic.
- [ ] Require remote access connections through IPsec VPN.

**Answer:** Deploy a Cisco SSL Appliance.
