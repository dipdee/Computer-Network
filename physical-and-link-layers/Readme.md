### Goal:
1. Fix problems with links on all hosts.
2. Configure network interfaces on all hosts and management on switches.
3. Outline in blue all broadcast domains, and in red all collision domains.

### Solution:
1. For each PC need to set up the IP address in FastEthernet0 > IP Configuration and check if the port is turned on.
2. Set up sw1 with the following commands:
* =>`en`
* =>`conf t`
* =>`interface vlan1`
* =>`ip add 192.168.1.1 255.255.0.0`
* =>`no shut`
3. Set up sw2 with the following commands:
* =>`en`
* =>`conf t`
* =>`interface vlan1`
* =>`ip add 192.168.1.2 255.255.0.0`
* =>`no shut`
4. It’s necessary to set up bandwidth 100 Mbps and full-duplex for each PC(except PC-PT 10.0.0.8 and PC-PT 10.0.0.9 because they are connected via Hub)
5. Check sw1 and sw2, all connected ports need to be set in a full-duplex mode with 100 Mbps bandwidth.
6. PC has to be connected to switch with Streight Through cables and switch to switch has to be connected by Crossover cable.
7. Connect sw1 to Hub0 with Crossover cable and connection port need to switch to half-duplex mode.
8. Hub needs to be connected to the PC-PT 10.0.0.8 and PC-PT 10.0.0.9 with Streight Through cables and both computers need to turn to the half-duplex mode.







