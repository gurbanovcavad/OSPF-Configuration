# OSPF Single-Area Routing Configuration

This project demonstrates the use of **OSPF (Open Shortest Path First)** routing in a single area to ensure that all end devices (PCs and servers) can communicate with each other.

---

## 📝 Task Description

- All **PCs must be able to access each server** across the network.
- Use **OSPF single-area routing** to enable dynamic route exchange.
- Activate **Telnet/SSH access** on routers for remote management.

---

## 🌐 IP Addressing & VLANs

| VLAN | Subnet         | Description    |
|------|----------------|----------------|
| 10   | 10.0.0.0/30    | PC0            |
| 20   | 10.0.0.4/30    | DNS Server     |
| 30   | 10.0.0.8/30    | GOOGLE Server  |
| 40   | 10.0.0.12/30   | PC2            |
| 50   | 10.0.0.16/30   | YANDEX Server  |
| 60   | 10.0.0.20/30   | PC3            |
| WAN  | 10.0.0.24/30 - 10.0.0.36/30 | Router-to-Router links |
| Loopbacks | 192.168.1.1 – 1.4 | Router IDs |

---
## Configuration Steps

### 1. Assign IP Addresses
- Configure all router interfaces with the correct IP addresses according to the topology.
- Set IP addresses, subnet masks, and default gateways on all PCs and servers.

### 2. Configure OSPF Routing
- Enable OSPF routing on each router.
- Set a unique router ID on each router.
- Add all directly connected networks into OSPF using the `network` command.
- Ensure all routers are in **OSPF Area 0**.

### 3. Activate Telnet/SSH Access on Routers
- Set a hostname for each router.
- Set console and VTY passwords.
- Enable login on VTY lines.
- Configure transport protocols (SSH and/or Telnet).
- (Optional) Set domain name and generate RSA keys for SSH.

### 4. Configure VLANs and Switches
- Assign the appropriate VLAN to each switch port connected to a PC or server.
- Ensure each access port is in the correct VLAN.
- No trunking is required in this topology.

### 5. Test Connectivity
- Use `ping` to verify that each PC can reach each server.
- Confirm that dynamic routes are visible in each router’s routing table.
- Verify Telnet/SSH access to each router is functional.

## Project Files

- `.pkt` file containing the full Packet Tracer simulation.
--
## Additional Information

- All routers have **hw6** enable password.