# XENOR SOUL AI PRO V3 — Source Package

## Contents
- `pages/`: the uploaded Android PWA frontend, preserved as supplied.
- `worker/index.js`: backend Worker source for the existing D1 schema and bindings.

## Existing Cloudflare bindings expected by the Worker
- `AI`: Workers AI binding
- `DB`: D1 database binding with tables `soul_users`, `soul_memories`, `soul_messages`, `soul_tasks`, `soul_profiles`

## Deploy outline
1. Keep the existing Worker `xenor-soul-ai-pro-v3`.
2. Open its code editor / Quick Edit and replace the Hello World source with `worker/index.js`.
3. Save and Deploy.
4. Open the PWA from Pages and enter the Worker URL in Settings > Worker API URL:
   `https://xenor-soul-ai-pro-v3.ezzathazem780.workers.dev`
5. Test connection, chat, memory, and tasks.

## Important
- This package has not been deployed to the user's Cloudflare account.
- Workers AI calls can incur usage charges.
- The vision model `@cf/meta/llama-3.2-11b-vision-instruct` may require accepting Meta's license in Cloudflare before first use.
- The frontend's task reminders are browser/device notifications, not guaranteed background notifications when the app is closed.
