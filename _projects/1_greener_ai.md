---
layout: page
title: Greener AI — LLM Carbon Benchmarking
description: IEEE ICECET 2026 — Benchmarking carbon emissions across FP32, FP16, INT8, INT4 quantization on Tesla T4 GPUs
img:
importance: 1
category: AI/ML Research
related_publications: true
---

This project investigates the energy efficiency and carbon footprint of large language models across multiple quantization precision modes on Azure GPU infrastructure.

Key finding: INT8/INT4 quantization — commonly assumed to reduce energy consumption — paradoxically increases CO2 emissions on Tesla T4 GPUs due to dequantization overhead. FP16 delivers the best quality-to-efficiency ratio across all three benchmarks tested (XSum, SQuAD, ARC-Challenge).

Technical stack: Python, Hugging Face Transformers, PyTorch, CodeCarbon, Streamlit, Azure GPU VM

Highlights:

- Ran 20+ instrumented experiments across 4 precision modes and 3 NLP tasks
- Tracked per-run emissions and latency with CodeCarbon
- Built a Streamlit dashboard for reproducible comparison of results
- Research accepted at IEEE ICECET 2026, co-authored with Prof. Duy Ho, CSU Fullerton
