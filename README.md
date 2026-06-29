## Course
- Name: Network Programming
- Instructor: I-Chen Wu Professor

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
- Part 1 (Linux Environment)
  - `http_server.cpp`
    - Accepts HTTP requests from clients.
    - Parses incoming HTTP requests.
    - Executes and returns the corresponding CGI program based on the requested resource.
  - `console.cpp`
    - Implements the CGI program.
    - Processes request forwarded by the HTTP server.
    - Executes CGI logic and generates dynamic HTML responses.
- Part 2 (Windows Environment)
  - `cgi_server.cpp`
    - Integrates the functionalities of both `http_server.cpp` and `console.cpp` into a single application.
    - Handle HTTP request processing, CGI execution, and response generation within one server program.

## Project 4: SOCK 4
- SOCKS 4 is a proxy protocol for relaying TCP connections.
- It forwards traffic between clients and destination servers through a SOCKS proxy server.
- It hides the client's IP address from the destination server.
- It supports access control based on predefined firewall rules.
- It is commonly used in proxy and firewall environments.
