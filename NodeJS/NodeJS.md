25 ELITE NODE.JS SCENARIO QUESTIONS (USED BY UBER, NETFLIX, AMAZON)
1–5: API Performance & Reliability

1️⃣ A Node API becomes slow under 500 RPS. How do you design load shedding, rate limiting, and backpressure?

2️⃣ A downstream service is intermittently failing. How do you implement retries, circuit breakers, and exponential backoff?

3️⃣ You must process 10k queue jobs per second. How do you scale workers and manage concurrency limits?

4️⃣ A Redis cache becomes a bottleneck. How do you redesign your caching strategy?

5️⃣ A single API endpoint suddenly causes event loop blocking. How do you detect and fix the synchronous bottleneck?

6–10: Distributed Systems Behavior

6️⃣ You need to design idempotent APIs for payment processing. Explain the architecture.

7️⃣ A database write is happening twice. How do you detect race conditions?

8️⃣ Multiple Node services need shared configuration. How do you architect a config service?

9️⃣ You have inconsistent data across services. How do you design eventual consistency?

🔟 A long-running task breaks your Node server. How do you offload it?

11–15: Security & Authentication

1️⃣1️⃣ A JWT refresh strategy goes wrong and causes infinite token refresh loops. How do you fix it?

1️⃣2️⃣ A sensitive endpoint is vulnerable to timing attacks. How do you secure comparisons?

1️⃣3️⃣ You must throttle login attempts across distributed instances. How?

1️⃣4️⃣ Sessions need to persist across containers. How do you design distributed session storage?

1️⃣5️⃣ You need role-based access across microservices. How do you design an auth service?

16–20: Architecture & Scaling

1️⃣6️⃣ Design a scalable API gateway for microservices.

1️⃣7️⃣ Your Node service runs out of memory. How do you identify leaks using heap snapshots?

1️⃣8️⃣ Your DB connection pool is exhausted. How do you architect retries and pooling strategy?

1️⃣9️⃣ A queue backlog develops. How do you introduce worker autoscaling?

2️⃣0️⃣ Node server crashes on unhandled promise rejection. How do you build safe guards?

21–25: Real Engineering Scenarios

2️⃣1️⃣ Build a rate limiter that works across a distributed cluster.

2️⃣2️⃣ Your GraphQL server makes too many database queries. How do you optimize using batching & caching?

2️⃣3️⃣ File uploads block the event loop. How do you stream them efficiently?

2️⃣4️⃣ Logs are inconsistent across multiple pods. How do you implement a centralized logging system?

2️⃣5️⃣ API latency spikes in production. How do you build observability to diagnose root cause?