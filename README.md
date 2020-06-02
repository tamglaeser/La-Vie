##_Conway's Game of Life_ in Rust and WebAssembly
This project is based on the tutorial from the Rust🦀 and WebAssembly🕸 [book](https://rustwasm.github.io/docs/book/), realizing _Conway's Game of Life_.

##Getting Started

####Prerequisites
This project requires the standard Rust toolchain (`rustup`, `rustc`, and `cargo`). If you do not have it or have an older version than
Rust 1.30, follow this [link](https://www.rust-lang.org/tools/install) to install it now.

Furthermore, you will also need [`wasm-pack`](https://rustwasm.github.io/wasm-pack/installer/) and 
[`npm`](https://www.npmjs.com/get-npm).
  
####Get the Sources
```
$ git clone https://github.com/tamglaeser/La-Vie.git
$ cd ./La-Vie
```
####Project Structure

```
$ tree -L 3 .
.
├── Cargo.toml
├── LICENSE_APACHE
├── LICENSE_MIT
├── README.md
├── src
│   ├── lib.rs
│   └── utils.rs
├── tests
│   └── web.rs
└── www
    ├── bootstrap.js
    ├── index.html
    ├── index.js
    ├── package.json
    ├── README.md
    └── webpack.config.js     
```

####Building the project
Execute the following command to build the core crate.
```
$ wasm-pack build
```
Next, run the following commands to install the Node.js dependencies and run the server.
```
$ cd ./www
$ npm install
$ npm run start
```
Assuming the client and server are on the same machine, navigate to http://localhost:8080/ on your Web browser and you should be able to see
the evolution of life!