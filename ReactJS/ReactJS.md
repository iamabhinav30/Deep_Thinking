[Scenario_ : ](#scenario_-)
ELITE REACT SCENARIO QUESTIONS (REAL FAANG INTERVIEW STYLE)
1–5: Performance & Rendering

1️⃣ You have a React page with 50+ components re-rendering unnecessarily. How do you trace renders and fix them using memoization, selectors, useCallback, and profiling tools?

2️⃣ A prop drill chain is causing unnecessary re-renders across a large tree. How do you refactor using context selectors or Zustand/Jotai?

3️⃣ A React list with 10k items lags on scroll. How do you virtualize it and avoid layout thrashing?

4️⃣ Your React app freezes during hydration in Next.js. How do you redesign components to defer hydration using server components?

5️⃣ A React Form with 100+ fields becomes slow. How do you restructure using controlled vs uncontrolled inputs and form libraries?

6–10: Advanced Hooks & Concurrency

6️⃣ You detect a stale closure bug. How do you identify it and rewrite the hook?

7️⃣ An expensive calculation runs on every render even with useMemo. Why? What's the root cause?

8️⃣ A custom hook shares state across multiple component instances unintentionally. Why?

9️⃣ You need to cancel API requests when components unmount. How do you architect cancellation?

🔟 A React Suspense boundary fails to recover from an error. How do you design nested boundaries?

11–15: Next.js + SSR + Server Components

1️⃣1️⃣ Your Next.js API routes must handle high traffic. How do you optimize caching in route handlers?

1️⃣2️⃣ A server component triggers too many re-renders. Why does this happen?

1️⃣3️⃣ You need real-time updates on a server component page. How do you architect this?

1️⃣4️⃣ Next.js middleware must authenticate users quickly. How do you avoid cold starts and optimize edge handlers?

1️⃣5️⃣ A page breaks because server/client boundaries are misplaced. How do you diagnose this?

16–20: Architecture & Code Design

1️⃣6️⃣ You need a plugin-based UI that supports themes, forms, widgets. How do you design a React component registry?

1️⃣7️⃣ A global modal service must work anywhere in the app. How do you build it without prop drilling?

1️⃣8️⃣ You have repetitive API calls across pages. How do you centralize data fetching with SWR/React-Query?

1️⃣9️⃣ A dashboard has multiple real-time widgets. How do you optimize WebSocket state distribution?

2️⃣0️⃣ You must migrate a large app from Redux to Zustand. Explain your strategy.

21–25: Testing, Security, Reliability

2️⃣1️⃣ You need to test a React component using mocking of fetch/axios. How do you design it?

2️⃣2️⃣ A cross-site scripting vulnerability exists in dangerouslySetInnerHTML. How do you sanitize input?

2️⃣3️⃣ A flaky Jest test passes locally but fails in CI. How do you debug and solve it?

2️⃣4️⃣ A React tree crashes in production due to invalid props. How do you add runtime validation?

2️⃣5️⃣ How do you ensure error boundaries capture all async rendering errors?