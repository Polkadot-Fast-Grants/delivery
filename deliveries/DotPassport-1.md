# Milestone Delivery 📬

**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**  

* **Application Document:** https://github.com/Polkadot-Fast-Grants/apply/blob/master/applications/DotPassport.md  
* **Milestone Number:** 1  
* **DOT Payment Address:** 15MKh6ZjeKkRqz46gcMxEK9yLXpqhjzRYVKqK7dPg5UE2YA9  

**Context**  
Milestone 1 delivers the foundation of DotPassport: a deterministic **Reputation Engine** and a **Badge Generator** with clear metrics and levels, plus a minimal **DotPassport Profile UI** for demonstration.  An article on dotpassport.io describes the architecture and progress.

Check the dotpassport platform at [dotpassport.io](https://dotpassport.io)

**Deliverables**

| Number | Deliverable | Link | Notes |
| --- | --- | --- | --- |
| 0a. | License | https://github.com/SachinCoder1/DotPassport/blob/4467786d12465be1273f2b441ba6d70a32932faf/LICENSE | MIT |
| 0b. | Documentation | README: https://github.com/SachinCoder1/DotPassport/blob/4467786d12465be1273f2b441ba6d70a32932faf/README.md · OpenAPI: https://github.com/SachinCoder1/DotPassport/blob/4467786d12465be1273f2b441ba6d70a32932faf/backend/docs/openapi.yaml | Setup, environment variables, and API endpoints |
| 0c. | Article | https://dotpassport.io/blog/dotpassport-m1 | Milestone 1 overview published on dotpassport.io |
| 1a. | **Reputation Engine** | Score definitions: https://github.com/SachinCoder1/DotPassport/blob/4467786d12465be1273f2b441ba6d70a32932faf/backend/src/service/score/scoreDefinitions.ts · Score service: https://github.com/SachinCoder1/DotPassport/blob/4467786d12465be1273f2b441ba6d70a32932faf/backend/src/service/score/index.ts · Categories API: https://backend.dotpassport.io/api/v1/score/categories | Calculates reputation by summing category scores (longevity, tx count/volume, modules, governance, staking, token diversity, NFTs, extrinsic depth).  Category definitions include reasons, thresholds, and advice—for example, the **Account Longevity** category tiers from “Brand New” to “Veteran”:contentReference[oaicite:0]{index=0} and the **Transaction Count** tiers from “None” to “Transaction Master”:contentReference[oaicite:1]{index=1}.  Full category details are available via the `/score/categories` API. |
| 1b. | **Badge Generator** | Badge definitions: https://github.com/SachinCoder1/DotPassport/blob/4467786d12465be1273f2b441ba6d70a32932faf/backend/src/service/badge/badgeDefinitions.ts · Badge service: https://github.com/SachinCoder1/DotPassport/blob/4467786d12465be1273f2b441ba6d70a32932faf/backend/src/service/badge/index.ts · Definitions API: https://backend.dotpassport.io/api/v1/badge/definitions | Static badge catalog with levels based on metrics (e.g., `extrinsicCount`, `accountAgeDays`, `parachainInteractionCount`).  Badges like **Relay Chain Initiate** and **Polkadot Regular** define criteria and advice for each level:contentReference[oaicite:2]{index=2}.  The badge service fetches user metrics and evaluates badge levels.  Detailed badge metadata is accessible via the `/badge/definitions` API. |
| 2. | **DotPassport Profile UI** | Live demo: https://dotpassport.io · Landing: https://github.com/SachinCoder1/DotPassport/blob/4467786d12465be1273f2b441ba6d70a32932faf/client/src/components/landing/Landing.tsx · App shell: https://github.com/SachinCoder1/DotPassport/blob/4467786d12465be1273f2b441ba6d70a32932faf/client/src/app/app/page.tsx | Minimal front‑end built with Next.js + Tailwind to demonstrate the concept.  A full wallet connect flow, profile page, and widgets will be delivered in the next milestone. |

**Additional Information**  
Live demo: https://dotpassport.io  
A hosted data service (Subscan) provides on‑chain metrics in M1; a caching layer improves performance.  Public read endpoints, a TypeScript SDK, wallet integration, reusable widgets, and automated tests will be delivered in Milestone 2.
