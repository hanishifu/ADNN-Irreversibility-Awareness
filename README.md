# ADNN-Irreversibility-Awareness
Investigating whether AI agents understand and act on irreversible actions.
# Do AI Agents Know Which Actions Cannot Be Undone?

## Project Overview

This project investigates whether AI agents can recognise irreversible actions and whether that knowledge is reflected in their actual behaviour.

We study three main research questions:

- **RQ1:** Can reversibility information be decoded from the model's internal representations?
- **RQ2:** Can the model correctly state whether an action is reversible, partially reversible, or irreversible?
- **RQ3:** Does the agent behave more cautiously when performing irreversible actions compared with reversible actions?

## Model and Environment

- **Model:** Qwen/Qwen2.5-7B-Instruct
- **Quantisation:** 4-bit NF4
- **Transformer layers:** 28
- **Hidden size:** 3584
- **Experiments:** Internal representation probing, direct reversibility classification, and simulated agent behaviour.

## Repository Structure

```text
ADNN-Irreversibility-Awareness/
│
├── ADNN_Irreversibility_Project_FINAL.ipynb
├── ADNN_Reversibility_Report_Combined.pdf
├── ADNN_Reversibility_Report_Combined.docx
├── requirements.txt
├── README.md
│
├── qwen_probe_results.csv
├── qwen_direct_answers.csv
└── RQ3_FINAL_ALL_120_RUNS.csv
```

## Key Results

### RQ1 — Internal Representation Probing

- 29 layer positions were evaluated.
- Balanced accuracy was 1.00 at positions 1–28.
- The embedding-layer baseline achieved 0.3333 balanced accuracy.
- The full-text TF-IDF baseline also achieved 1.00, indicating a potential lexical or template shortcut.

These results demonstrate decodability on the current dataset, not necessarily semantic understanding.

### RQ2 — Direct Reversibility Classification

- 60 examples were evaluated.
- Overall accuracy: 81.67%.
- Balanced accuracy: 81.67%.
- Macro F1-score: 80.84%.

The partially reversible class was the most difficult to identify.

### RQ3 — Agent Behaviour

- 60 paired scenarios were evaluated.
- 120 total runs were recorded.
- The agent showed different action-level caution rates between reversible and irreversible conditions.

The results and statistical analysis are documented in the final report.

## Limitations

The current experiments have several limitations:

- Only one model family was evaluated.
- A second testbed was not completed.
- Some required probe controls and ablations remain incomplete.
- Repeated probe splits were not completed.
- Independent human annotation agreement was not established.
- The headline irreversibility blindness gap could not be reliably estimated from the available aligned predictions.

These limitations are discussed in the report.

## Software Requirements

See `requirements.txt` for the recorded package versions.

## Project Files

- **Notebook:** Contains the experimental workflow and saved outputs.
- **Probe results:** `qwen_probe_results.csv`
- **Direct-answer results:** `qwen_direct_answers.csv`
- **Agent behaviour results:** `RQ3_FINAL_ALL_120_RUNS.csv`
- **Report:** PDF and editable Word versions.

## Safety

All irreversible actions were evaluated in a simulated environment. No real files, email accounts, financial accounts, or external services were used for irreversible actions.
