# Coqui TTS Framework -- Complete Guide

## Overview

This project provides a full setup for using **Coqui TTS** for: -
Text-to-Speech (TTS) - Multilingual speech generation - Voice cloning
(XTTS v2) - Dialect and accent simulation

------------------------------------------------------------------------

## Requirements

-   Python 3.9 -- 3.11
-   Windows / Linux / macOS
-   8GB+ RAM recommended

------------------------------------------------------------------------

## Environment Setup

``` powershell
python -m venv .venv
.\.venv\Scripts\activate
```

### Install Dependencies

``` powershell
pip install --upgrade pip
pip install coqui-tts
pip install "transformers<5"
pip install torch torchaudio --index-url https://download.pytorch.org/whl/cpu
pip install torchcodec
```

------------------------------------------------------------------------

## Verify Installation

``` powershell
tts --list_models
```

------------------------------------------------------------------------

## Project Structure

    project/
    │
    ├── samples/
    │   ├── reference.wav
    │   ├── en_us.wav
    │   ├── en_uk.wav
    │   ├── ar_eg.wav
    │   ├── ar_gulf.wav
    │
    ├── outputs/
    ├── main.py
    └── README.md

------------------------------------------------------------------------

## Models Overview

  Model      Use Case
  ---------- ------------------------------
  xtts_v2    Multilingual + voice cloning
  jenny      Fast English
  vctk       Multi-speaker
  bark       Expressive
  tortoise   High quality

------------------------------------------------------------------------

## Basic Usage

### Simple TTS

``` powershell
tts --text "Hello world" --model_name "tts_models/en/jenny/jenny" --out_path output.wav
```

------------------------------------------------------------------------

## Voice Cloning (XTTS)

### Requirements

-   Reference WAV file
-   Language selection

### Example

``` powershell
tts --text "Hello Ahmed, this is cloned voice." `
    --model_name "tts_models/multilingual/multi-dataset/xtts_v2" `
    --language_idx en `
    --speaker_wav samples\reference.wav `
    --out_path outputs\cloned.wav
```

------------------------------------------------------------------------

## Multilingual Examples

### English

``` powershell
tts --text "Good morning" `
    --model_name "tts_models/multilingual/multi-dataset/xtts_v2" `
    --language_idx en `
    --speaker_wav samples\reference.wav `
    --out_path outputs\en.wav
```

### Arabic

``` powershell
tts --text "مرحبا أحمد، كيف حالك؟" `
    --model_name "tts_models/multilingual/multi-dataset/xtts_v2" `
    --language_idx ar `
    --speaker_wav samples\reference.wav `
    --out_path outputs\ar.wav
```

------------------------------------------------------------------------

## Dialects & Accents

Dialect is controlled by: 1. Reference voice 2. Text style

### Examples

  Dialect     Text
  ----------- ---------------
  Egyptian    إزيك يا أحمد
  Gulf        شلونك يا أحمد
  Levantine   كيفك يا أحمد

------------------------------------------------------------------------

## Creating Reference Audio

### Option 1: Record

-   Use Windows Voice Recorder
-   Speak 5 seconds
-   Export as WAV

### Option 2: Convert

``` powershell
ffmpeg -i input.mp3 -ar 24000 -ac 1 -c:a pcm_s16le reference.wav
```

------------------------------------------------------------------------

## Python Usage

``` python
from TTS.api import TTS

tts = TTS(model_name="tts_models/multilingual/multi-dataset/xtts_v2")

tts.tts_to_file(
    text="Hello Ahmed",
    file_path="output.wav",
    speaker_wav="samples/reference.wav",
    language="en"
)
```

------------------------------------------------------------------------

## Batch Generation Example

``` python
texts = ["Hello", "How are you", "Good morning"]

for i, t in enumerate(texts):
    tts.tts_to_file(
        text=t,
        file_path=f"outputs/out_{i}.wav",
        speaker_wav="samples/reference.wav",
        language="en"
    )
```

------------------------------------------------------------------------

## Troubleshooting

### Missing speaker_wav

→ Provide valid WAV file

### Audio errors

→ Convert to PCM WAV

### TorchCodec error

→ Use PyTorch 2.8 or install FFmpeg

------------------------------------------------------------------------

## Best Practices

-   Use clean audio (3--10 sec)
-   Keep samples organized
-   Use XTTS for multilingual
-   Freeze dependencies

``` powershell
pip freeze > requirements.txt
```

------------------------------------------------------------------------

## Storage Path

Downloaded models stored in:

    C:\Users\<user>\AppData\Local\tts

------------------------------------------------------------------------

## Notes

-   Models auto-download
-   Do not download all models (very large)
-   Focus on quality samples instead
