# serving-stack

The one system this course builds. This repository contains my work throughout the AI Data Center Bootcamp.

## What is here

The repository is organized by week and day. Each branch contains the work completed for that activity.

## What you add, and when

| Week | Day | What you add |
|---|---|---|
| 1 | D1 | W1D1 work |
| 1 | D2 | W1D2 work |
| 2 | D1 | W2D1 work |

---

## W1D1

Work completed during Week 1 Day 1.

---

## W1D2

Work completed during Week 1 Day 2.

---

## W2D1: What Can My Own Laptop Run?

### My Machine

| Field | My Specs |
|---|---|
| OS | Windows |
| System RAM | 32 GB |
| GPU | NVIDIA GeForce RTX 4060 |
| Dedicated VRAM | 8 GB |
| Unified Memory | No |
| GPU Type | Discrete GPU |

### Memory Ceiling

Using **7.0 GB** of usable GPU memory and **1.5 GB** of overhead:

| Precision | Bytes per Parameter | Maximum Model Size |
|---|---:|---:|
| FP32 | 4 | 1.4B |
| FP16 | 2 | 2.8B |
| INT8 | 1 | 5.5B |
| INT4 | 0.5 | 11.0B |

### Questions

**1. At INT4, what is the largest model I could run locally?**

My calculated INT4 ceiling is **11.0B parameters**. A real model below this ceiling is **Qwen2.5-7B-Instruct**.

**2. How much does moving from FP16 to INT4 buy me?**

Moving from FP16 to INT4 gives approximately a **4× increase** in theoretical parameter capacity.

**3. My laptop versus a 15 GB T4**

My laptop has **7.0 GB of usable VRAM**, while a T4 has **15 GB**, so the T4 can run a larger model based on memory capacity.

**4. What did I subtract for overhead?**

I used **1.5 GB** of overhead for the runtime, activations, and KV cache.

### Output

The results are saved in `my_machine.json`.
