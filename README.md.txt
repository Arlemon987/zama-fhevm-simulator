# Zama fhEVM Visual Simulator

![Zama Simulator Banner](logo.jpg)

## ⚡ Live Demo
[Click here to view the Simulator](https://zama-fhevm-simulator.vercel.app) *(Replace this link with your actual Vercel URL)*

## 📖 About
This project is an interactive web-based simulator designed to visualize the architecture and transaction flow of **Zama's fhEVM** (Fully Homomorphic Encryption Virtual Machine).

While standard blockchains process data in plaintext, fhEVM allows for computations on encrypted data. This simulator breaks down that complex process into understandable, animated steps, helping developers and students understand how **End-to-End Encryption** is achieved on-chain.

## 🚀 Key Features

* **Dual Modes:**
    * 🔴 **Public Mode:** Visualizes how standard EVM chains expose data (inputs and results are visible).
    * 🟡 **Zama Mode:** Visualizes the secure flow where data remains encrypted throughout computation.
* **Architectural Accuracy:** detailed visualization of the fhEVM ecosystem components based on the technical whitepaper:
    * **Relayers:** Handling gas and connectivity.
    * **Gateways:** Verifying ZK Proofs (ZKPoK).
    * **Coprocessors:** Performing off-chain FHE arithmetic.
    * **Threshold KMS:** Distributed Key Generation (DKG) and collaborative decryption.
    * **Oracles:** Bridging off-chain results back to the Host Chain.
* **Educational Insights:** Real-time logs and step-by-step explanations for every stage of the transaction lifecycle.
* **Responsive Design:** Fully optimized for both Desktop and Mobile viewing.

## 🛠️ How It Works
The simulator walks through the lifecycle of a confidential transaction:
1.  **Setup:** KMS performs Distributed Key Generation.
2.  **Input:** User encrypts data and generates ZK proofs.
3.  **Routing:** Relayers handle the transaction submission.
4.  **Verification:** Gateway validates proofs before execution.
5.  **Execution:** Host chain performs symbolic execution (Handles) while Coprocessors perform the actual math on ciphertexts.
6.  **Decryption:** A threshold protocol reassembles the private key to decrypt the specific result.
7.  **Callback:** An Oracle delivers the decrypted result back to the chain.

## 💻 Tech Stack
* HTML5
* CSS3 (Responsive Grid & Flexbox)
* Vanilla JavaScript (ES6+)
* SVG for dynamic vector graphics

## 📄 Disclaimer
This simulation is an educational tool based on the [Zama fhEVM Whitepaper](https://github.com/zama-ai/fhevm/blob/main/fhevm-whitepaper.pdf). It is intended for visualization purposes and may simplify certain cryptographic primitives for clarity.

---
*Built with ❤️ for the Privacy Community.*