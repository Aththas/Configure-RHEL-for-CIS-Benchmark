# RDS Support
RDS (Reliable Datagram Sockets) is a transport layer protocol designed for high-performance, low-latency communication between nodes in a cluster. It is commonly used in environments that require efficient communication between servers, such as in high-performance computing (HPC) clusters and database systems.

## Key Features of RDS:
### Reliable Delivery:

Ensures that messages are delivered reliably between nodes in a cluster.

### Low Latency:

Optimized for low-latency communication, making it suitable for performance-critical applications.

### Connectionless Protocol:

Unlike TCP, RDS is connectionless, meaning that it does not establish a persistent connection between nodes. This reduces the overhead associated with connection management.

### Scalability:

Designed to scale well in large clusters, providing efficient communication even as the number of nodes increases.

### Built-In Congestion Control:

Includes mechanisms for managing congestion, ensuring that the network remains stable under load.

## Kernel Module for RDS:
In Linux, support for the RDS protocol is provided by the rds kernel module. This module must be loaded into the kernel for RDS functionality to be available.

## Security Considerations:
Similar to other network protocols, enabling RDS can increase the attack surface of your system. If RDS is not required for your environment, it is a good security practice to disable and blacklist the rds kernel module.

## Simple explanationn
Imagine you have a special way of sending messages really fast to your friends in a big playground. This special way is called RDS. But if you don't need to send messages like this, you might want to make sure no one can use it to keep things safe.

**Reliable Messages**: RDS makes sure your messages get to your friends without getting lost.

**Fast Communication**: It helps you send messages really quickly.

**No Constant Checking**: Unlike other ways that check every time if your friend is still there, RDS just sends the message.

To turn off RDS, you tell your computer, "Hey, don't use this special way to send messages." You can do this by:

**Hiding the Special Way (install rds /bin/true)**: Pretend the special way doesn't exist.

**Putting Up a Sign (blacklist rds)**: Tell everyone not to use it.

By using these commands, you make sure your computer doesn't use RDS if it's not needed, keeping it safer from potential problems.
