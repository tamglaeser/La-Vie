  <h2><i>Conway's Game of Life</i> in Rust and WebAssembly</h1>

  <p>This project is based on the tutorial from the Rust🦀 and WebAssembly🕸 <a href="https://rustwasm.github.io/docs/book/">book</a>, realizing <i>Conway's Game of Life</i>. 
  
  <h3>Getting Started</h3>
  <h4>Prerequisites</h4>
  <p>This project requires the standard Rust toolchain (<code>rustup</code>, <code>rustc</code>, and <code>cargo</code>). If you do not have it or have an older version than
   Rust 1.30, follow this <a href="https://www.rust-lang.org/tools/install">link</a> to install it now.
   
   Furthermore, you will also need <code><a href="https://rustwasm.github.io/wasm-pack/installer/">wasm-pack</a></code>, <code>cargo-generate</code>, and 
   <code><a href="https://www.npmjs.com/get-npm">npm</a></code>. Use the following command to install cargo-generate.</p>
   ```
   cargo install cargo-generate
   ```
  
  <h4>Get the Sources</h4>
  
  
  ```
  $ git clone https://github.com/tamglaeser/La-Vie.git
  $ cd ./la-vie
  ```
  
  <h4>Running the project</h4>
  <p>Execute the following command in the root folder, <i>la-vie</i>, of the terminal to build the core crate.</p>
  
  ```
  $ wasm-pack build
  ```
  <p>Next, run the following commands in the <i>www/</i> subfolder of <i>la-vie</i> to install the dependencies and run the server, repsectively.</p>
  
  ```
  $ npm install
  npm run start
  ```
  <p>Assuming the client and server are on the same machine, navigate to http://localhost:8080/ on your Web browser and you should be able to see
   the evolution of life!</p>
   
   <h4>Project Structure</h4>
   
   ```
   /La-Vie$ tree -L 3 .
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