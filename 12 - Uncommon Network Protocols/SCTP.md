# SCTP Support
SCTP (Stream Control Transmission Protocol) is a transport layer protocol, like TCP and UDP, designed for reliable, message-oriented communication. SCTP provides some unique features that make it particularly useful for certain types of applications, such as telecommunication signaling (e.g., SS7) and applications requiring robust data transfer.

## Key Features of SCTP:
### Multi-Homing:

SCTP supports multi-homing, where a single SCTP association (connection) can span multiple IP addresses. This provides redundancy and can improve reliability and fault tolerance.

### Multi-Streaming:

SCTP allows multiple independent streams within a single connection. Each stream can be managed separately, preventing head-of-line blocking common in TCP.

### Message-Oriented:

Unlike TCP, which is byte-oriented, SCTP is message-oriented. This means that it sends data in distinct messages, preserving message boundaries.

### Built-In Congestion Control:

SCTP includes congestion control mechanisms similar to TCP, ensuring fair usage of network resources.

### Ordered and Unordered Delivery:

SCTP supports both ordered and unordered delivery of messages within streams, providing flexibility for different types of applications.

## Kernel Module for SCTP:
In Linux, SCTP support is provided by the sctp kernel module. This module must be loaded into the kernel to enable SCTP functionality.

## Security Considerations:
Enabling SCTP increases the attack surface of your system. If SCTP is not required for your environment, it is a good security practice to disable and blacklist the sctp kernel module to reduce potential vulnerabilities.

## simple explanation
Imagine you have a new way to send messages to your friends, called SCTP. This new way has some cool features:

**Multiple Addresses**: You can send messages to your friends even if they are moving around, by using multiple addresses.

**Multiple Streams**: You can send different types of messages at the same time without them getting mixed up.

**Message Packages**: SCTP sends messages in neat packages, so they don't get mixed up or lost.

But, if you don't need this new way to send messages, you might want to turn it off to keep things simple and safe.

To turn off SCTP, you can tell your computer:

**Don't Use SCTP (install sctp /bin/true)**: Pretend SCTP doesn't exist.

**Don't Load SCTP (blacklist sctp)**: Make sure no one can use SCTP.

By doing this, you make sure your computer doesn't use SCTP if it's not needed, keeping it safer from potential problems.
