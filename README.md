# 🎧 SERTUS: Speech Emotion Recognition in Tunisian Spontaneous Dialect

## Overview

SERTUS is a spontaneous speech emotion recognition corpus built from Tunisian Arabic broadcast materials. The corpus is annotated with both categorical and dimensional (VAD) emotion labels.

## 🛠️ Data Collection and Annotation Pipeline

➡️ [Click here to see the full pipeline](Pipeline.md)

Or scroll below for a summary:

| Step | Task                                                       | Tool                            |
|------|------------------------------------------------------------|---------------------------------|
| 1    | Selection of Tunisian spontaneous speech from YouTube      | Manual search (legally justified) |
| 2    | Extraction, silence reduction, anonymization               | WavePad                         |
| 3    | Dimensional annotation (Valence, Arousal, Dominance)       | CARMA                           |
| 4    | Categorical annotation (6 basic emotions)                  | Manual (majority vote)          |

## 📁 Data

- Audio format: `.wav`, 44.1 kHz
- Number of speakers: 1259
- Segments: 3793
- Annotated duration: >23 hours

## ⚖️ Legal Note

In Tunisia, fair use of copyrighted broadcast material is allowed under Law No. 94-36...
