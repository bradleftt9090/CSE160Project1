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
# Introduction
TODO: ADD THIS SECTION

# General Informatoin
## Data Structures
There are two data structures included into the project design to help with the
assignment. See dataStructures/interfaces/ for the header information of these
structures.

* **Hashmap** - This is for anything that needs to retrieve a value based on a key.

* **List** - The list is design to have pushfront, pushback capabilities. For the most part,
you can stick with an array or even a QueueC (FIFO) which are more robust.

## General Libraries
/lib/interfaces

* **CommandHandler** - CommandHandler is what interfaces with TOSSIM. Commands are
sent to this function, and based on the parameters passed, an event is fired.
* **SimpleSend** - This is a wrapper of the lower level sender in TinyOS. The features
included is a basic queuing mechanism and some small delays to prevent collisions. Do
not change the delays. You can duplicate SimpleSendC to use a different AM type or
possibly rewire it.
* **Transport** - There is only the interface of Transport included. The actual
implementation of the Transport layer is left to the student as an exercise. For
CSE160 this will be Project 3 so don't worry about it now.

## Noise
/noise/

This is the "noise" of the network. A heavy noised network will cause issues with
packet loss.

* **no_noise.txt** - There should be no packet loss using this model.

## Topography
/topo/

This folder contains a few example topographies of the network and how they are
connected to each other. Be sure to try additional networks when testing your code
since additional ones will be added when grading.

* **long_line.topo** - this topography is a line of 19 motes that have bidirectional
links.
* **topo.txt** - A slightly more complex connection

# Running Simulations
TODO: ADD THIS SECTION
