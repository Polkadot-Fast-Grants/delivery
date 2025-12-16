# Milestone Delivery 📬

> ⚡ Only the GitHub account that submitted the application is allowed to submit milestones. 
> 
> Don't remove any of the mandatory parts presented in bold letters or as headlines! Lines starting with `>`, such as this one, can be removed.

**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**  

* **Application Document:** 
https://github.com/Polkadot-Fast-Grants/apply/blob/master/applications/eunoia.md 

* **Milestone Number:** 
1

* **DOT Payment Address:** 
15MRXEPxWHfS5o7Ahri6C2kCzvSLPfpvMfrNa9Mm8QgKFpjt

**Context** (optional)
> Please provide a short paragraph or two connecting the deliverables in this milestone and describing their purpose.

Milestone 1 focuses on developing and deploying the Eunoia project onto the Polkadot mainnet, enabling real token donations. This milestone delivers the foundation of the platform, the mainnet-ready UI with integrated APIs, and the initial documentation and licensing required for transparency. Together, these deliverables provide the essential infrastructure to support real-world testing, allowing donors to make verified contributions and charities to begin receiving on-chain donations through the platform.

As the Polkadot team deprecated older tools and introduced new builds with critical fixes and features, we migrated our codebase to use the latest PAPI SDK and the updated ink! v6 provided by the Polkadot team. This ensures compatibility, stability, and alignment with the most up-to-date ecosystem standards.

**Deliverables**
> Please provide a list of all deliverables of the milestone extracted from the initial application and a link to the deliverable itself. Ideally all links inside the below table should include a commit hash, which will be used for testing. If you don't provide a commit hash, we will work off the default branch of your repository. Thus, if you plan on continuing work after delivery, we suggest you create a separate branch for either the delivery or your continuing work.
> 
> Remember that milestone payments are capped at $5,000 USD and must be delivered within 3 months of approval.
> 
> If there is anything particular about any of the deliverables we or a future reader should know, use the respective `Notes` column.

| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 0a. | License | https://github.com/JY20/eunoia/blob/polkadot-m1/tutorial/integration_test.md | MIT licenses are included in the GitHub repository. | 
| 0b.  | Documentation | https://github.com/JY20/eunoia/blob/polkadot-m1/tutorial/integration_test.md | Separate README files are provided for different components, along with a main README for users and a tutorial file. | 
| 0c.  | Testing and Testing Guide | https://github.com/JY20/eunoia/blob/polkadot-m1/tutorial/integration_test.md | The majority of the work is completed, final updates are in progress. | 
| 0d.  | Article | https://github.com/JY20/eunoia/tree/polkadot-m3 | The majority of the work is completed, final updates are in progress. | 
| 1.  | Mainnet Smart Contract Launch | https://github.com/JY20/eunoia/blob/polkadot-m1/tutorial/integration_test.md | Instead of using Ink! v6 (due to its instability in the alpha stage), the Polkadot team instructed us to adopt PAPI. The contract is available in the eunoia2 repo, but alternative approaches are recommended for stability. See tutorial.md to test this deliverable. | 
| 2.  | Mainnet UI + API Launch | https://github.com/JY20/eunoia/blob/polkadot-m1/tutorial/integration_test.md | The mainnet UI is complete and integrated with PAPI instead of Polkadot-JS. See tutorial.md to test this deliverable. | 
| 3.  | Compass Launch | https://github.com/JY20/eunoia/tree/polkadot-m2 | Completed as part of Milestone 2. | 
| 4.  | Charities Onboarding | https://github.com/JY20/eunoia/tree/polkadot-m3 | The majority of the work is completed, final updates are in progress. | 
| 5.  | Users Onboarding | https://github.com/JY20/eunoia/tree/polkadot-m3 | The majority of the work is completed, final updates are in progress. | 
| 6.  | Eunoia Documents | https://github.com/JY20/eunoia/tree/polkadot-m3 | The majority of the work is completed, final updates are in progress. | 

**Additional Information**
> Any further comments on the milestone that you would like to share with us.
> 
We faced significant barriers during Milestone 1 due to the migration to ink! v6, which is still in its alpha stage. This made troubleshooting and contract development difficult, and the delayed response times from the support team (often 1–3 days) further slowed progress. Later, the Polkadot team instructed us to use PAPI to achieve our goals instead.

To maintain momentum, we focused on completing Milestone 2 in parallel, as our team had been working on all three milestones concurrently. With this PR, we are providing the updates and delivery for Milestone 1 and awaiting its approval before submitting Milestone 2.

Looking ahead to Milestone 3, we’ve secured a letter of interest from one of the largest charities in Ontario, along with interest from other organizations, and are actively working on onboarding them onto the Eunoia platform.

> Note: After submission, your milestone will be evaluated within 14 days. If changes are needed, you will have one opportunity to fix and resubmit within 14 days.
