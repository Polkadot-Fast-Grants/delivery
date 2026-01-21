# Milestone Delivery

**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**

* **Application Document:** [Link to merged application](https://github.com/Polkadot-Fast-Grants/apply/pull/93)
* **Milestone Number:** 2
* **DOT Payment Address:** *15rJebyfaZn19EPWavAw89UMaKkqfvTs8ahbnH2d4UjvHpue*

## Context

This milestone delivers the **On-Chain Integration and Multi-Sig Implementation** for the GrantFlow.dev platform. The implementation enables full grant cycles from submission to on-chain payout using Polkadot's multisig and child bounties pallets on the Paseo Asset Hub TestNet.

Key achievements:
- **Full multisig integration** using the Polkadot multisig pallet for committee-based approvals
- **Child bounty pallet integration** for proper on-chain indexing by Subscan/Subsquare
- **Two workflow patterns** (merged and separated) for different committee needs
- **Transaction simulation** with comprehensive error handling and user-friendly error messages
- **Balance validation** for both transaction fees and parent bounty funds
- **Live testnet deployment** with Bounty #32 on Paseo Asset Hub

The platform now supports the complete on-chain workflow:
1. Grantee submits milestone
2. Committee members review and sign with their Polkadot wallets
3. Upon threshold reached, the payout executes automatically via child bounty creation
4. Funds are transferred to the beneficiary address

## Deliverables

| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 0a. | License | [LICENSE](https://github.com/MbBrainz/grantflow-dev/blob/main/LICENSE) | MIT License |
| 0b. | Documentation | [Multisig Integration Docs](https://github.com/MbBrainz/grantflow-dev/blob/main/src/lib/polkadot/README.md), [Multisig Discovery Docs](https://github.com/MbBrainz/grantflow-dev/blob/main/src/lib/polkadot/MULTISIG_DISCOVERY.md), [docs.grantflow.dev](https://docs.grantflow.dev) | Comprehensive documentation covering multisig workflows, child bounty integration, and committee configuration. Updated user guides for on-chain features. |
| 0c. | Testing and Testing Guide | [Testing Guide](https://github.com/MbBrainz/grantflow-dev/blob/main/tutorial-milestone2.md), [Multisig Tests](https://github.com/MbBrainz/grantflow-dev/blob/main/__tests__/lib/polkadot/multisig.test.ts), [Child Bounty Tests](https://github.com/MbBrainz/grantflow-dev/blob/main/__tests__/lib/polkadot/child-bounty.test.ts) | Step-by-step testing guide for Paseo Asset Hub TestNet. Unit tests for multisig operations and child bounty creation. |
| 1. | Polkadot Multisig Integration | [multisig.ts](https://github.com/MbBrainz/grantflow-dev/blob/main/src/lib/polkadot/multisig.ts) | Core multisig utilities including `initiateMultisigApproval`, `approveOrExecuteMultisigCall`, quorum detection, and pending multisig queries. Supports both 2-of-3 and other threshold configurations. |
| 2. | Child Bounty Pallet Integration | [child-bounty.ts](https://github.com/MbBrainz/grantflow-dev/blob/main/src/lib/polkadot/child-bounty.ts) | Full child bounty lifecycle implementation: addChildBounty, proposeCurator, acceptCurator, awardChildBounty, claimChildBounty - bundled atomically using `utility.batchAll`. |
| 3. | Transaction Simulation & Validation | [transaction-simulation.ts](https://github.com/MbBrainz/grantflow-dev/blob/main/src/lib/polkadot/transaction-simulation.ts), [balance.ts](https://github.com/MbBrainz/grantflow-dev/blob/main/src/lib/polkadot/balance.ts) | Pre-flight transaction simulation to catch errors before signing. Balance validation for transaction fees and parent bounty funds with user-friendly error messages. |
| 4. | Multisig Discovery & Address Utilities | [multisig-discovery.ts](https://github.com/MbBrainz/grantflow-dev/blob/main/src/lib/polkadot/multisig-discovery.ts), [multisig-address.ts](https://github.com/MbBrainz/grantflow-dev/blob/main/src/lib/polkadot/multisig-address.ts), [address.ts](https://github.com/MbBrainz/grantflow-dev/blob/main/src/lib/polkadot/address.ts) | Automatic multisig discovery from chain state, address validation across networks, and SS58 encoding/decoding support. |
| 5. | React Hooks & UI Components | [use-multisig-approval.ts](https://github.com/MbBrainz/grantflow-dev/blob/main/src/lib/hooks/use-multisig-approval.ts), [milestone-voting-panel.tsx](https://github.com/MbBrainz/grantflow-dev/blob/main/src/components/milestone/milestone-voting-panel.tsx), [multisig-flow-explanation.tsx](https://github.com/MbBrainz/grantflow-dev/blob/main/src/components/milestone/multisig-flow-explanation.tsx) | React hooks for wallet connection and multisig operations. UI components for milestone approval flows, signatory vote lists, and multisig workflow explanations. |
| 6. | Server Actions & Database Integration | [multisig-actions.ts](https://github.com/MbBrainz/grantflow-dev/blob/main/src/app/(dashboard)/dashboard/submissions/multisig-actions.ts), [milestone-approvals.ts](https://github.com/MbBrainz/grantflow-dev/blob/main/src/lib/db/writes/milestone-approvals.ts) | Server-side actions for persisting multisig state, tracking approvals, and managing milestone completion. |
| 7. | Testnet Deployment | [grantflow.dev](https://grantflow.dev) | Live deployment on Paseo Asset Hub TestNet with Bounty #32 configured for the Fast Grants committee. |

## Testing Guide Summary

A comprehensive testing tutorial is available at [tutorial-milestone2.md](https://github.com/MbBrainz/grantflow-dev/blob/main/tutorial-milestone2.md). Key testing steps:

### Test Environment
- **Network:** Paseo Asset Hub TestNet
- **Bounty:** #32
- **Committee:** Fast Grants (testnet version)
- **Multisig Configuration:** 2-of-3 threshold

### Test Wallet Import
Import the following seed phrase with derivation path `//2`:
```
media spice upset obvious slush advice derive know staff like hold extra
```

### Testing Workflow
1. Navigate to [grantflow.dev](https://grantflow.dev)
2. Connect wallet and claim committee membership
3. Review milestone with existing approval (1/2 signatures) - sign to complete
4. Review milestone with no approvals (0/2 signatures) - initiate process
5. Process pending grant submissions

### Verification Commands
```bash
# Run unit tests
pnpm test

# Type checking
pnpm typecheck

# Run specific multisig tests
pnpm test __tests__/lib/polkadot/multisig.test.ts
pnpm test __tests__/lib/polkadot/child-bounty.test.ts
```

## Additional Information

### Technical Implementation Details

**Multisig Workflow Patterns:**

1. **Merged Workflow** - Review approval and blockchain signature happen together. Ideal for high-trust committees wanting faster, one-step approvals.

2. **Separated Workflow** - Two-phase process where review approval and payment execution are separate. Better for regulated environments or high-value grants.

**Child Bounty Integration:**

The platform uses Polkadot's `childBounties` pallet for proper on-chain indexing. The payout process bundles 5 calls atomically:
1. `addChildBounty` - Creates child bounty under parent
2. `proposeCurator` - Parent curator proposes curator for child
3. `acceptCurator` - Curator accepts the role
4. `awardChildBounty` - Awards to beneficiary
5. `claimChildBounty` - Pays out funds

All calls are wrapped in `utility.batchAll` for atomic execution (all-or-nothing).

**Libraries Used:**
- **dedot** - Modern TypeScript Polkadot API client
- **luno-kit** - React hooks for Polkadot wallet integration
- **@polkadot/util-crypto** - Address encoding/decoding utilities

### Known Limitations

1. **Race Condition Risk**: Child bounty IDs are predicted by querying `childBountyCount`. If another child bounty is created between query and execution, the ID may mismatch. This is mitigated by the atomic batch execution.

2. **Network Support**: Currently optimized for Paseo Asset Hub TestNet. Production deployment to Polkadot/Kusama will require additional configuration and testing.

### Future Improvements (Milestone 3+)

- Production deployment to Polkadot mainnet
- Enhanced error recovery for failed transactions
- Batch milestone approvals
- Real-time transaction status updates via WebSockets

## Milestone Submission Verification

All deliverables can be verified by:

1. **Code Review**: Inspect the Polkadot integration code in `/src/lib/polkadot/`
2. **Run Tests**: Execute `pnpm test` to run the multisig and child bounty test suites
3. **TestNet Testing**: Follow the testing guide to perform actual multisig transactions on Paseo Asset Hub
4. **Live Demo**: Access [grantflow.dev](https://grantflow.dev) and test the full workflow

### Demo Environment
- **URL**: [grantflow.dev](https://grantflow.dev)
- **TestNet**: Paseo Asset Hub
- **Bounty ID**: #32
- **Committee**: Fast Grants

Note: After submission, your milestone will be evaluated within 14 days. If changes are needed, you will have one opportunity to fix and resubmit within 14 days.
