# university-project-computer-networks
# Computer Networks Project Requirements - Code Babes Team

The project will consist of a client-server application using sockets or remote method invocation, implemented in a programming language of choice (C#, Java, C++/C, etc.). It can be completed individually or in teams of up to three people and will be presented on a computer during the last seminar session, on a topic chosen from the list below:

# Distributed processing:

- The server listens for packets on the loopback address of the subnet on a specific port and maintains a list of all active clients.
- Clients, upon starting, send a packet to the server's loopback address and port to register themselves in the active clients list.
- Each client application opens a port to await processing requests, communicating this port to the server upon registration.
- Before closing, the client sends a message to the server’s loopback address and port to remove itself from the active clients list.
- The server listens on a port for processing requests from clients, consisting of executing a custom task provided at the time of the request, along with the necessary arguments. The result returned by the server is the exit code of the task's execution.
- Upon receiving a processing task, the server selects the next available client in line, sends the binary code of the task and its arguments to the client's processing port. The client executes the task locally with the provided arguments and returns the task's exit code to the server, which is then forwarded to the client that originally requested the task execution.
