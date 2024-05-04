---
title: "Resources"
sitemap: false
permalink: /resources.html
---


### Some resources I've found interesting or useful (all are free)
- [Eugene Yan: List of Applied ML Papers/tech blogs on ML in production](https://github.com/eugeneyan/applied-ml?tab=readme-ov-file)
- [Eugene Yan: Language Modeling Reading List (to Start Your Paper Club)](https://eugeneyan.com//writing/llm-reading-list/)
- [How Prototyping Can Help You to Get Buy-In](https://eugeneyan.com/writing/prototyping-to-get-buy-in/)
- [Chip Huyen: Building LLM applications for production](https://huyenchip.com/2023/04/11/llm-engineering.html)
- [Chip Huyen: Llama Police -- A dashboard of Open Source LLM Tools](https://huyenchip.com/llama-police)
- [Eugene Yan's List of Open-source LLMs](https://github.com/eugeneyan/open-llms)
- [Erik Linder-Norén: Machine Learning From Scratch: Python implementations of fundamental algorithms from scratch](https://github.com/eriklindernoren/ML-From-Scratch/tree/master)
- [Stas Bekman - Machine Learning Engineering](https://github.com/stas00/ml-engineering?tab=readme-ov-file)
    - Excerpt: 
    > Tell how many GPUs do you need in 5 secs
    >    * Training in half mixed-precision: model_size_in_B * 18 * 1.25 / gpu_size_in_GB
    >    * Inference in half precision: model_size_in_B * 2 * 1.25 / gpu_size_in_GB
    >    
    >    That’s the minimum, more to have a bigger batch size and longer sequence length.
    >    Here is the breakdown:
    >    * Training: 8 bytes for AdamW states, 4 bytes for grads, 4+2 bytes for weights
    >    * Inference: 2 bytes for weights (1 byte if you use quantization)
    >    * 1.25 is 25% for activations (very very approximate)
    >    
    >    For example: Let’s take an 80B param model and 80GB GPUs and calculate how many of them we will need for:
    >    * Training: at least 23 GPUs 80*18*1.25/80
    >    * Inference: at least 3 GPUs 80*2*1.25/80