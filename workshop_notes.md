
# Workshop exercises 
You can try out each of the three clients by following the instructions in each subsection of this document. 

### Downloading / building Nym client binaries 
If you're using a Debian-based OS or MacOSX you can grab binaries that _should_ work from the [releases page](https://github.com/nymtech/nym/releases/tag/nym-binaries-1.0.2). Make sure to grab the `v1.0.2` binaries. 

Otherwise, you'll have to build the monorepo yourself, by following the instructions [here](https://docs.nymtech.net/docs/stable/run-nym-nodes/build-nym). 

Once you have the client binaries compiled for your system, select which client you'd like to try out. 

### Socks5 Client ('no code')
This is the easiest client to start playing around with the mixnet, as you don't need to change any code in your app, simply point an application that can communicate via the SOCKS5 proxy protocol at `localhost 1080` and start sending traffic through the mixnet.  

* Use the [quickstart docs](https://docs.nymtech.net/docs/stable/quickstart/socks5) to get started. 
* Now try changing the proxy settings in a desktop application to use your running `nym-socks5-client` - point it towards `localhost:1080`.  

### Websocket Client (JSON or Binary data) - send yourself messages through the mixnet 
As long as you can send and receive messages from a websocket connection, you can use this client for your application. 

We have example code in Rust, Go, Python, and Javascript [here](https://github.com/nymtech/nym/tree/release/v1.1.0/clients/native/examples). 

You can try these out by: 
* Starting a Websocket client process according to instructions [here](https://docs.nymtech.net/docs/stable/integrations/websocket-client)
* Running one of the pieces of example code

> If you want to run the Rust examples, use `cargo run --example <rust_file>` from the `examples` directory. The Rust example code isn't in its own directory as its already _in_ a Cargo project

### WebAssembly (wasm) Client - send messages to yourself or someone else through the mixnet 
The WebAssembly client is in the process of being rewritten as a Typescript SDK - but you get a sneak peak today. 

> In order to use the WebAssembly example, you need to build the Nym monorepo at the unreleased `v1.1.1` tag. Check out to [this](https://github.com/nymtech/nym/tree/release/v1.1.1) branch and build the repository with `cargo build --release`

You can read about the WebAssembly client [here](https://github.com/nymtech/nym/tree/release/v1.1.1/sdk/typescript/examples/plain-html), and you can try sending me a message with this deployed example [here](https://chat-demo.nymtech.net/).  



