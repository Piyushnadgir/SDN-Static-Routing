# SDN-Static-Routing
# Static Routing using SDN (Mininet)

## Overview

This project demonstrates how network routing can be controlled manually using Software Defined Networking (SDN). Instead of allowing the network to decide how data is forwarded, explicit rules are defined to control the path of packets.

## Objective

The objective of this project is to:

* Create a simple network topology
* Observe behavior without any routing rules
* Manually define routing paths
* Verify communication between hosts
* Test what happens when rules are removed and reapplied

## Network Topology

The network consists of:

* Two hosts: h1 and h2
* Two switches: s1 and s2

Topology structure:
h1 — s1 — s2 — h2

## Methodology

### Initial Behavior

At the beginning, the network is created without any predefined rules. When communication is tested, it fails because the switches do not know where to send the data.

### Manual Routing

Routing rules are then added manually to each switch. These rules define how packets should move from one port to another, effectively controlling the path of data through the network.

### Validation

After applying the rules, communication between the hosts becomes successful. This confirms that the manually defined paths are working correctly.

### Regression Testing

The routing rules are removed, and communication is tested again. As expected, the network stops working. When the same rules are reapplied, communication is restored. This shows that the behavior of the network depends entirely on the defined rules.

## Results

* Without rules: communication fails
* With rules: communication is successful
* After removing rules: communication fails again
* After reapplying rules: communication is restored

## Conclusion

This project demonstrates that network behavior in an SDN environment can be controlled manually using flow rules. It highlights how defining explicit paths allows precise control over how data travels through the network.
