**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**

* **Name of the grant project:** Polkadot API Playground  
* **Application Document:** [Polkadot API Playground Application](https://github.com/Polkadot-Fast-Grants/apply/pull/4)
* **Milestone Number:** 1
* **DOT Payment Address:** 13eJfzT8u1qKYkFDW6o7Ta19eGi9X8Y74cWLDComEVxbKGMa

## Context

This milestone delivers a developer-friendly, web-based interactive playground for learning and experimenting with the Polkadot API. It enables developers to write, test, and visualize Polkadot API code directly in the browser with real-time feedback, running against actual testnets. The playground provides a smooth learning curve for developers new to the Polkadot ecosystem while offering advanced features for experienced developers.


## Pre Deliverables

| Number | Deliverable | Link | Notes |
|--------|-------------|------|-------|
| 0.a | License | [LICENSE](https://github.com/developerfred/papi-simulator/blob/main/LICENSE.md) | MIT License |
| 0.b | Documentation | [README.md](https://github.com/developerfred/papi-simulator/blob/main/README.md) | Includes architecture, features, and usage instructions |
| 0.c | Testing Guide | [TESTING.md](https://github.com/developerfred/papi-simulator/blob/main/TESTING.md) | Instructions for setup, usage, and testing the playground |



## Deliverables

| Number | Deliverable | Link | Notes |
| ------ | ----------- | ---- | ----- |
| 1.a | Enhanced Code Editor | [CodeEditor.tsx](https://github.com/developerfred/papi-simulator/blob/main/src/lib/editor/CodeEditor.tsx) | Monaco-based editor with TypeScript support for Polkadot API including autocompletion, type checking, and parameter hints. The editor is configured with Polkadot API-specific type definitions in [definitions.ts](https://github.com/developerfred/papi-simulator/blob/main/src/lib/editor/definitions.ts). |
| 1.b | React Component Preview Panel | [LivePreview Component](https://github.com/developerfred/papi-simulator/blob/main/src/components/LivePreview/index.tsx) | Real-time preview of React components with error boundaries and state preservation. This is integrated into the main playground UI in [Main.tsx](https://github.com/developerfred/papi-simulator/blob/main/src/components/Playground/Main.tsx). |
| 1.c | State Management System | [Store Directory](https://github.com/developerfred/papi-simulator/tree/main/src/store) | Comprehensive state management for blockchain interactions, including hooks for chain connection ([useChainStore.ts](https://github.com/developerfred/papi-simulator/blob/main/src/store/useChainStore.ts)), querying ([useQueryStore.ts](https://github.com/developerfred/papi-simulator/blob/main/src/store/useQueryStore.ts)), transactions ([useTransactionStore.ts](https://github.com/developerfred/papi-simulator/blob/main/src/store/useTransactionStore.ts)), and event subscriptions ([useEventStore.ts](https://github.com/developerfred/papi-simulator/blob/main/src/store/useEventStore.ts)). |
| 1.d | Polkadot API Integration | [Chain Provider](https://github.com/developerfred/papi-simulator/blob/main/src/context/ChainProvider.tsx) | Core integration layer that handles connections to multiple Polkadot networks, with support for WebSocket connections and proper subscription lifecycle management. |
| 1.e | Parachain Support Framework | [Network Constants](https://github.com/developerfred/papi-simulator/blob/main/src/lib/constants/networks.ts), [Blockchain Descriptors Update Workflow](https://github.com/developerfred/papi-simulator/blob/main/.github/workflows/update-chains.yml) | Framework for supporting multiple parachains through descriptors, with an automated update system using GitHub Actions to keep chain descriptors current. |

## Additional Information

The playground currently supports the following Polkadot ecosystem networks:
- Westend (Testnet) 
- Paseo (Testnet)
- Rococo (Testnet)
- Polkadot (Mainnet)

The user interface is designed to be intuitive and responsive, working both on desktop and mobile devices. The project uses Next.js 14 with App Router, TypeScript, and Tailwind CSS for a modern development experience.

Key features implemented:
- Live code execution with real-time previews
- Simulated transactions for testnets to demonstrate functionality safely
- Type-safe interactions with the blockchain through @polkadot-api/descriptors
- Interactive dashboard for monitoring blockchain events and blocks
- Network switching with persistent configuration
- Comprehensive error handling and user feedback
- Well-documented examples covering common use cases

The deployed application is available at [papi-simulator.aipop.fun](https://papi-simulator.aipop.fun/).

Repository: [https://github.com/developerfred/papi-simulator](https://github.com/developerfred/papi-simulator)
