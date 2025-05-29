# Merkle Madness

## Index
1. [Visual_Project_Description](#visual-project-descritipon)
1. [Project Overview](#project-overview)
2. [Project Summary](#project-summary)
3. [Project Details](#project-details)
4. [Key Methods and Responsibilities](#key-methods-and-responsibilities)

## Visual Project Descritipon:

![blockchain](https://github.com/NoahBakayou/MerkleConquestCS294/assets/100172278/69067d51-e6bf-457d-8ebf-99ce73337b4b)
![blockchain2](https://github.com/NoahBakayou/MerkleConquestCS294/assets/100172278/76f98085-ecc4-47de-bd29-321a93543524)

## Project Overview

This collaborative project provides hands-on coding experience with multithreading and Merkle roots. It serves as an opportunity to reinforce essential skills related to SHA256 Hashing, Merkle trees, and Multithreading.

## Project Summary

The project introduces a console application that combines multithreading and Merkle roots in a simple game. Here's an overview of how the game works:

1. **User Input**: The user starts by entering the Merkle root of four words they intend to provide to the Merkle thread. The Merkle root can be manually calculated using a provided method or an online tool.

2. **Multithreading**: The application employs multithreading, allowing the user to submit strings on the main thread. Each submitted string is grabbed by either a Merkle or Rogue background thread, depending on the timing of the user.

3. **Merkle Thread**: If the Merkle thread successfully gathers four words, it creates a Merkle tree and generates a Merkle root string. If this root matches the initially entered Merkle root, the user wins the game. Otherwise, they lose.

4. **Random Delays**: Both background threads introduce an element of randomness by sleeping for a random number of seconds. This challenge requires the user to time their submissions correctly to ensure the Merkle thread grabs the words.

5. **Monitor Thread**: A third Monitor thread in the background constantly checks the progress and terminates the application once the user to time their submissions correctly to ensure the Merkle thread grabs the words.
  
6. **Miner**:
Handles Proof of Work. The doProofOfWork method finds a nonce that produces a hash with leading zeros based on block difficulty. If another miner finishes first (bAbortPoW is true), it aborts and returns false.
7. **Block**:
Stores transactions and computes the Merkle root. The 90% version handles 2 or 4 items; the full version supports any power of 2. populateMerkleNode sets child nodes and their hash.
8. **BlockchainUtil**:
Provides the generateHash method, which returns the SHA-256 hash of a string. Used for block and Merkle tree hashing.
9. **P2PMessageQueue**:
Manages a queue for P2P messages with methods to add (enqueue), remove (dequeue), and check for messages (hasNodes).
10. **P2PUtil**:
Sends one-time messages over sockets. The connectForOneMessage method connects, sends a message, receives a reply, and disconnects.
