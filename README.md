# NatureLM-CaneToad-Detection_Group_19

NatureLM-audio-based cane toad (*Rhinella marina*) vocalisation detection using bioacoustic recordings from the Australian Acoustic Observatory (A2O).

---

# NatureLM Cane Toad Detection

## Project Overview

This project investigates the use of NatureLM-audio, a large audio-language foundation model developed by the Earth Species Project, for detecting cane toad (*Rhinella marina*) vocalisations from environmental audio recordings.

The study evaluates the ability of NatureLM-audio to identify cane toad sounds using a zero-shot inference approach without additional model training or fine-tuning.

---

## Environment Configuration

### Local Environment

* Windows 11
* Windows PowerShell
* Python 3.10+

### Cloud Environment

* Google Colab Pro
* NVIDIA A100 GPU
* Google Drive (persistent storage)

### Main Dependencies

* transformers==4.44.2
* tokenizers==0.19.1
* peft==0.11.1
* accelerate==0.33.0
* librosa
* soundfile
* sentencepiece
* mir_eval
* resampy

---

## Dataset

Source:

* Australian Acoustic Observatory (A2O)

Dataset Characteristics:

* 22,006 labelled cane toad recordings
* FLAC audio format
* Approximately 3 seconds per recording

Dataset access information is provided in:

```text
audio_files.txt
```

---

## Repository Structure

```text
NatureLM-CaneToad-Detection_Group_19/
│
├── code/
│   └── NatureLM-audio/
│
├── outputs/
│
├── main_gc_file.ipynb
├── requirements.txt
├── audio_files.txt
├── User_Manual.pdf
└── README.md
```

---

## Installation

Install required dependencies:

```bash
pip install -r requirements.txt
```

For additional installation guidance, refer to the User Manual and the official NatureLM-audio repository.

---

## Execution Steps

### Google Colab Workflow

1. Open `main_gc_file.ipynb` in Google Colab.
2. Enable GPU acceleration.
3. Mount Google Drive.
4. Configure Hugging Face authentication.
5. Upload audio recordings to the project directory.
6. Execute notebook cells sequentially.
7. Monitor batch-processing progress.
8. Review generated outputs.

Recommended GPU:

* NVIDIA A100

---

## Outputs

NatureLM-audio generates outputs in JSONL format.

Each output entry typically contains:

* Audio file path
* User prompt
* Generated response
* Species identification information

Generated outputs are stored within:

```text
outputs/
```

and may also be saved directly to Google Drive depending on the execution workflow.

---

## Documentation

Additional project documentation is provided in:

```text
User_Manual.pdf
```

The user manual contains:

* Installation procedures
* Environment configuration
* Local execution instructions
* Google Colab setup
* Batch-processing workflow
* Troubleshooting guidance

---

## References

### NatureLM-audio

https://github.com/earthspecies/NatureLM-audio

### Australian Acoustic Observatory

https://acousticobservatory.org/

### Earth Species Project

https://www.earthspecies.org/
