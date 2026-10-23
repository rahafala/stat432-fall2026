---
id: w09-rahafaa2-kernel-choice-collinear
title: "Linear or Radial Kernel for Collinear Data?"
author: "Rahaf Alabdullah (rahafaa2)"
---

Suppose we have high-dimensional data ($p \gg n$) where many features are highly collinear. What are the advantages and disadvantages of fitting an SVM with a linear kernel $K(x, x') = \langle x, x' \rangle$ versus a radial kernel $K(x, x') = \exp(-\gamma \lVert x - x' \rVert^2)$? In particular, how does collinearity affect each kernel's interpretability, risk of overfitting, and tuning?
