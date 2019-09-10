### Goal:
1. Configure the network according to the scheme, using only static routing
2. Verify the network is working with the ping command (all interfaces from everywhere must ping)
3. Check the routing tables
4. Practice using the tracert command
5. *. Configure loop back interfaces


### Solution:
1. For each PC and Server need to set up the IP address in FastEthernet0 > IP Configuration and check if the port is turned on. Set the Gateway.
2. Configure each port of the router it's own IP address.
3. Configure loop back interfaces on r5 and r6. Use commands:
* =>`int lo0 (or any other number)`
* =>`ip addr (use ip address followed by mask)`
4. To switch packet from one network to another, we need to manually set static routes on every router we have on the way of this packet. To set route use command:
* =>`ip route` 















