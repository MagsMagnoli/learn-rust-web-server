# Learn Rust Web Server

Building a simple web server following the [Rust guide](https://doc.rust-lang.org/book/ch20-00-final-project-a-web-server.html)

## Learnings

- TCP and HTTP main protocols in web servers
- TCP is lower-level and describes how information gets from one server to another but not what
- HTTP built on top of TCP and defines content of requests and responses
- Rust has `std::net` module that can listen for TCP connection