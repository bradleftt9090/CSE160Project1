# CSE 160 Project 1 - Flooding and Neighbor Discovery
TinyOS/NesC implementation of flooding and neighbor discovery for multi-hop wireless network simulation.

The goal of this project is to extend the TinyOS skeleton code to support:

- **Flooding:** Each node rebroadcasts received packets to neighbors, enabling multi-hop message delivery across the network. Packets must behave like pings and ping replies, without circulating indefinitely (using sequence numbers, source addresses, and TTL).  
- **Neighbor Discovery:** Each node discovers and maintains a list of its neighbors dynamically, even accounting for nodes leaving the network. Neighbor discovery is implemented without introducing new packet types, using existing ping, ping reply, flooding, and timers.

---

## 🔧 Features
- TinyOS NesC implementation of flooding and neighbor discovery.  
- Debug channels (`FLOODING_CHANNEL` and `NEIGHBOR_CHANNEL`) for verifying message flow and neighbor tracking.  
- Simulation with TOSSIM using the command:  
  ```bash
  make micaz sim
