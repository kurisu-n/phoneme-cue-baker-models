# phoneme-cue-baker-models

Public asset-only repo hosting model release assets consumed by the FaceCue
PhonemeCue baker (a Unity Editor extension). Each release tag is a recognizer
model bundle (`model.onnx` + `vocab.json`). The Setup wizard inside Unity
downloads + SHA256-verifies these assets on demand.

## Releases

| Tag | Recognizer | Upstream model | License |
| --- | --- | --- | --- |
| `v0.1.0` | Multilingual Transcript Decoder (lv60espeak) | `facebook/wav2vec2-lv-60-espeak-cv-ft` | Apache-2.0 |
| `v0.2.0` | English Free Decoder (Charsiu) | `charsiu/en_w2v2_fc_10ms` | MIT |
| `v0.3.0` | Mandarin Chinese Free Decoder (Charsiu) | `charsiu/zh_xlsr_fc_10ms` | MIT |
| `v0.4.0` | Japanese Free Decoder | `prj-beatrice/japanese-hubert-base-phoneme-ctc-v4` | Apache-2.0 |
| `v0.5.0` | Korean Free Decoder (slplab) | `slplab/wav2vec2-xls-r-300m_phone-mfa_korean` | Apache-2.0 |

Each `model.onnx` is an ONNX format conversion of the upstream weights (format
only; weights unchanged). See `NOTICE.md` for full per-model attribution and
`LICENSE-MIT.txt` / `LICENSE-Apache-2.0.txt` for the license texts.

## What is this?

This repo exists only to host model release assets so they can be downloaded
without authentication. No source code lives here.

The Unity-side Setup wizard reads a bundled `recognizers.manifest.json` that
points at this repo's release assets. Asset integrity is enforced via SHA256
hashes baked into the manifest at build time, so the download path is
tamper-evident.
