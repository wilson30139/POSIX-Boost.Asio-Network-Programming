## Course
- Name: Network Programming
- I-Chen Wu

## Project 1: NPShell
- NPShell is a Unix-like shell implemented in C++.
- It demonstrates process management using POSIX system calls.
- It implements inter-process communication (IPC) through pipe mechanisms.
- It supports the execution of shell commands and process control.
- It provides hands-on experience with POSIX system programming.

## Project 2: Remote Working Ground Server
- `np_simple.cpp` supports a single user connected to the remote server.
- `np_single_proc.cpp` allows multiple users to connect to the remote server through their own threads, while the server runs as a single process.
- `np_multi_proc.cpp` allows multiple users to connect to the remote server through their own processes, with each client handled by a separate server process.
- It demonstrates both multi-threaded and multi-process concurrent server architectures.
- It implements inter-process communication using FIFO and shared memory.
- It supports user pipes, broadcast messages, and multi-user interaction.

## Project 3: HTTP Server and CGI Programs
- HTTP Server and CGI Programs implementes an HTTP web server in C++.
- It processes HTTP requests and returns appropriate HTTP responses.
- It supports CGI (Common Gateway Interface) for generating dynamic web content.
- It uses TCP socket programming for client-server communication.
- It executes CGI programs using `fork()` and `exec()`.
- It demonstrates HTTP communication, process management, and web server implementation.

## Project 4: SOCK 4
- SOCKS 4 is a proxy protocol for relaying TCP connections.
- It forwards traffic between clients and destination servers through a SOCKS proxy server.
- It hides the client's IP address from the destination server.
- It supports access control based on predefined firewall rules.
- It is commonly used in proxy and firewall environments.
