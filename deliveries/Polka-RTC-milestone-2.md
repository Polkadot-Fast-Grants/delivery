# Milestone Delivery 📬

**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**

* **Application Document:** [Polka RTC](https://github.com/Polkadot-Fast-Grants/apply/blob/master/applications/polka_RTC.md)
* **Milestone Number:** 2
* **DOT Payment Address:** `1UGiZSCpf96g5uT7FdyC8SNhNgSWerv1ky7zBdeyyrJLHtS`

**Context** (optional)

Milestone 2 delivers the recording pipeline, decentralized storage, and blockchain integration for the proctoring system. The GStreamer-based recording infrastructure captures RTP streams and converts them to WebM format. Completed recordings are uploaded to IPFS for distributed storage, returning Content Identifiers (CIDs) for verification. A Solidity smart contract stores all proctoring session events on-chain including room creation, participant join/leave, ID verification, suspicious activity reports, recording metadata with IPFS CIDs, and exam results. The frontend integrates wallet connectivity (via Reown/WalletConnect) for on-chain interaction, allowing proctors and students to query their exam history and recordings directly from the blockchain.

**Deliverables**

| Number | Deliverable | Link | Notes |
|--------|-------------|------|-------|
| 0a. | License | [SFU-Backend](https://github.com/DDPidhi/sfu-server/blob/main/LICENSE) <br> [SFU-UI](https://github.com/DDPidhi/sfu-ui/blob/main/LICENSE) | MIT License |
| 0b. | Documentation | [Backend README](https://github.com/DDPidhi/sfu-server/blob/main/README.md) <br> [Frontend README](https://github.com/DDPidhi/sfu-ui/blob/main/README.md) <br> [CLI Guide](https://github.com/DDPidhi/sfu-server/blob/main/CLI_GUIDE.md) | Comprehensive documentation including setup instructions, configuration options, WebSocket protocol reference, and CLI validation guide. Includes inline code documentation. |
| 0c. | Testing and Testing Guide | [Integration Tests](https://github.com/DDPidhi/sfu-server/blob/main/tests/integration_test.rs) <br> [Frontend Tests](https://github.com/DDPidhi/sfu-ui/tree/main/src) <br> [CLI Validation](https://github.com/DDPidhi/sfu-server/blob/main/CLI_GUIDE.md) | Unit and integration tests for signaling, peer routing, IPFS upload, and blockchain integration. CLI tool provides validation scenarios for SFU server, IPFS connectivity, and blockchain operations. Run `make test` (Docker) or `cargo test` (local) for backend, `npm test` for frontend. |
| 0d. | Docker | [Dockerfile](https://github.com/DDPidhi/sfu-server/blob/main/Dockerfile) <br> [docker-compose.yml](https://github.com/DDPidhi/sfu-server/blob/main/docker-compose.yml) | Dockerized deployment with pre-configured GStreamer and IPFS dependencies. Run `make up` to start all services. |
| 1. | Recording Pipeline (GStreamer) | [Recording Module](https://github.com/DDPidhi/sfu-server/tree/main/src/recording) | GStreamer-based recording infrastructure that captures RTP streams from WebRTC peers and converts to WebM format. Supports per-participant recording with start/stop controls via WebSocket API. |
| 2. | IPFS Integration | [IPFS Module](https://github.com/DDPidhi/sfu-server/tree/main/src/ipfs) | Automatic upload of completed recordings to IPFS. Returns CID (Content Identifier) for each recording, enabling decentralized storage and verification. Configurable via environment variables. |
| 3. | Blockchain Integration | [Substrate Module](https://github.com/DDPidhi/sfu-server/tree/main/src/substrate) <br> [Smart Contract](https://github.com/DDPidhi/sfu-server/tree/main/contracts/proctoring) | Solidity smart contract for EVM-compatible chains. Records all proctoring events on-chain: room creation, participant join/leave, ID verification, suspicious activity, recording start/stop with IPFS CIDs, and exam results. |
| 4. | Event Logging System | [Smart Contract Events](https://github.com/DDPidhi/sfu-server/blob/main/contracts/proctoring/contracts/Proctoring.sol) | Comprehensive event logging for participant actions including join, leave (normal/kicked/disconnected), reconnect, ID verification status, suspicious activity reports (tab switch, window blur, multiple devices, etc.), and exam result submissions. |
| 5. | Frontend Wallet Integration | [Wallet Provider](https://github.com/DDPidhi/sfu-ui/blob/main/src/providers/WalletProvider.tsx) <br> [Contract Config](https://github.com/DDPidhi/sfu-ui/blob/main/src/config/contract.ts) <br> [Exam History Hook](https://github.com/DDPidhi/sfu-ui/blob/main/src/hooks/useExamHistory.ts) | React frontend with Reown (WalletConnect) integration for wallet connectivity. Students and proctors can view their exam history and recording CIDs directly from the blockchain. |

**Additional Information**

**Repositories:**
- Backend: https://github.com/DDPidhi/sfu-server
- Frontend: https://github.com/DDPidhi/sfu-ui

**Smart Contract:**
- The Solidity smart contract is EVM-compatible and can be deployed to any EVM chain
- Contract source: [contracts/proctoring](https://github.com/DDPidhi/sfu-server/tree/main/contracts/proctoring)

**Quick Start (Docker):**
```bash
# Backend
cd sfu-server
make up

# Frontend
cd sfu-ui
npm install && npm run dev
```

**CLI Validation:**
```bash
make cli-validate          # Run all validation tests
make cli-validate-sfu      # SFU server tests
make cli-validate-ipfs     # IPFS connectivity tests
make cli-validate-blockchain  # Blockchain integration tests
```