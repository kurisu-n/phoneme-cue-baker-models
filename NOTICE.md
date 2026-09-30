# NOTICE

This repository hosts model release assets consumed by the FaceCue PhonemeCue
baker (a Unity Editor extension). It contains no source code; each release tag
holds one or more model files plus small support files (vocabularies,
configuration, filterbanks).

Each model file is an ONNX **format conversion**, produced by the FaceCue
project, of an upstream open-source model. Unless its section below says
otherwise, the export changes only the serialization format (PyTorch -> ONNX)
and the trained weights are not otherwise altered. Where a release changes more
(weights stored as 16-bit floating point, parts of a graph replaced), its
section states the change. In the Apache-2.0 Section 4(b) sense each export is a
"modified file", and this notice states those changes here.

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

## v0.6.0 - Multilingual Phonemizer (CharsiuG2P)

- ONNX re-export (encoder and decoder) of `charsiu/g2p_multilingual_byT5_small_100`
  https://huggingface.co/charsiu/g2p_multilingual_byT5_small_100
  from the CharsiuG2P project, https://github.com/lingjzhu/CharsiuG2P
- License: MIT  (see `LICENSE-MIT.txt`)
- Copyright (c) 2022 jzhu
- Fine-tuned from `google/byt5-small`, https://huggingface.co/google/byt5-small,
  Apache-2.0  (see `LICENSE-Apache-2.0.txt`), Copyright (c) Google

## v0.7.0, v0.7.1, v0.8.0 - Multilingual ASR Transcript Generator (Whisper large-v3)

- ONNX re-export of `openai/whisper-large-v3`
  https://huggingface.co/openai/whisper-large-v3
  (v0.7.0: the encoder and decoder; v0.7.1: a configuration update only;
  v0.8.0: the decoder in a key-value-cached form, its weights in one shared file)
- Changes beyond the format: weights stored as 16-bit floating point.
- License: Apache-2.0  (see `LICENSE-Apache-2.0.txt`)
- Copyright (c) OpenAI

## v0.9.0 - English Specialized ASR Transcript Generator (Distil-Whisper)

- ONNX re-export of the decoder of `distil-whisper/distil-large-v3`
  https://huggingface.co/distil-whisper/distil-large-v3
  (used with the Whisper large-v3 encoder from v0.7.0)
- Changes beyond the format: weights stored as 16-bit floating point.
- License: MIT  (see `LICENSE-MIT.txt`)
- Copyright (c) Hugging Face (the Distil-Whisper authors)

## v1.0 - Voice Synthesis (tts_v1) and Hebrew Add-on (tts_he_v1)

`tts_v1`: ONNX exports of the Chatterbox Multilingual text-to-speech model and
the supporting feature and voice models it bundles, weights unchanged.

- Chatterbox (overall model, T3 token model, packaging)
  https://github.com/resemble-ai/chatterbox
  https://huggingface.co/ResembleAI/chatterbox
  License: MIT  (see `LICENSE-MIT.txt`), Copyright (c) 2025 Resemble AI
- S3Gen flow-matching synthesizer, HiFT vocoder, S3 speech tokenizer, CAMPPlus
  x-vector (CosyVoice lineage), https://github.com/FunAudioLLM/CosyVoice
  License: Apache-2.0  (see `LICENSE-Apache-2.0.txt`)
  Copyright (c) 2024 Alibaba Inc (authors: Xiang Lyu, Zhihao Du, Kai Hu, and others)
- Conformer / encoder building blocks (ESPnet / WeNet lineage)
  License: Apache-2.0  (see `LICENSE-Apache-2.0.txt`)
  Copyright (c) 2019 Shigeki Karita
  Copyright (c) 2020 Johns Hopkins University (author: Shinji Watanabe)
  Copyright (c) 2020, 2021 Mobvoi Inc (authors: Binbin Zhang, Di Wu)
- Voice encoder (speaker embedding), adapted from Real-Time-Voice-Cloning
  https://github.com/CorentinJ/Real-Time-Voice-Cloning
  License: MIT  (see `LICENSE-MIT.txt`)
  Modified & original work Copyright (c) 2019 Corentin Jemine; original work
  Copyright (c) 2018 Rayhane Mama, (c) 2019 fatchord, (c) 2015 braindead

`tts_he_v1`: `dicta_menaked.onnx`, the Hebrew diacritization model.

- Derivative of `dicta-il/dictabert-large-char-menaked`
  https://huggingface.co/dicta-il/dictabert-large-char-menaked
- Changes: exported from PyTorch to ONNX, weights stored as 16-bit floating point.
- License: CC-BY-4.0, https://creativecommons.org/licenses/by/4.0/
- Copyright (c) DICTA: The Israel Center for Text Analysis

These packs are not affiliated with or endorsed by Resemble AI, Alibaba, DICTA,
or the other upstream authors. They redistribute their work, in ONNX form, under
the terms of the licenses above.

## v1.1.0 - Voice Synthesis Changer Add-on (Speech Super-Resolution 48k)

- ONNX re-export of `alibabasglab/MossFormer2_SR_48K`
  https://huggingface.co/alibabasglab/MossFormer2_SR_48K
  from the ClearerVoice-Studio project, https://github.com/modelscope/ClearerVoice-Studio
  (the super-resolution transformer and its HiFi-GAN vocoder folded into one
  waveform-to-waveform graph, mel front-end included; both upstream checkpoints,
  weights unchanged)
- License: Apache-2.0  (see `LICENSE-Apache-2.0.txt`)
- Copyright (c) Alibaba Group (the ClearerVoice-Studio authors)

## v1.2.0 - Voice Synthesis Creation Denoise Add-on (Speech Enhancement 48k)

- ONNX export of `alibabasglab/MossFormer2_SE_48K`
  https://huggingface.co/alibabasglab/MossFormer2_SE_48K
  from the ClearerVoice-Studio project, https://github.com/modelscope/ClearerVoice-Studio
  (the filterbank front end, the mask network and the inverse transform folded
  into one waveform-to-waveform graph, weights unchanged)
- License: Apache-2.0  (see `LICENSE-Apache-2.0.txt`)
- Copyright (c) Alibaba Group (the ClearerVoice-Studio authors)

## v1.3.0 - Cross-Language Detection (VoxLingua107 language identification)

- ONNX export of `speechbrain/lang-id-voxlingua107-ecapa`
  https://huggingface.co/speechbrain/lang-id-voxlingua107-ecapa
  from the SpeechBrain project, https://github.com/speechbrain/speechbrain
  (the mel front end folded into the graph, weights unchanged)
- License: Apache-2.0  (see `LICENSE-Apache-2.0.txt`)
- Copyright (c) the SpeechBrain authors
- The model was trained on the VoxLingua107 dataset (CC-BY-4.0).

## v1.4.0 - Voice Synthesis vocoder update (tts_v1)

- `hift_vocoder_v1.4.0.onnx`: ONNX export of the S3Gen HiFT vocoder from
  Resemble AI's Chatterbox, https://github.com/resemble-ai/chatterbox
  (weights unchanged)
- Modified file: the two random-number operations in the vocoder's sine
  source (the harmonics' start phases and the noise bed) are removed and
  exposed as graph inputs (`sine_phase`, `sine_noise`), so the caller supplies
  them. The rest of the graph is unchanged.
- License: MIT  (see `LICENSE-MIT.txt`), Copyright (c) 2025 Resemble AI
- The vocoder code is adapted from CosyVoice,
  https://github.com/FunAudioLLM/CosyVoice, Apache-2.0  (see
  `LICENSE-Apache-2.0.txt`), Copyright (c) 2024 Alibaba Inc (authors:
  Xiang Lyu, Kai Hu)
- Used by FaceCue 1.0.2 and later in place of the `v1.0` `hift_vocoder.onnx`,
  which earlier versions keep using.
