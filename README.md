# phoneme-cue-baker-models

Public asset-only repo hosting model release assets consumed by the FaceCue
PhonemeCue baker (Unity Editor extension). Each release tag is a recognizer
model bundle. The Setup wizard inside Unity downloads + SHA256-verifies these
assets on demand.

## Releases

- `v0.1.0` â€” `lv60espeak` (wav2vec2-lv-60-espeak-cv-ft, ~1.18 GB ONNX + 6 KB vocab)

## What is this?

This repo exists only to host model release assets so they can be downloaded
without authentication. No source code lives here. See `NOTICE.md` for upstream
attribution.

The Unity-side Setup wizard reads a bundled `recognizers.manifest.json` that
points at this repo's release assets. Asset integrity is enforced via SHA256
hashes baked into the manifest at build time, so the download path is
tamper-evident.
