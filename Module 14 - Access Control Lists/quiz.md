 Quiz: ACLs

## Question 1

In applying an ACL to a router interface, which traffic is designated as outbound?

- traffic that is coming from the source IP address into the router
- **traffic that is leaving the router and going toward the destination host**
- traffic that is going from the destination IP address into the router
- traffic for which the router can find no routing table entry

**Answer:** traffic that is leaving the router and going toward the destination host

---

## Question 2

Refer to the exhibit. A network administrator wants to create a standard ACL to prevent Network 1 traffic from being transmitted to the Research and Development network. On which router interface and in which direction should the standard ACL be applied?

- R1 Gi0/0 inbound
- R1 Gi0/0 outbound
- R1 S0/0/0 outbound
- R2 S0/0/0 inbound
- **R2 Gi0/0 outbound**
- R2 Gi0/0 inbound

**Answer:** R2 Gi0/0 outbound

---

## Question 3

Which operator is used in an ACL statement to match packets of a specific application?

- **eq**
- lt
- gt
- established

**Answer:** eq

---

## Question 4

Which two statements describe appropriate general guidelines for configuring and applying ACLs? (Choose two.)

- Multiple ACLs per protocol and per direction can be applied to an interface.
- **If an ACL contains no permit statements, all traffic is denied by default.**
- **The most specific ACL statements should be entered first because of the top-down sequential nature of ACLs.**
- Standard ACLs are placed closest to the source, whereas extended ACLs are placed closest to the destination.
- If a single ACL is to be applied to multiple interfaces, it must be configured with a unique number for each interface.

**Answers:**

- If an ACL contains no permit statements, all traffic is denied by default.
- The most specific ACL statements should be entered first because of the top-down sequential nature of ACLs.

---

## Question 5

Refer to the exhibit.

```text
permit icmp any any nd-na
permit icmp any any nd-ns
deny ipv6 any any
```

Which statement describes the function of the ACEs?

- These ACEs allow for IPv6 neighbor discovery traffic.
- These ACEs must be manually added to the end of every IPv6 ACL to allow IPv6 routing to occur.
- **These ACEs automatically appear at the end of every IPv6 ACL to allow IPv6 routing to occur.**
- These are optional ACEs that can be added to the end of an IPv6 ACL to allow ICMP messages that are defined in object groups named nd-na and nd-ns.

**Answer:** These ACEs automatically appear at the end of every IPv6 ACL to allow IPv6 routing to occur.

---

## Question 6

What wildcard mask will match networks 172.16.0.0 through 172.19.0.0?

- 0.0.3.255
- 0.0.255.255
- 0.252.255.255
- **0.3.255.255**

**Answer:** 0.3.255.255

---

## Question 7

What method is used to apply an IPv6 ACL to a router interface?

- the use of the access-class command
- the use of the ip access-group command
- **the use of the ipv6 traffic-filter command**
- the use of the ipv6 access-list command

**Answer:** the use of the ipv6 traffic-filter command

---

## Question 8

Which ICMP message type should be stopped inbound?

- **echo**
- echo-reply
- unreachable
- source quench

**Answer:** echo

---

## Question 9

What type of ACL offers greater flexibility and control over network access?

- flexible
- named standard
- **extended**
- numbered standard

**Answer:** extended

---

## Question 10

Refer to the exhibit. A network administrator is configuring an IPv6 ACL to allow hosts on the 2001:DB8:CAFE:10::/64 network to access remote web servers, except for PC1. However, a user on PC1 can successfully access the web server PC2. Why is this possible?

- The IPv6 ACL Deny_WEB is spelled incorrectly when applied to the interface.
- The IPv6 ACL Deny_WEB is applied to the wrong interface of router R1.
- The IPv6 ACL Deny_WEB is applied in the incorrect direction on router R1.
- **The IPv6 ACL Deny_WEB is permitting all web traffic before the specific host is blocked.**

**Answer:** The IPv6 ACL Deny_WEB is permitting all web traffic before the specific host is blocked.

---

## Question 11

Which scenario would cause an ACL misconfiguration and deny all traffic?

- Apply a standard ACL in the inbound direction.
- Apply a named ACL to a VTY line.
- **Apply an ACL that has all deny ACE statements.**
- Apply a standard ACL using the ip access-group out command.

**Answer:** Apply an ACL that has all deny ACE statements.

---

## Question 12

What is the quickest way to remove a single ACE from a named ACL?

- **Use the no keyword and the sequence number of the ACE to be removed.**
- Use the no access-list command to remove the entire ACL, then recreate it without the ACE.
- Copy the ACL into a text editor, remove the ACE, then copy the ACL back into the router.
- Create a new ACL with a different number and apply the new ACL to the router interface.

**Answer:** Use the no keyword and the sequence number of the ACE to be removed.

---

## Question 13

Which two keywords can be used in an access control list to replace a wildcard mask or address and wildcard mask pair? (Choose two.)

- most
- **host**
- all
- **any**
- some
- gt

**Answers:**

- host
- any

---

## Question 14

Consider the following access list.

```text
access-list 100 permit ip host 192.168.10.1 any
access-list 100 deny icmp 192.168.10.0 0.0.0.255 any echo
access-list 100 permit ip any any
```

Which two actions are taken if the access list is placed inbound on a router Gigabit Ethernet port that has the IP address 192.168.10.254 assigned? (Choose two.)

- **A Telnet or SSH session is allowed from any device on the 192.168.10.0 network into the router with this access list assigned.**
- **Devices on the 192.168.10.0/24 network are allowed to reply to any ping requests.**
- Only Layer 3 connections are allowed to be made from the router to any other network device.
- Only the network device assigned the IP address 192.168.10.1 is allowed to access the router.
- Devices on the 192.168.10.0/24 network can successfully ping devices on the 192.168.11.0 network.

**Answers:**

- A Telnet or SSH session is allowed from any device on the 192.168.10.0 network into the router with this access list assigned.
- Devices on the 192.168.10.0/24 network are allowed to reply to any ping requests.