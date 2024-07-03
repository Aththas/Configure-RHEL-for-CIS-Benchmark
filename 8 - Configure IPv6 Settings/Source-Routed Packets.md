# Source-Routed Packets on IPv6 Interfaces
Imagine you’re sending a package to a friend, but instead of letting the delivery person choose the best route, you write down every single stop the package should make along the way. This is similar to what source-routed packets do in a network.

## What Are Source-Routed Packets?

**Source-Routed Packets**: These are data packets where the sender specifies the exact route the packet should take through the network, rather than letting each router along the way decide the next hop.

**IPv6 Interfaces**: These are the network interfaces on devices that handle IPv6 traffic, which is the newer version of internet addressing.

## How It Normally Works

**Normal Packet Routing**: When you send a packet (like a letter), each router (like a post office) decides the best next hop to get it closer to its destination. The packet hops from router to router until it reaches its target.

**Source Routing**: In source routing, the sender specifies the route, listing all the intermediate stops (routers) the packet must take.

## Risks of Source-Routed Packets
### Security Concerns:

**Manipulation**: Attackers can manipulate the route to send packets through vulnerable or untrusted networks, potentially intercepting or altering the data.

**Bypassing Security**: Source-routed packets can be used to bypass security controls, like firewalls, that rely on standard routing.

### Network Performance:

**Inefficiency**: Specifying a route might not be the most efficient path, causing delays or congestion in the network.

**Resource Consumption**: Processing source-routed packets requires more resources, as routers need to handle the specified route instructions.

## Summary

**Source-Routed Packets**: Like sending a package with a specific delivery route written on it.

**Normal Routing**: Letting each post office (router) decide the best way to forward the package.

**Risks**: Bad people (attackers) can trick the delivery route, causing security issues or delays.

**Protection**: Telling the delivery system (network) to ignore specific routes and just use the best paths it knows.
<br><br>
By disabling source-routed packets, you help ensure that data follows the safest and most efficient paths through the network, reducing the risk of manipulation and improving overall security and performance.
