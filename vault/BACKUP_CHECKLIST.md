# Backup and recovery checklist

- [x] GitHub fork exists: https://github.com/seq23/Deep-seek-infra-vault
- [x] User reports a source ZIP saved to Google Drive (not independently verified here)
- [x] Model/download source inventory recorded
- [x] API documentation URLs recorded
- [x] Self-hosting plan documented
- [ ] Save offline copies of API documentation to Drive
- [ ] Pin source commit and record a SHA-256 for the Drive ZIP
- [ ] Download and checksum model weights to dedicated large-capacity storage, if desired
- [ ] Create independent Git mirror/bundle to protect against fork deletion
- [ ] Test restoring source from Drive ZIP
- [ ] Test frontend build and model-serving endpoint separately

For disaster recovery, use at least two independent storage providers, keep a dated manifest, and test restores. A public GitHub fork alone is not a guaranteed permanent archive.
