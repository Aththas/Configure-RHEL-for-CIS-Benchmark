# ICMP Redirect Messages
ICMP Redirect Messages are a type of Internet Control Message Protocol (ICMP) message used by routers to inform a host that a better route is available for a particular destination. This is typically used for optimizing the routing of packets in a network. However, these messages can be exploited by attackers to perform malicious activities, such as redirecting traffic to an unintended path, leading to potential security risks.

Imagine you are riding your bike and your friend tells you there's a shortcut to get to the park faster. This message from your friend is like an ICMP Redirect Message. It helps you find a better way to reach your destination.

## How ICMP Redirect Works
### 1. Normal Operation:

When a host sends a packet to a router, and the router knows a better route to the packet’s destination, it sends an ICMP Redirect message back to the host.
The host then updates its routing table to use the new route suggested by the ICMP Redirect message.

### 2. Fields in an ICMP Redirect Message:

**Type**: Identifies the type of message (e.g., Redirect message is type 5).

**Code**: Specifies the specific type of redirect (e.g., 0 for network redirect, 1 for host redirect).

**Checksum**: Used for error-checking the message.

**Gateway Address**: The IP address of the gateway to which the packet should be redirected.

**Original Datagram**: The initial portion of the original datagram that triggered the redirect.

# Illicit ICMP Redirect Messages
Illicit ICMP Redirect Messages are maliciously crafted ICMP Redirect messages used by attackers to manipulate the routing tables of hosts, leading to potential security breaches. By sending false ICMP Redirect messages, attackers can redirect traffic to a malicious gateway, enabling them to intercept, modify, or drop packets, leading to a variety of attacks, such as:

Now, imagine a stranger comes up and tells you to take a different path, but this path leads you away from the park to a dangerous place. This is like an Illicit ICMP Redirect Message. The stranger is trying to trick you into going somewhere you shouldn't.

**Man-in-the-Middle (MitM) Attacks**: An attacker can redirect traffic through a malicious gateway, intercepting and potentially modifying the data.

**Denial of Service (DoS) Attacks**: Redirecting traffic to an invalid or unreachable gateway can cause a disruption in network services.

**Traffic Analysis**: By redirecting traffic, an attacker can monitor the data being sent and received by the host.

## Example of Illicit ICMP Redirect Attack
### Scenario:

An attacker on the same network as the target host sends an illicit ICMP Redirect message.
The message falsely informs the target host that a better route exists through a malicious gateway controlled by the attacker.

### Consequences:

The target host updates its routing table to use the attacker's gateway.
All subsequent traffic from the target host is routed through the attacker’s gateway, enabling the attacker to intercept or manipulate the data.
