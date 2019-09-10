### Goal:
1. Configure the network according to the scheme, using only dynamic routing (RIPv2)
2. Verify the network is working with the ping command (all interfaces from everywhere must ping)
3. Check the routing tables
4. Practice using the tracert command
5. Configure the DHCP server on r1 for the network 10.0.0.0/24


### Solution:
1. For the Server need to set up the IP address in FastEthernet0 > IP Configuration and check if the port is turned on. Set the Gateway.
2. Configure each port of the router it's own IP address.
3. Configure loop back interfaces on r5 and r6. Use commands:
* =>`int lo0 (or any other number)`
* =>`ip addr (use ip address followed by mask)`
4. Setup RIP adresses for each router:
* => `route rip`
* => `version 2`
* => `no auto-summary`
* => `network (network IP)`
5. Configure DHCP server on the r0.
* => `service ?`
* => `ip dhcp ?`
* => `ip dhcp pool (pool name)`
* => `network (IP with mask)`
* => `defauilt-router (IP)`
* => `dns-server (IP)`














