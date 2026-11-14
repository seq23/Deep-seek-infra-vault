# DeepSeek AI Infrastructure Preservation Vault

Snapshot research date: 2026-11-14.

This folder supplements the upstream chat-demo source. It does **not** contain model weights or a self-hosted replica of DeepSeek's proprietary hosted services.

## Inventory
- [Model weights and licenses](MODEL_INVENTORY.md)
- [API documentation index](API_DOCUMENTATION.md)
- [Self-hosting playbook](SELF_HOSTING.md)
- [Backup verification](BACKUP_CHECKLIST.md)

## Preservation boundary
The upstream chat-demo is a static React/TypeScript frontend, licensed MIT. It stores conversations in browser IndexedDB and calls a configured remote API. A fork or ZIP preserves source code, not server-side model inference, search, speech, or stored user chats.

Do not commit API keys, customer data, or downloaded multi-GB model files to this repository. Preserve upstream copyright/license notices. Check third-party licenses before commercial use.
