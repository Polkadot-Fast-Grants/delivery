# Milestone Delivery 📬

**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**  

* **Application Document:** [Polka RTC](https://github.com/Polkadot-Fast-Grants/apply/blob/master/applications/polka_RTC.md)
* **Milestone Number:** 1
* **DOT Payment Address:** `1UGiZSCpf96g5uT7FdyC8SNhNgSWerv1ky7zBdeyyrJLHtS`

**Context** (optional)

Milestone 1 focuses on establishing the foundational infrastructure and core functionality of the proctoring system. The signaling server, built using Actix-Web, provides the essential communication layer for managing WebRTC session initiation and coordination between peers. The SFU media routing module, implemented with webrtc, enables efficient real-time handling of audio and video streams, ensuring scalability and performance during multi-user sessions.

Additionally, a basic React-based frontend integration was developed to demonstrate real-time video streaming and connection flow, serving as the initial interface for the proctoring system’s user experience. Together, these deliverables establish a working prototype that connects backend signaling and SFU components with a functional frontend interface.

**Deliverables**

| Number | Deliverable | Link                                                     | Notes |
|--------| ------------- |----------------------------------------------------------|------------- |
| 1      | Set up signaling server (actix-web) | [SFU-Backend](https://github.com/DDPidhi/sfu-server/)                                         | ...| 
| 2      | Implement SFU media routing (webrtc-rs) | [SFU-Backend](https://github.com/DDPidhi/sfu-server/)                                                   | ...| 
| 3      | Develop test suite + CLI validation | [SFU-Backend](https://github.com/DDPidhi/sfu-server/)                                                   | ...| 
| 4      | Basic frontend (React) integration for proctoring | [SFU-UI](https://github.com/DDPidhi/sfu-ui/) | ...|

**Additional Information**
