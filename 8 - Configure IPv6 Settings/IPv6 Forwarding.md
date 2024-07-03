# IPv6 Forwarding
Imagine you are at a mail sorting center, and your job is to take mail from one bin and place it in another bin that will send it to its final destination. This is similar to what a computer or router does with IPv6 forwarding.

## Simple Explanation
### What is IPv6?

IPv6 is like a new version of the address system for computers on the internet. Just like your home address helps mail reach you, IPv6 addresses help data reach the correct computer.

### Forwarding Data:

When a computer receives data that is not meant for itself, it can pass it on to the correct destination. This is called forwarding.

Think of it like this: If you get a letter by mistake that is meant for your neighbor, you take it to your neighbor's house. This is what IPv6 forwarding does with internet data.

## Technical Explanation:
### IPv6 Forwarding:

IPv6 forwarding is the process where a router or a computer forwards IPv6 packets (chunks of data) from one network interface to another. This is essential for routing data between different networks.

### How It Works:

When a device (like a router) receives an IPv6 packet, it checks the destination address of the packet.
If the packet's destination is not the device itself, the router uses its routing table to decide the best next hop (another router or the destination device) and forwards the packet accordingly.

### Enabling IPv6 Forwarding:

By default, IPv6 forwarding is usually disabled on most devices to prevent accidental routing and potential security risks.
To enable IPv6 forwarding, you need to set a specific kernel parameter.
