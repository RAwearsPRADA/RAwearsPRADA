# RAwearsPRADA
**Backend & High-Performance Fullstack Engineer**  
*Location: Russia (Open to Remote / Relocation)*  
*Telegram: @RAwearsPRADA*  

---

### PROFILE SUMMARY
Performance-driven Full-Stack & Backend Engineer specializing in data layer optimization, distributed caching, and scalable real-time architectures. Proficient in TypeScript (Next.js / Node.js) and PostgreSQL. Experienced in offloading critical, low-latency network and transport layers to asynchronous Rust microservices to handle high concurrent loads efficiently. 

---

### TECHNICAL SKILLS
* **Languages:** TypeScript, JavaScript, Rust, C, SQL, PHP  
* **Backend & Web:** Node.js (Express, NestJS), Next.js (App Router/API Routes), WebSockets, REST API  
* **Infrastructure & DB:** PostgreSQL, Redis (Pub/Sub, Queues, Caching), Docker, Docker Compose, Linux, Nginx  
* **Concepts:** Database Denormalization, Batching Pipelines, Real-Time Sync, Cryptography (ChaCha20, HMAC-SHA256)  

---

### TECHNICAL CASE STUDIES & KEY ACHIEVEMENTS

#### 💬 chat-g | High-Performance Real-Time Messenger (Full-Stack / Architect)
*Designed and built a scalable, microservice-based real-time messaging platform engineered to eliminate database bottlenecks and reduce transport latency.*

* **Data Layer & Query Optimization:** 
  * **Sped up main screen data loading by ~9x** by strategically **denormalizing database schemas** and implementing highly optimized **raw SQL queries** instead of heavy ORM abstractions.
  * Reduced primary database read overhead by introducing a distributed **Redis caching layer** for frequently accessed hot datasets (user profiles, active chat metadata).
* **Database Write Optimization (Batching Pipeline):** 
  * **Reduced database disk I/O by 80%** under peak simulated loads by deploying an asynchronous write pipeline. 
  * Real-time message events are buffered inside **Redis Queues** and flushed into PostgreSQL by background workers via **bulk batch inserts** instead of execution via single atomic transactions, completely preventing table-locking issues.
* **Transport Layer Migration (Node.js -> Rust):** 
  * Extracted the heavy real-time WebSocket connection state management from Node.js into a dedicated asynchronous **Rust microservice**. 
  * **Cut memory consumption by 60%** and completely eliminated single-threaded Event Loop blocking spikes during rapid concurrent connection waves.
* **State Synchronization:** 
  * Designed an application-level real-time data framing protocol over WebSockets. Offloaded volatile, high-frequency state updates (user online/offline status, typing indicators, read receipts) to a **Redis Pub/Sub** mechanism to ensure near-zero latency delivery.

#### 🔒 synapse | Low-Level Network Protocol & Packet Analyzer (R&D / Systems)
*An experimental systems project focused on kernel-level packet manipulation and traffic security.*
* Developed a low-level packet capture engine in **C** leveraging the **WinDivert** library for network traffic interception and analysis.
* Implemented a fast **ChaCha20** stream cipher mechanism optimized for lightweight, low-overhead stream encryption.

---

### ENGINEERING PRINCIPLES
* **Pragmatic Tooling:** I prefer writing simple, type-safe, and maintainable TypeScript code for standard business features, migrating critical bottlenecks to compiled languages (Rust/C) only when driven by concrete performance metrics.
* **Bottleneck-Oriented Mindset:** I optimize based on profiling logs, execution plans, and load testing data rather than clean-code dogmas or premature engineering assumptions.
* **Full-Lifecycle Ownership:** Capable of designing database schemas, writing efficient backend logic, building responsive interfaces, and configuring production environments via Docker and Linux.
