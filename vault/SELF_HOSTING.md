# Self-hosting playbook

## A. Run the saved chat frontend
Prerequisites: Node.js 22.12+, pnpm, and a computer.

```bash
git clone https://github.com/seq23/Deep-seek-infra-vault.git
cd Deep-seek-infra-vault
pnpm install
pnpm dev
```

Open http://localhost:8090. For a static build run `pnpm build`. See upstream README for browser file:// limitations.

**This frontend still requires a compatible API service and an API key.** The upstream application defaults to the DeepSeek API and uses extensions for search, link reading, speech and other features. A generic OpenAI-compatible server may not implement those extensions.

## B. Self-host model inference independently
1. Choose a published weight set and read its exact model card/license.
2. Provision a GPU server with adequate VRAM, RAM, disk and bandwidth. Full V3.2 weights are roughly 690 GB on Hugging Face; consumer laptop inference is not a realistic default.
3. Use a runtime specifically supporting the chosen model architecture; follow the model's official deployment guide, not generic unverified commands.
4. Expose an authenticated, rate-limited inference endpoint over TLS.
5. Build a compatibility adapter for the chat frontend's actual API protocol; test streaming, tool calling, errors and attachments.
6. Replace hosted search, fetch, OCR, ASR and TTS with independently selected components if complete independence is the goal.
7. Run privacy, security, cost and license reviews before handling customer data.

## C. What remains unverified
No GPU was provisioned, no weights were downloaded, no local inference service was started, and no end-to-end compatibility test was run. This document is a deployment plan, not a tested one-command full-stack installer.
