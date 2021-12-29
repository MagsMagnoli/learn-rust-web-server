# Learn Rust Web Server

Building a simple web server following the [Rust guide](https://doc.rust-lang.org/book/ch20-00-final-project-a-web-server.html)

## Learnings

- TCP and HTTP main protocols in web servers
- TCP is lower-level and describes how information gets from one server to another but not what
- HTTP built on top of TCP and defines content of requests and responses
- Rust has `std::net` module that can listen for TCP connection
- Using `FnOnce` for closure with `'static` lifetime
- `cargo doc --open` launches docs of codebase
- use `Vec::with_capacity(size);` to create `Vec` with size. `Vec::new` dynamically sizes while items are added
- use `Arc<Mutex<T>>` for sharing ownership across threads and allowing mutation
  - `Arc` lets multiple receivers own receiver
  - `Mutex` ensures one worker gets a job at a time
- with `let` any temp values in expression are dropped when statement ends
  - `while let`, `if let`, and `match` don't drop until block ends. this means long running inner code can hold up locks above
