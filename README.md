# CSE160Project1
TinyOS/NesC implementation of flooding and neighbor discovery for multi-hop wireless network simulation (CSE 160 Project 1).

The goal of this project is to extend the TinyOS skeleton code to support:
Flooding: Each node rebroadcasts received packets to neighbors, enabling multi-hop message delivery across the network. Packets must behave like pings and ping replies, without circulating indefinitely (using sequence numbers, source addresses, and TTL).
Neighbor Discovery: Each node discovers and maintains a list of its neighbors dynamically, even accounting for nodes leaving the network. Neighbor discovery is implemented without introducing new packet types, using existing ping, ping reply, flooding, and timers.
🔧 Features
TinyOS NesC implementation of flooding and neighbor discovery.
Debug channels (FLOODING_CHANNEL and NEIGHBOR_CHANNEL) for verifying message flow and neighbor tracking.
Simulation with TOSSIM using the command: make micaz sim
Source code includes handling for packet rebroadcasting, sequence numbers, TTL, and periodic neighbor checks.
📚 Deliverables
Source code (.nc files + Makefile).
One-page design decisions document.
Short answers to project discussion questions (event-driven programming, flooding vs TTL, packet counts, alternative multi-hop methods, and design trade-offs).
🚀 Getting Started
Clone the repo into your TinyOS workspace:
  git clone https://github.com/<your-username>/CSE160-Project1-Flooding.git
  cd CSE160-Project1-Flooding
Build for simulation: make micaz sim
Run TOSSIM with the provided Python driver script.
