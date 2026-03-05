# Switch and Router Network Lab

## Objective
This lab demonstrates how to build and configure a small network using a router, a switch, and two PCs in Cisco Packet Tracer. The goal was to practice configuring network devices using Cisco IOS commands, assigning IP addresses, enabling interfaces, and verifying connectivity between devices across different networks.

---

## Overview

In this lab, Cisco Packet Tracer was used to create a small network consisting of:

- 1 Router (Cisco 1941)
- 1 Switch (Cisco 2960)
- 2 PCs

The lab focused on configuring network devices using Cisco IOS CLI commands and verifying connectivity between devices on different networks.

Skills practiced in this lab include:

- Network topology design
- Static IPv4 addressing
- Router interface configuration
- Switch management interface configuration
- Troubleshooting network connectivity
- Testing connectivity using the `ping` command

This lab helped reinforce the role of routers in enabling communication between different networks while switches manage communication within the same local network.

---

# Evidence and Interpretations

## Initial Network Topology

This screenshot shows the initial network topology created in Cisco Packet Tracer before configuration began. The PCs, switch, and router were connected according to the lab diagram.

![Initial Network Topology](network-topology.png)

---

## Resetting the Switch Configuration

Before configuring the switch, the startup configuration stored in NVRAM was erased to ensure the device started from a clean default state.

The following commands were used:


This removed any previous configurations and returned the switch to factory defaults.

![Switch Reset Configuration](switch-reset-config.png)

---

## PC IP Address Configuration

Static IP addresses were assigned to the PCs to allow communication within the network.

Example configuration:

- IP Address: 192.168.1.3  
- Subnet Mask: 255.255.255.0  
- Default Gateway: 192.168.1.1  

![PC IP Configuration](pc-ip-configuration.png)

---

## Initial Connectivity Test (Failure)

A ping test was performed between the PCs before router configuration. The ping request failed because the router had not yet been configured to route traffic between the networks.

This demonstrates a common troubleshooting situation where connectivity fails due to missing routing configuration.

![Initial Ping Failure](initial-ping-failure.png)

---

## Router CLI Configuration

The router was configured using the Cisco IOS command line interface (CLI). Interface IP addresses were assigned and interfaces were enabled using the `no shutdown` command.

Key configuration steps included:


This configuration allows the router to route traffic between the two networks.

![Router CLI Configuration](router-cli-configuration.png)

---

## Successful Network Connectivity

After configuring the router interfaces, connectivity tests were repeated using the ping command.

This time, the devices were able to successfully communicate across different networks.

![Successful Network Ping](successful-network-ping.png)

---

## Switch VLAN Management Configuration

The switch management interface (VLAN 1) was configured with an IP address and default gateway so the switch could be managed on the network.

Example configuration:



![Switch VLAN Configuration](switch-vlan-management-config.png)

---

## Ping Test to Switch Management Interface

A ping test was performed from PC-A to the switch management IP address (192.168.1.2) to verify connectivity and confirm that the switch was properly configured.

![Switch Management Ping](switch-management-ping.png)

---

## Final Network Topology

This screenshot shows the final network topology after all configurations were completed. All devices are properly connected and the router successfully routes traffic between networks.

![Final Network Topology](final-network-topology.png)

---

# Conclusion

In this lab, a small network consisting of a router, switch, and two PCs was successfully built and configured using Cisco Packet Tracer.

Static IPv4 addressing and Cisco IOS CLI commands were used to configure device interfaces and enable communication between different networks. Initial connectivity tests failed because routing had not yet been configured. After configuring the router interfaces and enabling them using the `no shutdown` command, the devices were able to communicate successfully.

Additionally, the switch management interface was configured so that the switch could be managed within the network.

This lab strengthened practical skills in network configuration, troubleshooting connectivity issues, and verifying communication between devices using ping tests.

---

# Tools Used

- Cisco Packet Tracer  
- Cisco IOS CLI  
- Static IPv4 Addressing  
- Ping for network connectivity testing

---

# Sources

Cisco Networking Academy – Packet Tracer Lab Instructions  
Cisco Networking Academy course modules and lesson materials
