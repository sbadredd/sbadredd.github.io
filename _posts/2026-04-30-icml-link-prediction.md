---
layout: post
title: On the Theoretical Limitations of Embedding-based Link Prediction
date: 2026-04-30 12:00:00-0400
description: Why most knowledge graph embeddings fail to scale to large graphs, and how a Mixture of Softmaxes fixes it.
tags: neurosymbolic link-prediction knowledge-graphs ICML
categories: research
related_posts: false
---

**Full paper:** [arxiv.org/abs/2506.22271](https://arxiv.org/abs/2506.22271)

We show a structural limitation which prevents most knowledge graph embeddings from scaling to large graphs. Link prediction is how we fill gaps in knowledge graphs. Most approaches encode queries into low-dimensional embeddings and decode linearly to (much) larger answer spaces, which introduces a bottleneck.

This matters regardless of the encoder you use (GNNs, LLMs, ...). We show how it behaves across different task objectives and then break the limitation by adapting a Mixture of Softmaxes from the LLM literature. 🔨 We derive an output layer that can be equiped on most KGE models and find it improves their performance on large graphs at a low parameter cost.

TL;DR: Let's focus on decoders, not just encoders! 💡

<div class="row justify-content-center">
    <div class="col-12">
        <iframe src="{{ '/assets/html/icml-link-prediction.html' | relative_url }}"
                frameborder="0"
                scrolling="no"
                style="width: 100%; height: 680px; border: none;"
                title="Link prediction bottleneck visualization"></iframe>
    </div>
</div>

For more visualizations of bottlenecks in output layers (classification and rankings which we also discuss in the paper), check also [the website of Andreas Grivas](https://grv.unargmaxable.ai/viz) !
