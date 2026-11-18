# Dataset Card: Reversibility Awareness

## Dataset Overview

This dataset supports the project *Do AI Agents Know Which Actions Cannot Be Undone?*

It contains labelled examples designed to study how actions differ in terms of reversibility.

## Dataset Files

| File | Description |
|---|---|
| `reversibility_dataset.jsonl` | Complete labelled dataset |
| `train.jsonl` | Training split |
| `test.jsonl` | Testing split |

## Dataset Size

- Complete dataset: approximately 0.67 MB
- Training split: approximately 0.54 MB
- Testing split: approximately 0.13 MB

## Labels

The project uses three reversibility categories:

1. Reversible
2. Partially reversible
3. Irreversible

## Intended Use

The dataset is used for training and evaluating linear probes that investigate whether a language model's internal representations encode information about action reversibility.

It is also used in the project's direct-answer evaluation.

## Limitations

The dataset is manually authored. Independent human annotation agreement and inter-annotator reliability have not been established.

Results should therefore be interpreted in the context of this dataset and its scenario design.

## Data Format

The dataset is stored in JSONL format, with one JSON record per line.
