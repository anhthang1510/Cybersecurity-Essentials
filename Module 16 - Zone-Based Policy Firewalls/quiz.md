# Quiz - Zone-Based Policy Firewall (ZPF)

## Question 1
**Which statement describes a feature of a zone-based policy firewall?**

- It does not depend on ACLs.
- It uses a flat, non-hierarchical data structure making it easier to configure and troubleshoot.
- The router security posture is to allow traffic unless explicitly blocked.
- All traffic through a given interface is subject to the same inspection.

**Correct answer:** It does not depend on ACLs.

---

## Question 2
**Which statement describes a zone when implementing ZPF on a Cisco router?**

- A zone establishes a security border of a network.
- Only one zone can be attached to a single interface.
- A zone is used to define security policies for a unique interface on the router.
- A zone is used to implement traffic filtering for either TCP or UDP.

**Correct answer:** A zone establishes a security border of a network.

---

## Question 3
**Designing a ZPF requires several steps. Which step involves defining boundaries where traffic is subjected to policy restrictions as it crosses to another region of the network?**

- establish policies between zones
- identify subsets within zones and merge traffic requirements
- design the physical infrastructure
- determine the zones

**Correct answer:** determine the zones

---

## Question 4
**Which statement describes one of the rules that govern interface behavior in the context of implementing a zone-based policy firewall configuration?**

- By default, traffic is allowed to flow between a zone member interface and any interface that is not a zone member.
- An administrator can assign an interface to multiple security zones.
- An administrator can assign interfaces to zones, regardless of whether the zone has been configured.
- By default, traffic is allowed to flow among interfaces that are members of the same zone.

**Correct answer:** By default, traffic is allowed to flow among interfaces that are members of the same zone.

---

## Question 5
**Which three statements describe zone-based policy firewall rules that govern interface behavior and the traffic moving between zone member interfaces? (Choose three.)**

- An interface can be assigned to multiple security zones.
- Interfaces can be assigned to a zone before the zone is created.
- To permit traffic to and from a zone member interface, a policy allowing or inspecting traffic must be configured between that zone and any other zone.
- If traffic is to flow between all interfaces in a router, each interface must be a member of a zone.
- Pass, inspect, and drop options can only be applied between two zones.
- Traffic is implicitly prevented from flowing by default among interfaces that are members of the same zone.

**Correct answers:**
- To permit traffic to and from a zone member interface, a policy allowing or inspecting traffic must be configured between that zone and any other zone.
- If traffic is to flow between all interfaces in a router, each interface must be a member of a zone.
- Pass, inspect, and drop options can only be applied between two zones.

---

## Question 6
**In ZPF design, what is described as the self zone?**

- a predefined cluster of routers with configured interfaces
- the router itself, including all interfaces with assigned IP addresses
- a predefined cluster of servers with configured interfaces
- the outward facing interface on the edge router

**Correct answer:** the router itself, including all interfaces with assigned IP addresses

---

## Question 7
**How does ZPF handle traffic between an interface that is a zone member and another interface that does not belong to any zone?**

- inspect
- drop
- pass
- allow

**Correct answer:** drop

---

## Question 8
**Which statement describes a factor to be considered when configuring a zone-based policy firewall?**

- The router always filters the traffic between interfaces in the same zone.
- The classic firewall `ip inspect` command can coexist with ZPF as long as it is used on interfaces that are in the same security zones.
- An interface can belong to multiple zones.
- A zone must be configured with the `zone security` global command before it can be used in the `zone-member security` command.

**Correct answer:** A zone must be configured with the `zone security` global command before it can be used in the `zone-member security` command.

---

## Question 9
**Which statement accurately describes Cisco IOS zone-based policy firewall operation?**

- The pass action works in only one direction.
- Service policies are applied in interface configuration mode.
- Router management interfaces must be manually assigned to the self zone.
- A router interface can belong to multiple zones.

**Correct answer:** The pass action works in only one direction.

---

## Question 10
**When a Cisco IOS zone-based policy firewall is being configured, which two actions can be applied to a traffic class? (Choose two.)**

- copy
- inspect
- forward
- hold
- drop
- log

**Correct answers:**
- inspect
- drop

---

## Question 11
**In what step of zone-based policy firewall configuration is traffic identified for policy application?**

- creating policy maps
- defining zones
- assigning policy maps to zones
- configuring class maps

**Correct answer:** configuring class maps

---

## Question 12
**When configuring a class map for a zone-based policy firewall, how is the match criteria applied when using the match-all parameter?**

- Traffic must match at least one of the match criteria statements.
- Traffic must match the first criteria in the statement.
- Traffic must match all of the match criteria specified in the statement.
- Traffic must match all of the criteria solely defined by ACLs.

**Correct answer:** Traffic must match all of the match criteria specified in the statement.