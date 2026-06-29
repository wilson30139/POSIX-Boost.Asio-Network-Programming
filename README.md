# [Course](https://timetable.nycu.edu.tw/?r=main/crsoutline&Acy=112&Sem=2&CrsNo=535603&lang=en-us)
- Name: Network Programming
- Instructor: I-Chen Wu Professor

# Introduction
This repository contains a collection of C++ network programming projects developed using POSIX system calls and Boost.Asio. It focuses on fundamental network programming conecepts, including process management, concurrent server design, socket programming, and asynchronous I/O.<br><br>
This repository includes projects covering Unix-like shell implementation, multi-user remote working servers, HTTP servers with CGI programs, and SOCKS 4 proxy servers. Together, these projects demonstrate the design and implementation of network applications using POSIX APIs and the Boost.Asio networking library.

# [Project 1: NPShell](https://github.com/wilson30139/POSIX-Boost.Asio-Multi-Server/tree/main/Project%201)
- NPShell is a Unix-like shell implemented in C++.
- It demonstrates process management using POSIX system calls.
- It implements inter-process communication (IPC) through pipe mechanisms.
- It supports the execution of shell commands and process control.
- It provides hands-on experience with POSIX system programming.

# [Project 2: Remote Working Ground Server](https://github.com/wilson30139/POSIX-Boost.Asio-Multi-Server/tree/main/Project%202)
- `np_simple.cpp` supports a single user connected to the remote server.
- `np_single_proc.cpp` allows multiple users to connect to the remote server through their own threads, while the server runs as a single process.
- `np_multi_proc.cpp` allows multiple users to connect to the remote server through their own processes, with each client handled by a separate server process.
- It demonstrates both multi-threaded and multi-process concurrent server architectures.
- It implements inter-process communication using FIFO and shared memory.
- It supports user pipes, broadcast messages, and multi-user interaction.

# [Project 3: HTTP Server and CGI Programs](https://github.com/wilson30139/POSIX-Boost.Asio-Multi-Server/tree/main/Project%203)
## Part 1 (Linux Environment)
- `http_server.cpp`
  - Accepts HTTP requests from clients.
  - Parses incoming HTTP requests.
  - Executes and returns the corresponding CGI program based on the requested resource.
- `console.cpp`
  - Implements the CGI program.
  - Processes request forwarded by the HTTP server.
  - Executes CGI logic and generates dynamic HTML responses.
## Part 2 (Windows Environment)
- `cgi_server.cpp`
  - Integrates the functionalities of both `http_server.cpp` and `console.cpp` into a single application.
  - Handle HTTP request processing, CGI execution, and response generation within one server program.

# [Project 4: SOCK 4](https://github.com/wilson30139/POSIX-Boost.Asio-Multi-Server/tree/main/Project%204)
## Part 1: SOCKS 4 CONNECT Operation
- Implements a SOCKS 4 proxy server supporting the CONNECT operation.
- Accepts client requests, parses the SOCKS 4 protocol, and establishes connections to destination servers.
- Applies firewall rules and returns Accept or Reject responses based on the connection request.
## Part 2: SOCKS 4 BIND Operation
- Implements the BIND operation required for Active Mode FTP.
- Establishes FTP data connections between clients and servers through the SOCKS proxy.
- Supports large file transfers through the SOCKS proxy.
## Part 3: CGI Proxy Client
- Extends the CGI program from Project 3 to operate as a SOCKS 4 client.
- Connects to mulitple remote shell servers through the SOCKS proxy using the CONNECT operation.
- Displays the outputs of multiple remote sessions simultaneously through a web-based interface.
## Files
- `socks_server.cpp`
  - Implements the SOCKS 4 proxy server.
  - Handles both CONNECT and BIND operations.
  - Parses SOCKS 4 requests, applies firewall rules, and forwards client connection to destination servers.
- `console.cpp`
  - Implements the CGI proxy client.
  - Parses CGI parameters, establishes connections to the SOCKS server, and communicates with multiple remote shell servers.
  - Collects and displays the outputs of multiple remote sessions through a web interface.
