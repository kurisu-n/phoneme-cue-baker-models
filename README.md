# phoneme-cue-baker-models

Public asset-only repo hosting model release assets consumed by the FaceCue
PhonemeCue baker (a Unity Editor extension). Each release tag is a model pack —
a phoneme recognizer, the ASR transcript generator, or a Voice Synthesis pack
(with its optional Hebrew and Changer add-ons) — shipped as one or more files.
The Setup wizard inside Unity
downloads + SHA256-verifies these assets on demand.

## Releases

| Tag | Pack | Upstream model | License |
| --- | --- | --- | --- |
| `v0.1.0` | Multilingual Transcript Decoder (lv60espeak) | `facebook/wav2vec2-lv-60-espeak-cv-ft` | Apache-2.0 |
| `v0.2.0` | English Free Decoder (Charsiu) | `charsiu/en_w2v2_fc_10ms` | MIT |
| `v0.3.0` | Mandarin Chinese Free Decoder (Charsiu) | `charsiu/zh_xlsr_fc_10ms` | MIT |
| `v0.4.0` | Japanese Free Decoder | `prj-beatrice/japanese-hubert-base-phoneme-ctc-v4` | Apache-2.0 |
| `v0.5.0` | Korean Free Decoder (slplab) | `slplab/wav2vec2-xls-r-300m_phone-mfa_korean` | Apache-2.0 |
| `v0.6.0` | Multilingual Phonemizer (CharsiuG2P) | `charsiu/g2p_multilingual_byT5_small_100` | MIT |
| `v0.7.0`, `v0.7.1`, `v0.8.0` | Multilingual ASR Transcript Generator | `openai/whisper-large-v3` | Apache-2.0 |
| `v0.9.0` | English Specialized ASR Transcript Generator | `distil-whisper/distil-large-v3` | MIT |
| `v1.0` | Voice Synthesis (`tts_v1`) + Hebrew Add-on (`tts_he_v1`) | see `NOTICE.md` | MIT + Apache-2.0; Hebrew CC-BY-4.0 |
| `v1.1.0` | Voice Synthesis - Changer Add-on (`enhance_v1`) | `alibabasglab/MossFormer2_SR_48K` | Apache-2.0 |
| `v1.2.0` | Voice Synthesis - Creation Denoise Add-on (`denoise_v1`) | `alibabasglab/MossFormer2_SE_48K` | Apache-2.0 |
| `v1.3.0` | Cross-Language Detection (`lid_v1`) | `speechbrain/lang-id-voxlingua107-ecapa` | Apache-2.0 |
| `v1.4.0` | Voice Synthesis vocoder update (`tts_v1`, FaceCue 1.0.2 and later) | `resemble-ai/chatterbox` (S3Gen HiFT vocoder) | MIT + Apache-2.0, see `NOTICE.md` |

Each model is an ONNX format conversion of the upstream weights, and a pack may
ship as multiple files (see the manifest). Where a release changes more than the
format, `NOTICE.md` says what. See `NOTICE.md` for full per-model attribution
and `LICENSE-MIT.txt` / `LICENSE-Apache-2.0.txt` for the license texts.

## What is this?

This repo exists only to host model release assets so they can be downloaded
without authentication. No source code lives here.

The Unity-side Setup wizard reads a bundled `recognizers.manifest.json` that
points at this repo's release assets. Asset integrity is enforced via SHA256
hashes baked into the manifest at build time, so the download path is
tamper-evident.
