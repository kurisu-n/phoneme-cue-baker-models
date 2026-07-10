# NOTICE

This repository hosts model release assets consumed by the FaceCue PhonemeCue
baker (a Unity Editor extension). It contains no source code; each release tag
holds one `model.onnx` plus a small `vocab.json`.

Each `model.onnx` is an ONNX **format conversion**, produced by the FaceCue
project, of an upstream open-source model published on Hugging Face. The export
changes only the serialization format (PyTorch -> ONNX); the trained weights are
not otherwise altered. In the Apache-2.0 Section 4(b) sense each export is a
"modified file", and this notice states that change here.

Upstream sources, licenses, and copyright holders are listed per release below.
Full license texts are in `LICENSE-MIT.txt` and `LICENSE-Apache-2.0.txt`.

--------------------------------------------------------------------------------

## v0.1.0 - Multilingual Transcript Decoder (lv60espeak)

- ONNX re-export of `facebook/wav2vec2-lv-60-espeak-cv-ft`
  https://huggingface.co/facebook/wav2vec2-lv-60-espeak-cv-ft
- License: Apache-2.0  (see `LICENSE-Apache-2.0.txt`)
- Copyright (c) the wav2vec2 / fairseq authors, Facebook AI Research /
  Meta Platforms, Inc.

## v0.2.0 - English Free Decoder (Charsiu, English)

- ONNX re-export of `charsiu/en_w2v2_fc_10ms`
  https://huggingface.co/charsiu/en_w2v2_fc_10ms
  from the Charsiu project, https://github.com/lingjzhu/charsiu
- License: MIT  (see `LICENSE-MIT.txt`)
- Copyright (c) 2021 jzhu

## v0.3.0 - Mandarin Chinese Free Decoder (Charsiu, Mandarin)

- ONNX re-export of `charsiu/zh_xlsr_fc_10ms`
  https://huggingface.co/charsiu/zh_xlsr_fc_10ms
  from the Charsiu project, https://github.com/lingjzhu/charsiu
- License: MIT  (see `LICENSE-MIT.txt`)
- Copyright (c) 2021 jzhu

## v0.4.0 - Japanese Free Decoder (japanese-hubert-base-phoneme-ctc)

- ONNX re-export of `prj-beatrice/japanese-hubert-base-phoneme-ctc-v4`
  https://huggingface.co/prj-beatrice/japanese-hubert-base-phoneme-ctc-v4
  (a phoneme-CTC fine-tune of the base model `rinna/japanese-hubert-base`,
  https://huggingface.co/rinna/japanese-hubert-base)
- License: Apache-2.0  (see `LICENSE-Apache-2.0.txt`); base model also Apache-2.0
- Copyright (c) the Beatrice project (prj-beatrice); base model copyright (c)
  rinna Co., Ltd.

## v0.5.0 - Korean Free Decoder (slplab)

- ONNX re-export of `slplab/wav2vec2-xls-r-300m_phone-mfa_korean`
  https://huggingface.co/slplab/wav2vec2-xls-r-300m_phone-mfa_korean
- License: Apache-2.0  (see `LICENSE-Apache-2.0.txt`)
- Copyright (c) SLPlab (Speech and Language Processing Laboratory)

## v1.1.0 - Voice Synthesis Changer Add-on (Speech Super-Resolution 48k)

- ONNX re-export of `alibabasglab/MossFormer2_SR_48K`
  https://huggingface.co/alibabasglab/MossFormer2_SR_48K
  from the ClearerVoice-Studio project, https://github.com/modelscope/ClearerVoice-Studio
  (the super-resolution transformer and its HiFi-GAN vocoder folded into one
  waveform-to-waveform graph, mel front-end included; both upstream checkpoints,
  weights unchanged)
- License: Apache-2.0  (see `LICENSE-Apache-2.0.txt`)
- Copyright (c) Alibaba Group (the ClearerVoice-Studio authors)
