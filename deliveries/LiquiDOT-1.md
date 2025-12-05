# Milestone Delivery 📬


**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**  

* **Application Document:** Link to our merged application [application](https://github.com/Polkadot-Fast-Grants/apply/pull/86)

* **Milestone Number:** 1
* **DOT Payment Address:** 12Wi7yFMuNVoQjz8SnLdZDa8MT5jPVd49WxEnwv8A3SSDKAA (Polkadot Asset Hub wallet address)

**Context** 
This milestone focuses on delivering and proving the core smart-contract layer that powers LiquiDOT’s cross‑chain LP automation. We implemented and documented two production contracts: the Asset Hub Vault (custody, accounting, XCM orchestration on Asset Hub) and the XCM Proxy (DEX execution, LP mint/burn and liquidations on Moonbeam). The code ships with a testnet-first workflow, deployment artifacts, and a comprehensive testing guide so reviewers can reproduce the flows end‑to‑end. The primary product documentation lives in GitBook.

**Deliverables**

| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 0a. | License (Apache-2.0) | https://github.com/gabikreal1/LiquiDOT/blob/main/LICENSE | SPDX: Apache-2.0 as specified in the application. |
| 0b. | Documentation | https://liquidot.gitbook.io/liquidot-docs | All of the necessary docs are in GitBook. Smart Contracts README: https://github.com/gabikreal1/LiquiDOT/blob/main/SmartContracts/README.md |
| 0c. | Testing and Testing Guide | https://github.com/gabikreal1/LiquiDOT/blob/main/SmartContracts/test/README.md | Testnet-first suites for AssetHubVault, XCMProxy, and Integration.|
| 0d. | Article / Build-in-public | Thread on X: https://x.com/LiquiDOT_LDN/status/1982151106797957511 | Ongoing article thread on X (will continue as a series). We’ll mirror a recap on GitBook; public build updates continue on X. |
| 1. | Core Contracts (Asset Hub Vault + XCM Proxy) | Contracts: AssetHubVault.sol https://github.com/gabikreal1/LiquiDOT/blob/main/SmartContracts/contracts/V1%28Current%29/AssetHubVault.sol · XCMProxy.sol https://github.com/gabikreal1/LiquiDOT/blob/main/SmartContracts/contracts/V1%28Current%29/XCMProxy.sol | Deployments (testnet) AssetHubVault (Paseo Asset Hub) 0x67E5293e374219C515bD9838B23C792C555e51D4 · XCMProxy (Moonbase Alpha) 0xf935e063b2108cc064bB356107ac01Dc90f96652. Explorers: Moonbase Moonscan https://moonbase.moonscan.io/address/0xf935e063b2108cc064bB356107ac01Dc90f96652 · Paseo Asset Hub Blockscout https://blockscout-passet-hub.parity-testnet.parity.io/address/0x67E5293e374219C515bD9838B23C792C555e51D4?tab=index. Tests: AssetHubVault https://github.com/gabikreal1/LiquiDOT/tree/main/SmartContracts/test/AssetHubVault/testnet · XCMProxy https://github.com/gabikreal1/LiquiDOT/tree/main/SmartContracts/test/XCMProxy/testnet |

**Additional Information**
• Primary documentation lives in GitBook (as requested): https://liquidot.gitbook.io/liquidot-docs

• Links reference the latest code on the `main` branch. If you prefer a frozen snapshot for review, we can cut a tag (e.g., `m1-delivery`) and update links accordingly.

• Networks used for testing: Moonbase Alpha (ChainId 1287) and Paseo Asset Hub (ParaId 1000). Deployment artifacts under `SmartContracts/deployments/` include addresses and configuration used by the tests.

• Testnet infrastructure note: At delivery time, full end-to-end EVM↔EVM XCM on Paseo was constrained. While Paseo Asset Hub EVM exposes the required XCM precompiles, there wasn’t a second Paseo EVM chain with XCM precompiles to receive/execute the other side. Accordingly, we validated contract logic and cross-contract flows on Moonbase and used safe test‑mode paths on Asset Hub where direct XCM could not be exercised. Once a second EVM chain with XCM precompiles is available on Paseo (or Kusama Asset Hub precompiles land), we will re‑run and publish complete E2E XCM runs and update the docs.

