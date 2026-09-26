---
id: w05-rahafaa2-knn-correlated-euclidean
title: "Euclidean Distance and Correlated Predictors"
author: "Rahaf Alabdullah (rahafaa2)"
---

Euclidean distance in k-NN treats predictors as independent axes, so highly correlated features get extra implicit weight since shared information is counted twice. The lecture shows Mahalanobis distance fixes this using the covariance matrix. If we still use Euclidean distance on correlated predictors, what happens to neighbor selection and predictions? Does standardizing variables help, or is Mahalanobis distance necessary?
