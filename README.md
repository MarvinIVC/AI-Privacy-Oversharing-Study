# AI Privacy Oversharing Study

This repository contains the supplemental dataset and documentation for the research paper:

**Helpful or Hazardous? Measuring Whether AI Assistants Encourage Privacy-Risky Oversharing in Everyday User Requests**

Author: **Marvin Wang**

## Overview

This study evaluates whether consumer AI assistants protect user privacy or amplify oversharing when users provide sensitive information in ordinary drafting requests. The benchmark contains **360 model responses** from:

- **60 base scenarios**
- **10 privacy-sensitive categories**
- **3 prompt conditions**
- **2 AI assistants**

The two assistants are coded as:

- `Assistant_1` = ChatGPT 5.5 Instant
- `Assistant_2` = Gemini 3.5 Flash

## Research Design

Each base scenario was tested under three prompt conditions:

1. **Neutral** — the user includes sensitive information without special privacy instruction.
2. **Convenience Pressure** — the user asks the assistant to include details exactly or avoid privacy warnings.
3. **Privacy-Aware** — the user asks the assistant to protect privacy and use placeholders where appropriate.

The benchmark uses only **synthetic realistic stimuli**. No real personal information, credentials, banking details, medical records, student records, or private user data were collected or used.


## Main Dataset

The main response-level dataset is:

```text
data/scored_response_log.csv
```

The spreadsheet version with README, rubric, raw results, and summary sheets is:

```text
data/AI_Privacy_Oversharing_Raw_Results_Appendix.xlsx
```

## Main Outcome Variable

The main outcome variable is **Privacy Protection Score (PPS)**, calculated as the average of five 1–5 rubric dimensions:

1. Sensitive Data Recognition
2. Redaction Guidance
3. Data Minimization
4. Safe Helpfulness
5. Risk Communication

See [`CODEBOOK.md`](CODEBOOK.md) for full column definitions and scoring rules.

## Data Ethics

All data in this repository are synthetic or model-generated. The prompts use realistic-looking but non-real details to reduce experimental artifacts while avoiding collection of actual sensitive information.



## License

This repository is released under the Creative Commons Attribution 4.0 International License. See [`LICENSE`](LICENSE).
