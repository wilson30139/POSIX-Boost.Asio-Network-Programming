# Multi Server

## [Course](https://timetable.nycu.edu.tw/?r=main/crsoutline&Acy=112&Sem=2&CrsNo=535603&lang=en-us)
- Name: Network Programming
- Instructor: Professor I-Chen Wu

## Introduction
This repository contains a collection of C++ network programming projects developed using POSIX system calls and Boost.Asio. It focuses on fundamental networking concepts, including process management, concurrent server design, socket programming, inter-process communication, and asynchronous I/O.<br><br>
The projects demonstrate the implementation of Unix-like shells, multi-user remote working servers, HTTP servers with CGI programs, and SOCKS 4 proxy servers. Together, they showcase the design and development of scalable network applications using POSIX APIs and the Boost.Asio networking library.

## Technologies
- C++
- POSIX System Calls
- Boost.Asio
- TCP/IP Socket Programming
- Process Management
- Multi-threading
- Multi-processing
- Inter-Process Communication (IPC)
- CGI
- HTTP
- SOCKS 4
- Linux

## Overview
| Project | Topic | Category |
|--------|------|--------|
| [Project 1](#project-1-npshell) | NPShell | Shell |
| [Project 2](#project-2-remote-working-ground-server) | Remote Working Ground Server | Concurrent Server |
| [Project 3](#project-3-http-server-and-cgi-programs) | HTTP Server and CGI Programs | Web Server |
| [Project 4](#project-4-socks-4) | SOCKS 4 | Proxy Server |

## [Project 1: NPShell](https://github.com/wilson30139/POSIX-Boost.Asio-Multi-Server/tree/main/Project%201)
- Implemented a Unix-like shell using C++.
- Managed processes through POSIX system calls.
- Implemented inter-process communication (IPC) using pipes.
- Supported shell command execution and process control.
- Demonstrated fundamental POSIX system programming concepts.

## [Project 2: Remote Working Ground Server](https://github.com/wilson30139/POSIX-Boost.Asio-Multi-Server/tree/main/Project%202)
- Implemented three server architectures for remote shell services.
- Supported single-user, multi-threaded, and multi-process server models.
- Demonstrated concurrent server design using threads and processes.
- Implemented inter-process communication using FIFO and shared memory.
- Supported user pipes, broadcast messages, and multi-user interaction.
- `np_simple.cpp`
  - Supports a single user connected to the remote server.
- `np_single_proc.cpp`
  - Supports multiple users using a single process with multi-threading.
- `np_multi_proc.cpp`
  - Supports multiple users using multiple server processes.
  - Implements IPC using FIFO and shared memory.

## [Project 3: HTTP Server and CGI Programs](https://github.com/wilson30139/POSIX-Boost.Asio-Multi-Server/tree/main/Project%203)
### Part 1 (Linux Environment)
- Implemented an HTTP server capable of processing client requests.
- Executed CGI programs and generated dynamic web pages.
- `http_server.cpp`
  - Accepts and parses HTTP requests.
  - Executes the corresponding CGI program.
- `console.cpp`
  - Implements the CGI program.
  - Processes requests from the HTTP server and generates dynamic HTML responses.
### Part 2 (Windows Environment)
- Combined the HTTP server and CGI functionality into a single server application.
- `cgi_server.cpp`
  - Integrates both HTTP server and CGI functionalities into a single application.

## [Project 4: SOCKS 4](https://github.com/wilson30139/POSIX-Boost.Asio-Multi-Server/tree/main/Project%204)
### Part 1: CONNECT Operation
- Implemented the SOCKS 4 CONNECT operation.
- Parsed SOCKS requests and established connections to destination servers.
- Applied firewall rules to accept or reject client requests.
### Part 2: BIND Operation
- Implemented the SOCKS 4 BIND operation for Active Mode FTP.
- Supported FTP data connections and large file transfers.
### Part 3: CGI Proxy Client
- Extended the CGI program from Project 3 to operate as a SOCKS 4 client.
- Connected to multiple remote shell servers through the SOCKS proxy.
- Displayed multiple remote session outputs through a web-based interface.
### Files
- `socks_server.cpp`
  - Implements the SOCKS 4 proxy server.
  - Supports both CONNECT and BIND operations.
  - Parses SOCKS requests and forwards client connections.
- `console.cpp`
  - Implements the CGI proxy client.
  - Connects to multiple remote shell servers through the SOCKS proxy.
  - Displays outputs of multiple remote sessions in a web interface.

## Learning Outcomes
Through these projects, I gained hands-on experience in:
- POSIX system programming
- TCP/IP socket programming
- Process management
- Concurrent server architecture
- Multi-threading and multi-processing
- Inter-process communication (FIFO, Pipe, Shared Memory)
- HTTP server and CGI programming
- SOCKS 4 proxy implementation
- Asynchronous network programming with Boost.Asio
