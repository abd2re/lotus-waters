---
tags: []
---
# Internet
- Individual nodes (computers) in the internet are called:: hosts.
<!--SR:!2024-12-17,19,250-->
- Hosts are collected into:: networks on different scales: household, corporate, regional, national.
<!--SR:!2024-12-21,22,250-->
- Networks can be joined with:: other networks: this is inter-networking.
<!--SR:!2024-12-09,14,230-->
- “The Internet” is:: a massive, worldwide system of internetworked hosts.
<!--SR:!2024-12-04,9,210-->

## Network organization

The two types of networking organizations $\rightarrow$
?
![[image-20241114083547422.png]]
<!--SR:!2024-12-08,13,230-->

- The World Wide Web (sometimes called “the internet” by abuse of terminology) uses a:: client-server architecture.
<!--SR:!2024-12-09,13,230-->
- A web browser (client) sends:: a request to a web server to create or retrieve a resource.
<!--SR:!2024-12-16,19,250-->


### Packet switching
- Data to transmit is split into:: fixed-size bundles called packets equipped with metadata.
<!--SR:!2024-12-24,24,250-->
- The metadata includes:: source and destination addresses to identify where the packet came from and where it needs to go.
<!--SR:!2024-12-24,25,250-->
- Intermediary devices (such as routers) use the headers to:: forward the packet until it reaches its destination.
<!--SR:!2024-12-04,10,230-->



Circuit switching vs packet switching:
?
![[image-20241114084428055.png]]
<!--SR:!2024-12-21,19,230-->


### 4-layer, TCP/IP model

They are:
?
- Link. Network hardware handles this layer. Physically transmit data from one device to another with a cable or radio
- Network. This is where the packets come in. The OS handles this layer. Implement packet-switching and route of packets across multiple nodes.
- Transport. An abstraction on top of packets. Applications are programmed against this layer. Identify a particular application on a host, (TCP only:) provide a reliable data stream
- Application. What we actually want to do with the network. All the examples we discussed previously are applications. Play games, retrieve web pages, send email, etc.
<!--SR:!2024-12-09,6,150-->

## Network layer
Each node (a host or a router) in the internet is assigned:: an IP address (4 byte integer).
<!--SR:!2024-12-16,18,250-->

- Routers are:: intermediary devices
<!--SR:!2024-12-04,8,190-->
- Routers use a data structure called:: a routing table that expresses, for a given range of destination addresses, where a packet should be sent next.
<!--SR:!2024-12-15,13,210-->

IP is unreliable. It does not guarantee message delivery, for example:: messages could be lost or corrupted in transit, or messages could arrive out-of-order at their destination.
<!--SR:!2024-12-12,14,230-->

A transport-layer protocol accounts:: for these deficiencies of IP.
<!--SR:!2024-12-10,10,210-->

Designed to work on top of IP, TCP has these characteristics (3):
?
- Connection-oriented. Endpoints wanting to communicate first establish a connection, by a special back-and-forth exchange of IP packets.
- Stream abstraction. Connected endpoints communicate by sending a stream of bytes. Applications using TCP do not worry about breaking up their data into packets.
- Reliability. Acknowledgement messages confirm receipt of data. Data loss or corruption are detected and packets are re-sent automatically as needed
<!--SR:!2024-12-04,1,130-->

TCP is implemented by:: the OS.
<!--SR:!2024-12-08,12,230-->

- TCP establishes a connection between two parties. One is designated:: as a server and one is designated as a client.
<!--SR:!2024-12-13,10,210-->

A TCP connection is established following this procedure (3):
?
1. The server starts listening for incoming connections.
2. A client requests to connect to a listening server.
3. The server accepts (or rejects) the incoming connection. (three-way handshake)
<!--SR:!2024-12-08,9,190-->

In TCP and UDP, the port number identifies:: the specific application or service on a host device, enabling the correct routing of data to the intended process.
<!--SR:!2024-12-09,14,240-->

UDP guarantees:: only best-effort delivery, meaning it ensures that data is sent but does not guarantee its delivery, order, or integrity.
<!--SR:!2024-12-06,4,160-->

Explain the trade offs of TCP versus UDP
?
TCP provides reliable, ordered, and error-checked data transmission at the cost of higher latency and overhead, while UDP offers faster, connectionless communication with lower overhead but no guarantees of delivery, order, or error checking.
<!--SR:!2024-12-06,6,180-->

