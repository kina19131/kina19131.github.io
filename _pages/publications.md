---
layout: page
permalink: /publications/
title: Research
description: Ongoing projects and published work.
nav: true
nav_order: 3
---

<!-- _pages/publications.md -->

<h2 class="research-heading">Ongoing research</h2>

<div class="research-card">
  <div class="research-title">Robustness and Catastrophic Forgetting in LLM Fine-Tuning</div>
  <div class="research-meta">with <a href="https://www.sfu.ca/fas/computing/people/faculty/faculty-members/linyi-li.html" target="_blank" rel="noopener">Prof. Linyi Li</a>, Simon Fraser University &middot; 2026&ndash;present</div>
  <ul>
    <li>Designed an evaluation pipeline comparing SFT and GRPO to measure catastrophic forgetting during LLM adaptation.</li>
    <li>Investigating whether weight-space movement and robustness to parameter perturbations can predict forgetting beyond behavioral performance and KL-based measures.</li>
  </ul>
</div>

<div class="research-card">
  <div class="research-title">Representing and Searching Query Transformation Spaces</div>
  <div class="research-meta">IBM Db2 Query Optimization &middot; 2026&ndash;present</div>
  <ul>
    <li>Empirical study of how to represent and search large spaces of equivalent query transformations, comparing structured representations, learned embeddings, and Bayesian optimization for integration into the Db2 query compiler.</li>
  </ul>
</div>

<h2 class="research-heading">Publications</h2>

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}

</div>
<div class="caption">
    Interested in ML reliability, evaluation, robustness, and interpretability. If you'd like to collaborate, please reach out!
</div>

<style>
.research-heading {
  font-size: 0.75rem; font-weight: 600; letter-spacing: 0.08em;
  text-transform: uppercase; color: var(--global-text-color-light);
  padding-bottom: 0.6rem; margin: 1.5rem 0 0.85rem;
  border-bottom: 1px solid var(--global-divider-color);
}
.research-card {
  border: 1px solid var(--global-divider-color); border-radius: 10px;
  padding: 1rem 1.25rem; margin-bottom: 0.85rem;
}
.research-title { font-weight: 600; margin-bottom: 0.25rem; }
.research-meta { font-size: 0.82rem; color: var(--global-text-color-light); margin-bottom: 0.5rem; }
.research-card ul { padding-left: 1.1rem; margin: 0; font-size: 0.9rem; }
.research-card li { margin-bottom: 0.3rem; }
</style>
