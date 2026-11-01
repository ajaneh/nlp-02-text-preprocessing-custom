# Web Mining and Applied NLP Project Report

Alex Heyert | Project 02 | 2026-11

Here are a few limitations. the reviews ARE NOT evenly distributed at all. a high review of 5 dominates the combined values of the first 4 ratings

First I followed the example and combined all of the text from reviews into a corpus and noticed an increase in words after puncutation, I identified one reason and fixed it
counts before removing contractions were:
│ raw tokens                ┆ 1362913 │
│ after punctuation removal ┆ 1398169 │
│ after stop word removal   ┆ 784494 |

after change:
│ raw tokens                ┆ 1362913 │
│ after punctuation removal ┆ 1373258 │
│ after stop word removal   ┆ 786415 |
So it did make a difference. But there are still extra words
```
# 1. NEW STEP: Strip apostrophes inside contractions first (e.g., "don't" -> "dont")
# This targets apostrophes only when sandwiched between letters, preserving words.
no_contraction_text: str = re.sub(r"(?<=[a-z])'(?=[a-z])", "", lower_text)
```

## Overview

This project introduces text preprocessing
as a foundation for natural language processing.

The objective is to demonstrate how raw text
can be tokenized, normalized, cleaned,
and prepared for systematic analysis.

The project compares the results of
different preprocessing operations
to show how cleaning decisions affect
the representation of text.

## Tools and Methods

The project uses:

- Python with Polars for text processing and analysis.
- A kaggle dataset was downloaded to be a local file for input data.
- Regular expressions for punctuation removal.
- Tokenization for separating text into words.
- Lowercasing for text normalization. DID IT?
- Stopword filtering for reducing common vocabulary.
- Polars for calculating token frequencies.
- Matplotlib for visualizing preprocessing results.
- Logging for execution records. NO, the notebook doesn't support logging yet
- Ruff, ty, and pytest for code verification. It does use those things but tests haven't been built for the notebook.
- Zensical and GitHub Pages for published documentation.

The example script reads X,
combines them ?,
and applies a sequence of preprocessing operations.

The analysis compares raw and cleaned token counts
and identifies frequently occurring words.

## Verification

This will be rewritten for the notebook.
A successful execution displays:

    Pipeline executed successfully!

The script records execution details in a project log.

The output includes token counts,
frequency distributions,
and preprocessing comparison charts.

Automated tests provide additional verification
of the project's expected behavior.

## Interpretation




## Project Links

- [GitHub Repository](https://github.com/ajaneh/nlp-02-text-preprocessing-custom)
- [Example Script](https://github.com/denisecase/nlp-02-text-preprocessing/blob/main/src/nlp/text_preprocessing.py)
- [Example Notebook](https://github.com/ajaneh/nlp-02-text-preprocessing-custom/blob/main/notebooks/text_preprocessing.ipynb)
- [Example Data](https://github.com/ajaneh/nlp-02-text-preprocessing-custom/blob/main/data/clothing_reviews.csv)

## Project Resources

- [Project Instructions](project-instructions.md)
- [Professional Python Guide](https://denisecase.github.io/pro-analytics-02/)
- [Professional Python Project Explainer](https://pup-pack.github.io/professional-python-project-explainer/)
