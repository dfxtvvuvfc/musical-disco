# VODKA Panel — KV + two-step first login

## Cloudflare
1. Create a KV namespace.
2. Worker → Settings → Bindings → Add KV Namespace.
3. Variable name must be exactly `VODKA_KV`.
4. Set the namespace to your KV.
5. Add a Worker Secret named `VODKA_DEFAULT_PASSWORD`.
6. Deploy.

## GitHub / Builds
Build command: empty.
Deploy command:
`npx wrangler deploy`

No obfuscation/encoding GitHub workflow is included.

## First login
First open asks for the default password. Then it asks for a new master password twice. The master password is stored in KV.
