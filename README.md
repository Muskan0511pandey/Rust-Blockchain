# Rust-Blockchain
Build a blockchain in Rust
To begin, run RUST_LOG=info cargo run to start the client locally. Note that the blockchain isn't persisted anywhere.

You can initiate multiple instances in separate terminals to establish interconnected peer-to-peer clients.

In each client terminal, you can execute the following commands:

ls p: Lists connected peers.
ls c: Prints the local blockchain.
create b $data: Creates (mines) a new block with the provided data entry $data and broadcasts it.
When a node generates a block, it broadcasts it across the network, updating the blockchain on all other nodes if the block is valid.

Upon startup, a node requests another node's blockchain. If valid and longer than its own, the node updates its chain accordingly.

This implementation is extremely simplified, operates offline, and is both inefficient and insecure. If a node becomes out of sync, it ceases to function. This example is solely for educational purposes, showcasing fundamental blockchain concepts in Rust. It should not be used in any production environment, but it's perfect for learning and experimentation. Enjoy exploring!
