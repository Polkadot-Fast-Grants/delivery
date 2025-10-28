# Milestone Delivery 📬

> ⚡ Only the GitHub account that submitted the application is allowed to submit milestones. 
> 
> Don't remove any of the mandatory parts presented in bold letters or as headlines! Lines starting with `>`, such as this one, can be removed.

**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**  

* **Application Document:** Link to our merged application [application](https://github.com/Polkadot-Fast-Grants/apply/pull/86)

* **Milestone Number:** 1
* **DOT Payment Address:** 12Wi7yFMuNVoQjz8SnLdZDa8MT5jPVd49WxEnwv8A3SSDKAA (Polkadot Asset Hub wallet address)

**Context** 
This milestone focuses on delivering and proving the core smart-contract layer that powers LiquiDOT’s cross‑chain LP automation. We implemented and documented two production contracts: the Asset Hub Vault (custody, accounting, XCM orchestration on Asset Hub) and the XCM Proxy (DEX execution, LP mint/burn and liquidations on Moonbeam). The code ships with a testnet-first workflow, deployment artifacts, and a comprehensive testing guide so reviewers can reproduce the flows end‑to‑end. The primary product documentation lives in GitBook.

**Deliverables**

| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 0a. | License (Apache-2.0) | https://github.com/gabikreal1/LiquiDOT/blob/101b662/LICENSE | SPDX: Apache-2.0 as specified in the application. |
| 0b. | Documentation | https://liquidot.gitbook.io/liquidot-docs | All of the necessary docs are in GitBook. Smart Contracts README: https://github.com/gabikreal1/LiquiDOT/blob/101b662/SmartContracts/README.md |
| 0c. | Testing and Testing Guide | https://github.com/gabikreal1/LiquiDOT/blob/101b662/SmartContracts/test/README.md | Testnet-first suites for AssetHubVault, XCMProxy, and Integration. Quick commands: https://github.com/gabikreal1/LiquiDOT/blob/101b662/SmartContracts/test/.test-commands.md · Helpers (wiring/diagnostics): https://github.com/gabikreal1/LiquiDOT/tree/101b662/SmartContracts/test/helpers |
| 0d. | Article / Build-in-public | Thread on X: https://x.com/LiquiDOT_LDN/status/1982151106797957511 | Ongoing article thread on X (will continue as a series). We’ll mirror a recap on GitBook; public build updates continue on X. |
| 1. | Core Contracts (Asset Hub Vault + XCM Proxy) | Contracts: AssetHubVault.sol https://github.com/gabikreal1/LiquiDOT/blob/101b662/SmartContracts/contracts/V1%28Current%29/AssetHubVault.sol · XCMProxy.sol https://github.com/gabikreal1/LiquiDOT/blob/101b662/SmartContracts/contracts/V1%28Current%29/XCMProxy.sol | Deployments (testnet) AssetHubVault (Paseo Asset Hub) 0x67E5293e374219C515bD9838B23C792C555e51D4 · XCMProxy (Moonbase Alpha) 0xf935e063b2108cc064bB356107ac01Dc90f96652. Tests: AssetHubVault https://github.com/gabikreal1/LiquiDOT/tree/101b662/SmartContracts/test/AssetHubVault/testnet · XCMProxy https://github.com/gabikreal1/LiquiDOT/tree/101b662/SmartContracts/test/XCMProxy/testnet  |

**Additional Information**
• Primary documentation lives in GitBook (as requested): https://liquidot.gitbook.io/liquidot-docs

• Commit used for permalinks in this delivery: 101b662 (repository root). If you prefer a tag for review, we can cut `m1-delivery-101b662` upon request and update links accordingly.

• Networks used for testing: Moonbase Alpha (ChainId 1287) and Paseo Asset Hub (ParaId 1000). Deployment artifacts under `SmartContracts/deployments/` include addresses and configuration used by the tests.

• Repro quickstart: follow SmartContracts Testing Guide (link above). Suites are idempotent and include helpers to wire contracts across chains, seed liquidity, and verify configuration.

• Article status (0d): The Milestone 1 recap article is being finalized in GitBook; we will add the exact link to this file and to the PR thread once published (within the program’s allowed fix window). For now, see the demo video and build-in-public thread linked above.
