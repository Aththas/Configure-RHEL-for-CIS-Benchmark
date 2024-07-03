# Illicit Router Advertisements
Router Advertisements (RA) are messages sent by routers in an IPv6 network to advertise their presence along with various network and link parameters. These messages are part of the Neighbor Discovery Protocol (NDP), which is used in IPv6 for various network functions, such as address autoconfiguration and router discovery.

Now, imagine your robot is in a big park with other robots. They send each other postcards (messages) to tell where they are and how to find them. These postcards are called router advertisements.

**Router Advertisements**: Messages that tell robots how to connect and talk to each other. But sometimes, a bad robot might send fake postcards to trick your robot. This is called an illicit router advertisement.

**Illicit Router Advertisements**: Fake messages that try to trick your robot into doing something it shouldn't, like going to the wrong place or talking to the wrong robot.


Illicit Router Advertisements refer to unauthorized or malicious RA messages that can lead to security issues, such as:

1. Man-in-the-Middle Attacks: An attacker can send fake RA messages to trick devices into using the attacker's machine as a default gateway, intercepting and possibly altering network traffic.

2. Network Disruption: Unauthorized RA messages can cause network confusion, leading to network disruption or denial of service.

## How to Protect Against Illicit Router Advertisements
1. Disable Acceptance of Router Advertisements: For devices that do not need to auto-configure their IP addresses or use default gateways based on RA messages, you can disable the acceptance of RAs.

2. Make the Setting Persistent :Add the parameter to a sysctl configuration file.
