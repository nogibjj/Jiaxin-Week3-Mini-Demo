# Jiaxin-Week3-Mini-Demo
## Purpose
This is a mini demo to show how to use cargo-server in Rust.

## Benefits from using cargo-server in Rust:
* Private Crate Hosting: cargo-server provides a way to host private crates, allowing you to manage access to your code and dependencies.
* Testing and Development: With cargo-server, you can easily test and develop your packages without having to publish them to a public registry like crates.io. This is especially useful when you're developing an experimental feature and don't want to make it public yet.
* Local Cache: cargo-server caches packages locally, reducing the time it takes to download dependencies during build. This can be especially useful in CI/CD environments where builds are run frequently.
* Network Isolation: cargo-server provides a way to isolate a build environment from the internet, which can be useful in security-sensitive or low-bandwidth environments.
* Easy Deployment: Deploying a cargo-server registry is simple and can be done with a single command, making it accessible for small teams and personal projects.

## Install Rust on Terminal
1. Type: `curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`
2. To configure your current shell, run: `source "$HOME/.cargo/env"`
<img width="588" alt="Screen Shot 2023-02-01 at 3 31 00 PM" src="https://user-images.githubusercontent.com/112274822/216160331-f3634001-3bcb-4901-b1c1-ed2795985923.png">

## To use cargo-server in Rust
1. Install it by running the following command in your terminal:
```bash
cargo install cargo-server
```

2. After installing cargo-server, you can use this command inside the directory for your project. By default, it will create in port 8000:
<img width="476" alt="Screen Shot 2023-02-01 at 4 02 44 PM" src="https://user-images.githubusercontent.com/112274822/216162897-40fc89b9-591e-4317-a89a-1518e9abbce7.png">

3. After installing, you can run cargo server to start a local registry for your Rust packages. This can be useful for serving private crates, or for testing and development.

4. Here's an example of how you can use it to publish a package:

* Create a new Rust project using `cargo examples/simple-app`
* Change into the project directory using `cd`
* Publish the package to the local registry using `cargo server publish`
* Add the local registry as a source in your Cargo.toml file:

5. Using `—path`, you can also specify a special path:
* here is my example: `cargo server --quiet --open --path /workspaces/week-2-minn-repo-yjx/examples/simple-app`
<img width="146" alt="Screen Shot 2023-02-01 at 3 57 40 PM" src="https://user-images.githubusercontent.com/112274822/216162960-141e90ba-72f2-4ba8-ac0b-d4469d9fab04.png">

* The results are shown below:
<img width="839" alt="Screen Shot 2023-02-01 at 2 51 41 PM" src="https://user-images.githubusercontent.com/112274822/216162782-db6ffb3e-0b62-4df8-9111-fa2dd0b00e19.png">

