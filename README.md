# Cisco-packet-tracer-static-routing
This lab demonstrates communication between two different networks connected by two routers using static routing. Each network contains a switch and a PC. Static routes were configured so devices on separate networks could successfully communicate.
## Topology
- Router 1 connected to Network A
- Router 2 connected to Network B
- Each network contains:
  - 1 Switch
  - 1 PC
- Routers connected via a point-to-point link

## Objective
Enable a PC on Network A to successfully ping a PC on Network B by configuring routing between the two routers.

## Tools Used
- Cisco Packet Tracer
- Static Routing
- ICMP (Ping)

## Result
After configuring static routes on both routers, the ping between PCs on different networks was successful.


## Lab Explanation

Initially, the PCs were unable to communicate with each other because they were located on different networks connected by separate routers. Each router only knew about its directly connected network.

When a PC attempted to ping a device on the other network, the packet was sent to its default gateway (the local router). However, the router did not know where to forward the packet next, so the ping failed.

To solve this, static routes were configured on both routers. These routes explicitly told each router which network existed on the other side and which next-hop IP address to use.

Once the static routes were added:
- Router 1 learned how to reach Network B
- Router 2 learned how to reach Network A
- ICMP echo requests were successfully forwarded between networks

This allowed the ping to complete successfully, confirming proper routing between the two networks.
