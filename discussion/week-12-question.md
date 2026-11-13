---
id: w12-rahafaa2-when-spectral-clustering
title: "How Do We Know We Need Spectral Clustering?"
author: "Rahaf Alabdullah (rahafaa2)"
---

The lecture shows ring-shaped data where k-means fails and spectral clustering recovers the true groups. In practice, though, we often do not know the real shape of the data, especially in high dimensions where we cannot simply plot it. How do we know in advance that the clusters are ring-shaped (or otherwise non-convex), that k-means will fail, and that we need spectral clustering instead? Are there diagnostics we can use to decide between the two methods when the true shape is unknown?
