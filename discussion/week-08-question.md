---
id: w08-rahafaa2-svm-primal-vs-dual-genes
title: "Primal or Dual for Many-Feature Data?"
author: "Rahaf Alabdullah (rahafaa2)"
---

What if a hospital wants to classify tumors as malignant or benign using a soft-margin SVM, but they only have $n = 60$ patients and $p = 20{,}000$ gene expression features? The primal problem optimizes over $\beta_0$, $\beta \in \mathbb{R}^{p}$, and $\xi_1, \dots, \xi_n$, while the dual optimizes only over $\alpha_1, \dots, \alpha_n$ and depends on the data only through the inner products $\langle x_i, x_j \rangle$. In this situation, would it be better to solve the primal or the dual? What if the situation were reversed, with $n = 1{,}000{,}000$ patients and only $p = 10$ features?
