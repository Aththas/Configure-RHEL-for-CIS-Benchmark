# TCP Syncookies
TCP Syncookies is a security mechanism used to protect against SYN flood attacks, which are a type of Denial-of-Service (DoS) attack. This mechanism helps manage incoming TCP connection requests in a way that prevents server resource exhaustion.

## What is a SYN Flood Attack?
**SYN Flood Attack**: A type of attack where an attacker sends a large number of TCP connection requests (SYN packets) to a target server, but does not complete the handshake. This causes the server to allocate resources for each incomplete connection, potentially exhausting its resources and making it unable to handle legitimate connections.

## TCP Handshake
To understand TCP Syncookies, it's important to know the basics of the TCP handshake:

**SYN**: The client sends a SYN (synchronize) packet to the server to start a connection.

**SYN-ACK**: The server responds with a SYN-ACK (synchronize-acknowledge) packet, acknowledging the client's request.

**ACK**: The client sends an ACK (acknowledge) packet back to the server, completing the handshake, and the connection is established.


In a SYN flood attack, the attacker sends many SYN packets but does not respond to the SYN-ACK packets, leaving the server waiting and consuming resources.

## How TCP Syncookies Work
TCP Syncookies help mitigate SYN flood attacks by not allocating resources for a connection until the handshake is completed. Here's how it works:

### 1. Initial SYN Packet:

When the server receives a SYN packet, instead of allocating resources and storing the connection state, it creates a special SYN-ACK packet with a cryptographic cookie.

### 2. Sending the SYN-ACK:

The server sends the SYN-ACK packet with the cookie back to the client.

### 3. Validating the ACK Packet:

If the client responds with an ACK packet that includes the correct cookie, the server knows the connection is legitimate and allocates resources to complete the connection.

### 4. Ignoring Invalid Responses:

If the client does not respond or responds incorrectly, the server does not allocate any resources, effectively mitigating the impact of the attack.

## Summary
**TCP Handshake**: Think of it like a secret handshake between two friends to start playing together.

**SYN Flood Attack**: A bully keeps pretending to start the handshake but never finishes it, so the friend gets tired and can't play with anyone else.

**TCP Syncookies**: It's like having a special code in the handshake. The friend doesn't start playing until the code is correctly given, making sure only real friends (and not bullies) get to play.


By enabling TCP Syncookies, network administrators can protect their servers from SYN flood attacks, ensuring that resources are allocated only to legitimate connection requests and maintaining the availability of network services.
