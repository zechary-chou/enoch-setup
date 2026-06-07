# Enoch Openclaw Setup

This is my personal repository of how I setup OpenClaw on my Raspberry pi that's connected to my personal laptop with GPU.

## GOAL

- Feel like Ironman with Jarvis (LOL) but broke. 
- Optimizing for speed and accuracy all while not spending a single penny for tokens.
- Learn about LLM security, monitoring,

#Project Details

##Laptop Specs 
- RTX 4060
- 8GB VRAM
- 64GB DDR5 RAM
- 2TB SSD
- 13th Gen Intel Core i7-13620H

##Raspberry Pi
- Raspberry Pi Model B 4GB RAM
- 64bit ARM core

##Technical Setup
- Ollama hosted on laptop on WSL2
- Raspberry pi runs OpenClaw that connects to Laptop to access Ollama local + cloud models

##Approach

There are 3 main architectures I want to experiment with to see which one is the best for my setup/hardware:
- 1 main cloud agent (gpt-oss:120b-cloud) that does all the work
- 1 main orchestrator/conductor (gpt-oss:120b-cloud) cloud agent for complex thinking and delegation of small tasks to specialized agents like researcher (gpt-oss:20b-cloud), coder (qwen2.5:7b), and aide (qwen3:8b).
- 1 SLM router agent (qwen2.5:0.5b or 1.5b) that routes requests to cloud orchestrator for complex or smaller local agents (researcher, coder, aide, etc.). Conductor should still be able to delegate to local agent.

Important note: 
- performed aggressive prompt trimming on local agents due to limited context window (4k) for local models
- 3rd Architecture inspired by this [paper](https://arxiv.org/html/2606.03557v1#S5.T2)

##Future direction:
- switching over to llama.cpp for optimization of hardware resources to host bigger models with more context windows and better concurrency
- benchmarking each general architecture for speed, token consumption, and accuracy
- monitoring of devices with Prometheus + Grafana
- connect another dusty laptop to host small models
