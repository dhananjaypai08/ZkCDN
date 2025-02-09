# ZkCDN
A Dapp that enables secure content distribution using Zero-Knowledge Proofs (ZKPs), Soulbound Tokens (SBTs), and Internet Computer Protocol (ICP) for verifiable, privacy-preserving access control.

## Deployment 
- Smart Contract on Bitfinity : [ZKDNS Contract Link](https://explorer.testnet.bitfinity.network/address/0x110f4C328A3BcBEB68ce9dCF58479A8cB9A08e72)

## 📌 Problem Statement
Current content distribution mechanisms lack privacy and security, exposing user metadata, server locations, and content access patterns. Additionally, traditional CDNs and P2P solutions are vulnerable to VPN-based attacks, making location-based optimizations unreliable. We address these issues by integrating:

- **Zero-Knowledge Proofs (ZKPs):** Users prove they are authorized to access content without revealing sensitive information.
- **Soulbound Tokens (SBTs):** Content access rights are non-transferable and tied to users’ decentralized identities.
- **Proof of Location & Proof of Internet Geometry:** To verify user proximity to the nearest node securely.
- **DJB2 Hashing Algorithm:** Ensures content integrity and efficient lookups.

## 🚀 Solution Overview
Users upload content hashed using the DJB2 algorithm along with a zkProof, ensuring integrity and access control. To fetch content, users provide a unique integer derived from DJB2 hashing. The system:
1. **Verifies zkProof of location.**
2. **Identifies the nearest node using Proof of Internet Geometry.**
3. **Pings the server to detect VPN-based attacks.**
4. **Retrieves and serves the content without revealing location metadata.**

## 🛠 Tech Stack
- **Blockchain Layer:** ICP (Bitfinity testnet)
- **ZKPs:** Circom, SnarkJS
- **Frontend:** React.js, Tailwind CSS
- **Backend & Storage:** Canisters on ICP
- **Security & Access Control:** Soulbound Tokens (SBTs), Proof of Location
- **Content Integrity:** DJB2 Hashing Algorithm

## 🔄 Technical Breakdown
1. **User Uploads Content:**
   - The content is hashed using the **DJB2 algorithm**.
   - A **ZK proof of ownership** is generated via Circom & SnarkJS.
   - Content is stored on ICP’s decentralized storage.
   - An **SBT is minted** to represent access rights.

2. **User Requests Content:**
   - Provides a **unique integer** (DJB2 hash output).
   - Generates a **zkProof of location**.
   - Nearest node verification using **Proof of Internet Geometry**.
   - The server is pinged to **detect VPN-based attacks**.

3. **Content Retrieval & Privacy Preservation:**
   - Content is served from the nearest verified node.
   - User is unaware of the exact content source.
   - zkProof ensures privacy and integrity throughout.


## 💡 Innovations & Features
- **Privacy-Preserving Access:** No metadata leaks during content retrieval.
- **Decentralized Proof-of-Location:** Prevents VPN-based location spoofing.
- **Immutable Content Integrity:** DJB2 hashing ensures content validity.
- **Soulbound Content Ownership:** Access is permanently tied to a user’s identity.
- **Optimized Content Delivery:** Proof of Internet Geometry finds the nearest node.

## 🎯 Future Enhancements
- Integration with **ICP’s Internet Identity** for seamless authentication.
- **Multi-layer zkProofs** to further enhance privacy.
- **AI-driven Content Recommendation System** based on user access patterns.
- **NFT-based Content Licensing** to allow tokenized ownership.

## 🔗 Conclusion
This DApp revolutionizes content distribution by **ensuring privacy, security, and decentralization**. By leveraging **ICP, ZKPs, and Proof of Internet Geometry**, we eliminate traditional vulnerabilities and enable a truly trustless, censorship-resistant content network.

---
**Built on ICP | Powered by ZKPs | Secured with SBTs**

