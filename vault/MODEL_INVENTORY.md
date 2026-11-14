# Model weight inventory

Research date: 2026-11-14. These are **links and preservation instructions**, not downloaded weights.

| Artifact | Official location | Status |
|---|---|---|
| DeepSeek-V3.2 weights | https://huggingface.co/deepseek-ai/DeepSeek-V3.2 | Published; MIT model card; approx. 690 GB repository |
| DeepSeek-V3 inference reference | https://github.com/deepseek-ai/DeepSeek-V3 | Published code, docs and model download links |
| DeepSeek organization models | https://huggingface.co/deepseek-ai | Catalog; inspect each model's license and revision separately |

The currently hosted `deepseek-flash` and `deepseek-v4-pro` API offerings must **not** be assumed equivalent to downloadable V3.2 weights. Hosted services, model weights, and API names are separate artifacts.

## Download on a suitable machine
Install the Hugging Face CLI and download a pinned revision to storage with sufficient capacity:

```bash
python -m pip install -U huggingface_hub
hf download deepseek-ai/DeepSeek-V3.2 --local-dir ./weights/DeepSeek-V3.2
```

For reproducibility, resolve and record a commit SHA first; pass `--revision <commit-sha>` when downloading. Verify free disk space, transfer cost, licensing and hardware before starting. Do not attempt this on a phone or inside a GitHub repository.

## Manifest fields
Record model ID, upstream revision SHA, license, file sizes, SHA-256 checksums, download date, storage destination, inference runtime version, and a successful test result. No weight download has been performed as part of this vault update.
