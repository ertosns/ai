# AI and Machine Learning: Mathematics with Algorithmic Implementation

A book-length set of notes deriving the mathematics behind modern machine
learning, from logistic regression up through deep networks, computer vision,
sequence models, and probabilistic graphical models, with the algorithmic
steps (forward/backward propagation, optimization) worked out by hand.

**Author:** Mohab M. Metwally. **Started:** 2020.

## 📄 Read the PDF

- **View online:** https://github.com/ertosns/ai/blob/main/ml.pdf
- **Download (raw):** https://github.com/ertosns/ai/raw/main/ml.pdf

> GitHub renders the PDF directly in the browser via the *View online* link.

## Contents

1. **Logistic Regression as a neural network**: cost function, gradient
   descent, forward/backward propagation, Python implementation.
2. **Neural Networks**: initialization, deep nets, optimization (momentum,
   RMSprop, Adam, learning-rate decay), batch normalization, multi-class
   classification, SVM, intro to unsupervised learning.
3. **Structuring Machine Learning**: ML strategy, orthogonality,
   train/dev/test sets, human-level performance, error analysis, multi-task
   and end-to-end learning.
4. **Computer Vision**: convolutions, Inception, object detection, bounding
   box prediction, neural style transfer.
5. **Recurrent Neural Networks (RNN)**: forward/backward propagation through
   time, language models, vanishing/exploding gradients, deep RNNs, word
   representation, sequence-to-sequence, attention.
6. **Probabilistic Graphical Models (PGM)**: Bayesian networks, reasoning
   patterns, d-separation, naive Bayes, template models, structured CPDs.
7. **Natural Language Processing**: pre-processing, logistic-regression and
   naive-Bayes classifiers, probabilistic pronunciation/spelling models.

**Appendices:** probabilities, covariance, singular value decomposition,
exponentially weighted averages, smoothing (add-k / Laplacian), kernels and
convolution functions.

## Building from source

The document is a single LaTeX source, `ml.tex`. It uses `tikz`/`pgfplots`
for all figures (no external image assets).

```sh
# with latexmk (recommended)
latexmk -pdf ml.tex

# or manually (run twice to resolve references, plus makeindex/bibtex)
pdflatex ml.tex
makeindex ml.idx
bibtex ml
pdflatex ml.tex
pdflatex ml.tex
```

Requires a TeX distribution (TeX Live / MiKTeX) with `amsmath`, `hyperref`,
`natbib`, `tikz`, `pgfplots`, `subcaption`, `chapterbib`, `accents`, and
`index`.

Build artifacts (`.aux`, `.log`, `.toc`, ...) are git-ignored; only `ml.tex`
and the generated `ml.pdf` are tracked.

## Status

Originally drafted in 2020 and ratified in 2026. The appendices, the empty
"Summary"/"in Python" sections, and all previously-outstanding `%TODO`
markers have been completed; the source compiles cleanly to a 139-page PDF.
Remaining polish is a broader copy-edit pass and adding worked code to the
CNN/RNN/PGM/NLP chapters.

## License

Copyright (c) 2020-2026 Mohab M. Metwally.

This work is licensed under a
[Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).
You are free to share and adapt the material for any purpose, even
commercially, as long as you give appropriate credit. See the [LICENSE](LICENSE)
file for the full legal text.
