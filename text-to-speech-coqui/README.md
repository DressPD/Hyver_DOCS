# Coqui TTS Framework - Complete Guide

## Overview

This project provides a full setup for using **Coqui TTS** for:

- Text-to-Speech (TTS)
- Multilingual speech generation
- Voice cloning (XTTS v2)
- Dialect and accent simulation

---

## Requirements

- Python 3.9 - 3.11 (Recommended)
- Windows / Linux / macOS
- 8GB+ RAM recommended

> ⚠️ Python 3.13 works but may require workarounds (e.g. torch downgrade)

---

## Environment Setup

```powershell
python -m venv .venv
.\.venv\Scripts\Activate
```

### Install Dependencies

``` powershell
pip install --upgrade pip
pip install coqui-tts
pip install "transformers<5"
pip install torch==2.8.0 torchaudio==2.8.0 --index-url https://download.pytorch.org/whl/cpu
```
✅ Torch 2.8 avoids torchcodec + FFmpeg issues on Windows
------------------------------------------------------------------------

## Verify Installation

``` powershell
tts --list_models
```

------------------------------------------------------------------------

## Project Structure

    text-to-speech-coqui/
    │
    ├── samples/                 # Voice reference files
    │   ├── en-us_trump.wav
    │   ├── ar-ksa_01.wav
    │   ├── ar_01.wav
    │
    ├── output/                  # Generated audio
    ├── temp.wav                 # Working reference sample
    ├── command.txt
    └── README.md

------------------------------------------------------------------------

## Models Overview

  Model      Use Case
  ---------- ------------------------------
  xtts_v2    Multilingual + voice cloning
  jenny      Fast English
  vctk       Multi-speaker
  bark       Expressive speech
  tortoise   High quality (slow)

------------------------------------------------------------------------

## Basic Usage

### Simple TTS

``` powershell
tts --text "Hello world" --model_name "tts_models/en/jenny/jenny" --out_path output\basic.wav
```

------------------------------------------------------------------------

## Voice Cloning (XTTS)

### Requirements

-   Reference WAV file (3–10 seconds recommended)
-   Language selection

### Working Example (your setup)

``` powershell
    tts --text "
    What if you had an entire team of AI experts working for you?
    Writing code analyzing data researching automating tasks
    all in one place.
    Sounds crazy, right?
    Welcome to Hyver.
    ." `
    --model_name "tts_models/multilingual/multi-dataset/xtts_v2" `
    --language_idx en `
    --speaker_wav samples\en-us_trump.wav `
    --out_path output\Scene01_Hook.wav
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
### ⚠️ Important Notes About Reference Audio
Do NOT use:
- Huge files (like 400MB+)
- Long recordings (minutes)
 
Use instead:
- 3–10 seconds
- Clean voice
- No noise
------------------------------------------------------------------------
### Trim Large Files (Recommended)
``` powershell
ffmpeg -i samples\en-us_trump.wav -t 6 -ar 24000 -ac 1 samples\trump_short.wav
```
Then use:
``` powershell
--speaker_wav samples\trump_short.wav
```

------------------------------------------------------------------------
## Multilingual Examples
**English**
``` powershell
tts --text "Good morning" `
--model_name "tts_models/multilingual/multi-dataset/xtts_v2" `
--language_idx en `
--speaker_wav temp.wav `
--out_path output\en.wav
```

**Arabic**
``` powershell
tts --text "مرحبا أحمد، كيف حالك؟" `
--model_name "tts_models/multilingual/multi-dataset/xtts_v2" `
--language_idx ar `
--speaker_wav samples\ar-ksa_01.wav `
--out_path output\ar.wav
```

------------------------------------------------------------------------
## Dialects & Accents
Dialect is controlled by:
1. Reference voice
2. Text style

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
ffmpeg -i input.mp3 -ar 24000 -ac 1 -c:a pcm_s16le output.wav
```

------------------------------------------------------------------------

## Python Usage

``` python
from TTS.api import TTS

tts = TTS(model_name="tts_models/multilingual/multi-dataset/xtts_v2")

tts.tts_to_file(
    text="Hello Ahmed",
    file_path="output.wav",
    speaker_wav="temp.wav",
    language="en"
)
```

------------------------------------------------------------------------

## Batch Generation Example

``` python
texts = [
    "Hello",
    "How are you",
    "Good morning"
]

for i, t in enumerate(texts):
    tts.tts_to_file(
        text=t,
        file_path=f"output/out_{i}.wav",
        speaker_wav="temp.wav",
        language="en"
    )
```

------------------------------------------------------------------------

## Troubleshooting
❌ ```tts not recognized```
→ Activate ```.venv```

❌ ```reference.wav not found```
→ Use actual file name from ```samples```

❌ TorchCodec / FFmpeg error
→ Use:
```
torch==2.8.0
```
---
❌ Audio loading error

→ File is:
- missing
- corrupted
- wrong format
---
Best Practices
- Use short clean audio samples
- Keep files organized in /samples
- Use xtts_v2 for all multilingual work
- Avoid huge datasets as input

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
- Models download automatically on first use
- Do NOT download all models (very large)
- Focus on building a good voice sample library
