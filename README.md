# ConsistPRM

**ConsistPRM: Evaluating and Improving Logical Consistency in LLM Reasoning via Transformation-Invariant Probes**

Submitted to the ICLR 2026 Workshop on Logical Reasoning of LLMs.

## Overview

This paper argues that accuracy on isolated logic problems is an incomplete measure of LLM reasoning ability. We propose evaluating logical *consistency* as invariance under truth-preserving transformations.

### Key Contributions

1. **ConsistBench** -- A diagnostic benchmark of 162 base instances with 573 Z3-verified transformation probes across entailment, negation, contrapositive, and transitivity. Introduces two complementary metrics: *commutation consistency* (self-agreement under transformation) and *probe correctness* (agreement with ground truth).

2. **The Negation Consistency Gap** -- A cross-model finding where models achieving 82-95% base accuracy score only 5-14% on negation probes. This failure persists across GPT-4o, Claude 3.5 Sonnet, Llama-3.1-70B, Qwen2.5-72B, Mistral-Large-2, and Llama-3.1-8B. We identify three failure modes: negation blindness, polarity inversion, and scope confusion.

3. **ConsistPRM** -- A process reward model for step-level consistency scoring. Z3-verified step labels (+12.4% consistency) substantially outperform heuristic (+2.1%) and LLM-judge labels (+5.8%), identifying formal supervision quality as the critical bottleneck.

## Repository Structure

```
paper/
  iclr2026/
    iclr2026_conference.tex   # Main paper (LaTeX source)
    references.bib             # Bibliography
    iclr2026_conference.pdf    # Compiled paper
    iclr2026_conference.sty    # ICLR 2026 style file
    iclr2026_conference.bst    # Bibliography style
    math_commands.tex          # Math notation macros
    fancyhdr.sty               # Header/footer style
    natbib.sty                 # Citation style
```

## Building the Paper

```bash
cd paper/iclr2026
pdflatex iclr2026_conference.tex
bibtex iclr2026_conference
pdflatex iclr2026_conference.tex
pdflatex iclr2026_conference.tex
```

## Citation

```bibtex
@inproceedings{consistprm2026,
  title={ConsistPRM: Evaluating and Improving Logical Consistency in LLM Reasoning via Transformation-Invariant Probes},
  author={Anonymous},
  booktitle={ICLR 2026 Workshop on Logical Reasoning of LLMs},
  year={2026}
}
```
