# Milestone Delivery 📬

**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**  

* **Application Document:** https://github.com/Polkadot-Fast-Grants/apply/blob/master/applications/AgentDot.md .
* **Milestone Number:** 2
* **DOT Payment Address:** 14XNJmoUzkvmh9cYoqG4axBRR4BWzWRbnFP79oiZgKu7V9bz.

**Context**:
This milestone implements an automatic transaction queuing and batching system that enables efficient execution of multiple blockchain operations through a single wallet signature. The transaction queue is integrated directly into the Next.js chat interface, where the AI assistant automatically detects when users request multiple transactions in a single message and collects them into an in-memory queue using React refs. Users review pending transactions through the AI's confirmation messages, which display all queued operations (including transaction types, amounts, and destinations) before prompting for explicit approval. Once confirmed, the queued transactions are automatically passed to the batch extrinsic signer, which uses Polkadot's Utility pallet (`utility.batch` or `utility.batch_all`) to combine multiple transaction calls into a single extrinsic. The batch signer leverages PAPI's `signAndSubmit` method to sign and submit transactions, providing immediate feedback on success or failure through toast notifications and chat messages. Upon successful submission, users receive the transaction hash with a link to view the transaction on Subscan. This architecture eliminates the need for multiple wallet popups and enables atomic (batchAll) or partial-success (batch) transaction execution, significantly improving the user experience when performing complex multi-step operations on polkadot sdk chains.

**Deliverables**

| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 2a. | Transaction Queue UI(Build a Next.js-based interface for users to review, reorder, or cancel pending transactions) |miltestone-2| Kindly test on the milestone-2 branch | 
| 2b.  | Batch Extrinsic Signer(Implement batch signing (utility.batch) for queued transactions along with callback/tracing using PAPI’s signSubmitAndWatch) |milestone-2| Kindly test on the milestone-2 branch | 


**Additional Information**

The implementation differs from the original specification in a few key ways:

1. **Transaction Queue UI (Deliverable 2a)**: Instead of a separate Next.js interface for reviewing/reordering/canceling transactions, we implemented an automatic transaction queuing system directly integrated into the chat interface. Transactions are collected in-memory using React refs and users review them through AI confirmation messages before execution. This approach provides a more seamless user experience within the conversational flow, though it does not currently support manual reordering or cancellation of queued transactions.

2. **Batch Signing with Callbacks/Tracing (Deliverable 2b)**: The implementation uses PAPI's `signAndSubmit` method rather than `signSubmitAndWatch`. While `signAndSubmit` provides immediate feedback on transaction success/failure and returns the transaction hash, it does not provide ongoing callback/tracing functionality for transaction status updates (e.g., in-progress, finalized, failed). Users receive feedback through toast notifications and chat messages with Subscan links for transaction details. This was chosen for simplicity and immediate user feedback, though future enhancements could integrate `signSubmitAndWatch` for real-time transaction status updates.

3. **Automatic Batching**: The system automatically detects and batches multiple transactions when users request multiple operations in a single message, including XCM transfers and nomination pool operations. This reduces the need for explicit batch commands while still supporting manual batch requests through the `batchAgent` and `batchAllAgent` tools.

**Technical Decisions:**
- Used React refs for in-memory transaction queuing to avoid unnecessary re-renders
- Implemented automatic batching detection to improve UX for common multi-transaction scenarios
- Chose `signAndSubmit` for immediate feedback over `signSubmitAndWatch` for ongoing tracing
- Integrated queue review into chat flow rather than separate UI component for consistency with the conversational interface

**Future Enhancements:**
- Add support for manual transaction reordering and cancellation
- Integrate `signSubmitAndWatch` for real-time transaction status callbacks
- Consider a dedicated transaction queue UI component for advanced users
