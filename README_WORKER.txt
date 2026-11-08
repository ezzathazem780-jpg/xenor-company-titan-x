XENOR SOUL AI PRO V3 — Worker Backend

Contents:
- worker/index.js: Cloudflare Worker source compatible with the supplied XENOR SOUL AI PRO V3 PWA.

Required existing Cloudflare bindings:
- D1 binding name: DB
- Workers AI binding name: AI

Required D1 tables:
- soul_users
- soul_memories
- soul_messages
- soul_tasks
- soul_profiles

Deployment:
1. Open Cloudflare Dashboard > Workers & Pages.
2. Open the Worker service you want to use (recommended name: xenor-soul-ai-pro-v3).
3. Open Edit code / Quick Edit.
4. Replace the editor contents with worker/index.js from this package.
5. Save and Deploy.
6. In the PWA, open Settings and set Worker API URL to the deployed Worker URL.
7. Use the app's connection test.

Important:
- This package does not deploy anything to Cloudflare automatically.
- Do not create a new D1 database if the existing database is already bound as DB.
- Workers AI must be enabled and bound as AI.
- AI usage may incur charges.
- The vision model may require accepting its provider license in Cloudflare.
