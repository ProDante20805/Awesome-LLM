# Awesome-LLM [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

🔥 Large Language Models(LLM) have taken the ~~NLP community~~ **the Whole World** by storm. Here is a curated list of papers about large language models, especially relating to ChatGPT. It also contains frameworks for LLM training, tools to deploy LLM, courses and tutorials about LLM and all publicly available LLM checkpoints and APIs:

- [Awesome-LLM ](#awesome-llm-)
  - [Milestone Papers](#milestone-papers)
  - [ChatGPT Evaluation](#chatgpt-evaluation)
  - [LLM Training Frameworks](#llm-training-frameworks)
  - [Tools for using LLM](#tools-for-using-llm)
  - [Tutorials about LLM](#tutorials-about-llm)
  - [Courses about LLM](#courses-about-llm)
  - [Useful Resources](#useful-resources)
  - [Publicly Available LLM APIs](#publicly-available-llm-apis)
  - [Publicly Available LLM Checkpoints](#publicly-available-llm-checkpoints)
    - [BigScience/BLOOM](#bigsciencebloom)
    - [BigScience/T0](#bigsciencet0)
    - [Blink/RWKV](#blinkrwkv)
    - [Google/Flan-T5](#googleflan-t5)
    - [Meta/OPT](#metaopt)
    - [Meta/Galactica](#metagalactica)
    - [EleutherAI/GPT-NeoX](#eleutheraigpt-neox)
    - [Tsinghua/GLM](#tsinghuaglm)
  - [Contributing](#contributing)

## Milestone Papers

| <div style="width:60px">Year</div> | keywords     | Institute | Paper                                                        | Publication |
| :--: | :-----------: | :-------: | :----------------------------------------------------------- | :---------: |
| 2017-06 | Transformers |  Google   | [Attention Is All You Need](https://arxiv.org/pdf/1706.03762.pdf) |   NeurIPS   |
| 2018-06 | GPT 1.0      |  OpenAI   | [Improving Language Understanding by Generative Pre-Training](https://www.cs.ubc.ca/~amuham01/LING530/papers/radford2018improving.pdf) |             |
| 2018-10 | BERT         |  Google   | [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://aclanthology.org/N19-1423.pdf) |    NAACL    |
| 2019-02 | GPT 2.0      |  OpenAI   | [Language Models are Unsupervised Multitask Learners](https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf) |             |
| 2019-09 | Megatron-LM  | NVIDIA | [Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism](https://arxiv.org/pdf/1909.08053.pdf) ||
| 2019-10 | T5           |  Google   | [Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer](https://jmlr.org/papers/v21/20-074.html) |    JMLR     |
| 2020-01 | Scaling Law  |  OpenAI   | [Scaling Laws for Neural Language Models](https://arxiv.org/pdf/2001.08361.pdf) |             |
| 2020-05 | GPT 3.0      |  OpenAI   | [Language models are few-shot learners](https://papers.nips.cc/paper/2020/file/1457c0d6bfcb4967418bfb8ac142f64a-Paper.pdf) |   NeurIPS   |
| 2020-12 | LM-BFF | Princeton | [Making Pre-trained Language Models Better Few-shot Learners](https://arxiv.org/pdf/2012.15723.pdf) | ACL|
| 2021-08 | Codex | OpenAI | [Evaluating Large Language Models Trained on Code](https://arxiv.org/pdf/2107.03374.pdf) |  |
| 2021-08 | Foundation Models | Stanford |[On the Opportunities and Risks of Foundation Models](https://arxiv.org/pdf/2108.07258.pdf) |  |
| 2021-09 | FLAN | Google | [Finetuned Language Models are Zero-Shot Learners](https://openreview.net/forum?id=gEZrGCozdqR) | ICLR |
| 2021-12 | WebGPT | OpenAI | [WebGPT: Improving the Factual Accuracy of Language Models through Web Browsing](https://openai.com/blog/webgpt/) |  |
| 2021-12 | Retro | DeepMind | [Improving language models by retrieving from trillions of tokens](https://www.deepmind.com/publications/improving-language-models-by-retrieving-from-trillions-of-tokens) | ICML |
| 2022-01 | COT | Google | [Chain-of-Thought Prompting Elicits Reasoning in Large Language Models](https://arxiv.org/pdf/2201.11903.pdf) | NeurIPS |
| 2022-01 | LaMDA| Google | [LaMDA: Language Models for Dialog Applications](https://arxiv.org/pdf/2201.08239.pdf) |  |
| 2022-03 | InstructGPT | OpenAI | [Training language models to follow instructions with human feedback](https://arxiv.org/pdf/2203.02155.pdf) |  |
| 2022-04 | PaLM | Google | [PaLM: Scaling Language Modeling with Pathways](https://arxiv.org/pdf/2204.02311.pdf) |  |
| 2022-04 | Chinchilla| DeepMind | [An empirical analysis of compute-optimal large language model training](https://www.deepmind.com/publications/an-empirical-analysis-of-compute-optimal-large-language-model-training) | NeurIPS |
| 2022-05 | OPT | Meta | [OPT: Open Pre-trained Transformer Language Models](https://arxiv.org/pdf/2205.01068.pdf) |  |
| 2022-06 | Emergent Abilities | Google | [Emergent Abilities of Large Language Models](https://openreview.net/pdf?id=yzkSU5zdwD) | TMLR |
| 2022-06 | BIG-bench | Google | [Beyond the Imitation Game: Quantifying and extrapolating the capabilities of language models](https://github.com/google/BIG-bench) |  |
| 2022-06 | METALM | Microsoft | [Language Models are General-Purpose Interfaces](https://arxiv.org/pdf/2206.06336.pdf) |  |
| 2022-09 | Sparrow | DeepMind | [Improving alignment of dialogue agents via targeted human judgements](https://arxiv.org/pdf/2209.14375.pdf) |  |
| 2022-10 | Flan-T5 | Google | [Scaling Instruction-Finetuned Language Models](https://arxiv.org/pdf/2210.11416.pdf) |  |
| 2022-10 | GLM-130B | Tsinghua | [GLM-130B: An Open Bilingual Pre-trained Model](https://arxiv.org/pdf/2210.02414.pdf) | ICLR |
| 2022-11 | HELM | Stanford | [Holistic Evaluation of Language Models](https://arxiv.org/pdf/2211.09110.pdf) |  |
| 2022-11 | BLOOM | BigScience | [BLOOM: A 176B-Parameter Open-Access Multilingual Language Model](https://arxiv.org/pdf/2211.05100.pdf) |  |
| 2022-11 | Galactica | Meta | [Galactica: A Large Language Model for Science](https://arxiv.org/pdf/2211.09085.pdf) |  |
| 2023-01 | Flan 2022 Collection | Google | [The Flan Collection: Designing Data and Methods for Effective Instruction Tuning](https://arxiv.org/pdf/2301.13688.pdf) |  |

## ChatGPT Evaluation

- Is ChatGPT a General-Purpose Natural Language Processing Task Solver? [Link](https://arxiv.org/pdf/2302.06476.pdf)

- Is ChatGPT A Good Translator? A Preliminary Study [Link](https://arxiv.org/pdf/2301.08745.pdf)

## LLM Training Frameworks

<div align=center>
<img src="https://github.com/alpa-projects/alpa/blob/main/docs/logo/alpa-logo-cropped.png" width="120">
</div>  

> [Alpa](https://github.com/alpa-projects/alpa) is a system for training and serving large-scale neural networks. 
Scaling neural networks to hundreds of billions of parameters has enabled dramatic breakthroughs such as GPT-3, but training and serving these large-scale neural networks require complicated distributed system techniques. Alpa aims to automate large-scale distributed training and serving with just a few lines of code.


<div align=center>
<img src="https://raw.githubusercontent.com/microsoft/DeepSpeed/8be8c012c8a247e5512276676b5e7092d88633eb/docs/assets/images/DeepSpeed_light.svg">
</div>  

> DeepSpeed is an easy-to-use deep learning optimization software suite that enables unprecedented scale and speed for DL Training and Inference. Visit us at [deepspeed.ai](https://www.deepspeed.ai) or our [Github repo](https://github.com/microsoft/DeepSpeed).


<div align=center>
<img src="https://avatars.githubusercontent.com/u/1728152?s=200&v=4"  width="120" height="">
</div>  

> Megatron-LM could be visited [here](https://github.com/NVIDIA/Megatron-LM). Megatron ([1](https://arxiv.org/pdf/1909.08053.pdf), [2](https://arxiv.org/pdf/2104.04473.pdf), and [3](https://arxiv.org/pdf/2205.05198)) is a large, powerful transformer developed by the Applied Deep Learning Research team at NVIDIA. This repository is for ongoing research on training large transformer language models at scale. We developed efficient, model-parallel ([tensor](https://arxiv.org/pdf/1909.08053.pdf), [sequence](https://arxiv.org/pdf/2205.05198), and [pipeline](https://arxiv.org/pdf/2104.04473.pdf)), and multi-node pre-training of transformer based models such as [GPT](https://arxiv.org/abs/2005.14165), [BERT](https://arxiv.org/pdf/1810.04805.pdf), and [T5](https://arxiv.org/abs/1910.10683) using mixed precision.

<div align=center>
<img src="https://raw.githubusercontent.com/hpcaitech/public_assets/main/colossalai/img/colossal-ai_logo_vertical.png"  width="240" height="">
</div>  

> [Colossal-AI](https://colossalai.org) provides a collection of parallel components for you. We aim to support you to write your distributed deep learning models just like how you write your model on your laptop. We provide user-friendly tools to kickstart distributed training and inference in a few lines.

<div align=center>
<img src="https://github.com/OpenBMB/BMTrain/blob/main/docs/logo.png"  width="80" height="">
</div>  

> [BMTrain](https://github.com/OpenBMB/BMTrain) is an efficient large model training toolkit that can be used to train large models with tens of billions of parameters. It can train models in a distributed manner while keeping the code as simple as stand-alone training.


<div align=center>
<img src="https://camo.githubusercontent.com/aeb4f612bd9b40d81c62fcbebd6db44a5d4344b8b962be0138817e18c9c06963/68747470733a2f2f7777772e74656e736f72666c6f772e6f72672f696d616765732f74665f6c6f676f5f686f72697a6f6e74616c2e706e67"  width="240" height="">
</div> 

> [Mesh TensorFlow `(mtf)`](https://github.com/tensorflow/mesh) is a language for distributed deep learning, capable of specifying a broad class of distributed tensor computations. The purpose of Mesh TensorFlow is to formalize and implement distribution strategies for your computation graph over your hardware/processors. For example: "Split the batch over rows of processors and split the units in the hidden layer across columns of processors." Mesh TensorFlow is implemented as a layer over TensorFlow.


<div align=center>
<img src="https://jax.readthedocs.io/en/latest/_static/jax_logo_250px.png"  width="120" height="">
</div> 

> [This tutorial](https://jax.readthedocs.io/en/latest/notebooks/Distributed_arrays_and_automatic_parallelization.html) discusses parallelism via jax.Array.

## Tools for using LLM
🦜️🔗 [LangChain](https://github.com/hwchase17/langchain)

> Large language models (LLMs) are emerging as a transformative technology, enabling developers to build applications that they previously could not. But using these LLMs in isolation is often not enough to create a truly powerful app - the real power comes when you can combine them with other sources of computation or knowledge. This library is aimed at assisting in the development of those types of applications. Common examples of these types of applications include ❓ Question Answering over specific documents, 💬 Chatbots and 🤖 Agents.

👋 [wechat-chatgpt](https://github.com/fuergaosi233/wechat-chatgpt)

> Use ChatGPT On Wechat via wechaty

## Tutorials about LLM

- [ICML 2022] Welcome to the &#34;Big Model&#34; Era: Techniques and Systems to Train and Serve Bigger Models [Link](https://icml.cc/virtual/2022/tutorial/18440)

- [NeurIPS 2022] Foundational Robustness of Foundation Models [Link](https://nips.cc/virtual/2022/tutorial/55796)

- [Andrej Karpathy] Let's build GPT: from scratch, in code, spelled out. [Video](https://www.youtube.com/watch?v=kCc8FmEb1nY)|[Code](https://github.com/karpathy/ng-video-lecture)

- [DAIR.AI] Prompt Engineering Guide [Link](https://github.com/dair-ai/Prompt-Engineering-Guide)

- [Colossal-AI] Open source solution replicates ChatGPT training process! Ready to go with only 1.6GB GPU memory and gives you 7.73 times faster training! [Link](https://www.hpc-ai.tech/blog/colossal-ai-chatgpt)

## Courses about LLM

- [Stanford] CS224N-Lecture 11: Prompting, Instruction Finetuning, and RLHF [Slides](https://web.stanford.edu/class/cs224n/slides/cs224n-2023-lecture11-prompting-rlhf.pdf)

- [Stanford] CS324-Large Language Models [Homepage](https://stanford-cs324.github.io/winter2022/)

- [Stanford] CS25-Transformers United V2 [Homepage](https://web.stanford.edu/class/cs25/)

- [Stanford Webinar] GPT-3 & Beyond [Video](https://www.youtube.com/watch?v=-lnHHWRCDGk)

- [李沐] InstructGPT论文精读 [Bilibili](https://www.bilibili.com/video/BV1hd4y187CR/?spm_id_from=333.337.search-card.all.click&vd_source=1e55c5426b48b37e901ff0f78992e33f) [Youtube](https://www.youtube.com/watch?v=zfIGAwD1jOQ)

- [李沐] HELM全面语言模型评测 [Bilibili](https://www.bilibili.com/video/BV1z24y1B7uX/?spm_id_from=333.337.search-card.all.click&vd_source=1e55c5426b48b37e901ff0f78992e33f)

- [李沐] GPT，GPT-2，GPT-3 论文精读 [Bilibili](https://www.bilibili.com/video/BV1AF411b7xQ/?spm_id_from=333.788&vd_source=1e55c5426b48b37e901ff0f78992e33f) [Youtube](https://www.youtube.com/watch?v=t70Bl3w7bxY&list=PLFXJ6jwg0qW-7UM8iUTj3qKqdhbQULP5I&index=18)

- [Aston Zhang] Chain of Thought论文 [Bilibili](https://www.bilibili.com/video/BV1t8411e7Ug/?spm_id_from=333.788&vd_source=1e55c5426b48b37e901ff0f78992e33f) [Youtube](https://www.youtube.com/watch?v=H4J59iG3t5o&list=PLFXJ6jwg0qW-7UM8iUTj3qKqdhbQULP5I&index=29)

## Useful Resources
- [对话旷视研究院张祥雨｜ChatGPT的科研价值可能更大](https://zhuanlan.zhihu.com/p/606918875) \[2023-02-16][知乎][旷视科技]
- [关于ChatGPT八个技术问题的猜想](https://zhuanlan.zhihu.com/p/606478660) \[2023-02-15][知乎][张家俊]
- [ChatGPT发展历程、原理、技术架构详解和产业未来](https://zhuanlan.zhihu.com/p/590655677?utm_source=wechat_session&utm_medium=social&utm_oi=714896487502315520&s_r=0) \[2023-02-15][知乎][陈巍谈芯]
- [What Is ChatGPT Doing … and Why Does It Work?](https://writings.stephenwolfram.com/2023/02/what-is-chatgpt-doing-and-why-does-it-work/) \[2023-02-14][Stephen Wolfram]
- [对ChatGPT的二十点看法](https://zhuanlan.zhihu.com/p/605882945?utm_medium=social&utm_oi=939485757606461440&utm_psn=1609870392121860096&utm_source=wechat_session) \[2023-02-13]\[知乎][熊德意]
- [Why did all of the public reproduction of GPT-3 fail?](https://jingfengyang.github.io/gpt) \[2023-02-12]\[Jingfeng Yang]
- [ChatGPT-所见、所闻、所感](https://zhuanlan.zhihu.com/p/605331104) \[2023-02-11]\[知乎][刘聪NLP] 
- [The Next Generation Of Large Language Models ](https://www.notion.so/Awesome-LLM-40c8aa3f2b444ecc82b79ae8bbd2696b) \[2023-02-07][Forbes]
- [What Are Large Language Models Used For? ](https://www.notion.so/Awesome-LLM-40c8aa3f2b444ecc82b79ae8bbd2696b) \[2023-01-26][NVIDIA]  
- [通向AGI之路：大型语言模型(LLM)技术精要](https://zhuanlan.zhihu.com/p/597586623) \[2023-01-18]\[知乎][张俊林]
- [Major LLMs + Data Availability](https://docs.google.com/spreadsheets/d/1bmpDdLZxvTCleLGVPgzoMTQ0iDP2-7v7QziPrzPdHyM/edit#gid=0) \[2023-01-06\][Shayne Longpre] 
- [How does GPT Obtain its Ability? Tracing Emergent Abilities of Language Models to their Sources](https://yaofu.notion.site/How-does-GPT-Obtain-its-Ability-Tracing-Emergent-Abilities-of-Language-Models-to-their-Sources-b9a57ac0fcf74f30a1ab9e3e36fa1dc1) \[2022-12-11\][Yao Fu]
- [ChatGPT (可能)是怎麼煉成的 - GPT 社會化的過程](https://www.youtube.com/watch?v=e0aKI2GGZNg) \[2022-12-07\][Hung-yi Lee]
- [Large Language Models: A New Moore's Law ](https://huggingface.co/blog/large-language-models) \[2021-10-26\]\[Huggingface\]

## Publicly Available LLM APIs
- [Alpa/OPT-175B](https://opt.alpa.ai)
- [BLOOM](https://huggingface.co/bigscience/bloom)
- [ChatGPT](https://openai.com/blog/chatgpt/)
- [OpenAI](https://openai.com/api/)
- [GLM-130B](https://huggingface.co/spaces/THUDM/GLM-130B)
- [CPM-Bee](https://live.openbmb.org/models/bee)

## Publicly Available LLM Checkpoints
### BigScience/BLOOM

| Size  | Parameters | Link                                                |
| ----- | ---------- | --------------------------------------------------- |
| 560 M | 560 M      | [Huggingface](https://huggingface.co/bigscience/bloom-560m) |
| 1.1 B | 1.1 B      | [Huggingface](https://huggingface.co/bigscience/bloom-1.1b) |
| 1.7 B | 1.7 B      | [Huggingface](https://huggingface.co/bigscience/bloom-1.7b) |
|   3 B |   3 B      | [Huggingface](https://huggingface.co/bigscience/bloom-3b)   |
| 7.1 B | 7.1 B      | [Huggingface](https://huggingface.co/bigscience/bloom-7.1b) |
| 176 B | 176 B      | [Huggingface](https://huggingface.co/bigscience/bloom)      |

### BigScience/T0
| Size  | Parameters | Link                                                |
| ----- | ---------- | --------------------------------------------------- |
|   3 B |   3 B      | [Huggingface](https://huggingface.co/bigscience/T0_3B) |
|  11 B |  11 B      | [Huggingface](https://huggingface.co/bigscience/T0)    |


### Blink/RWKV
  | Size  | Parameters | Link                                                |
  | ----- | ---------- | --------------------------------------------------- |
  | 169 M | 169 M      | [Huggingface](https://huggingface.co/BlinkDL/rwkv-4-pile-169m) |
  | 430 M | 430 M      | [Huggingface](https://huggingface.co/BlinkDL/rwkv-4-pile-430m) |
  | 1.5 B | 1.5 B      | [Huggingface](https://huggingface.co/BlinkDL/rwkv-4-pile-1b5) |
  |   3 B |   3 B      | [Huggingface](https://huggingface.co/BlinkDL/rwkv-4-pile-3b)   |
  |   7 B |   7 B      | [Huggingface](https://huggingface.co/BlinkDL/rwkv-4-pile-7b)   |

### Google/Flan-T5

| Size  | Parameters | Link |     
| ----- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
  | small | 80 M       | [Huggingface](https://huggingface.co/google/flan-t5-small) \| [Original](https://github.com/google-research/t5x/blob/main/docs/models.md#flan-t5-checkpoints) |
  | base  | 250 M      | [Huggingface](https://huggingface.co/google/flan-t5-base) \| [Original](https://github.com/google-research/t5x/blob/main/docs/models.md#flan-t5-checkpoints)  |
  | large | 780 M      | [Huggingface](https://huggingface.co/google/flan-t5-large) \| [Original](https://github.com/google-research/t5x/blob/main/docs/models.md#flan-t5-checkpoints) |
  | xl    | 3 B        | [Huggingface](https://huggingface.co/google/flan-t5-xl) \| [Original](https://github.com/google-research/t5x/blob/main/docs/models.md#flan-t5-checkpoints)    |
  | xxl   | 11 B       | [Huggingface](https://huggingface.co/google/flan-t5-xxl) \| [Original](https://github.com/google-research/t5x/blob/main/docs/models.md#flan-t5-checkpoints)   |



### Meta/OPT
| Size  | Parameters | Link                                                 |
| ----- | ---------- | ---------------------------------------------------- |
| 125 M | 125 M      | [Huggingface](https://huggingface.co/facebook/opt-125m) |
| 350 M | 350 M      | [Huggingface](https://huggingface.co/facebook/opt-350m) |
| 1.3 B | 1.3 B      | [Huggingface](https://huggingface.co/facebook/opt-1.3b) |
| 2.7 B | 2.7 B      | [Huggingface](https://huggingface.co/facebook/opt-2.7b) |
| 6.7 B | 6.7 B      | [Huggingface](https://huggingface.co/facebook/opt-6.7b) |
| 13 B  | 13 B       | [Huggingface](https://huggingface.co/facebook/opt-13b)  |
| 30 B  | 30 B       | [Huggingface](https://huggingface.co/facebook/opt-30b)  |
| 66 B  | 66 B       | [Huggingface](https://huggingface.co/facebook/opt-66b)  |

### Meta/Galactica
| Size     | Parameters | Link                                                       |
| -------- | ---------- | ---------------------------------------------------------- |
| mini     | 125 M      | [Huggingface](https://huggingface.co/facebook/galactica-125m) |
| base     | 1.3 B      | [Huggingface](https://huggingface.co/facebook/galactica-1.3b) |
| standard | 6.7 B      | [Huggingface](https://huggingface.co/facebook/galactica-6.7b) |
| large    | 30 B       | [Huggingface](https://huggingface.co/facebook/galactica-30b)  |
| huge     | 120 B      | [Huggingface](https://huggingface.co/facebook/galactica-120b) |


### EleutherAI/GPT-NeoX
| Size  | Parameters | Link                                                |
| ----- | ---------- | --------------------------------------------------- |
| 20 B | 20 B      | [Huggingface](https://huggingface.co/docs/transformers/model_doc/gpt_neox)\|[Original](https://github.com/EleutherAI/gpt-neox) |


### Tsinghua/GLM
| Size  | Parameters | Link                                                |
| ----- | ---------- | --------------------------------------------------- |
| GLM-Base | 110M    |  [Original](https://github.com/THUDM/GLM)|
| GLM-Large | 335M    |  [Original](https://github.com/THUDM/GLM)|
| GLM-Large-Chinese | 335M    |  [Original](https://github.com/THUDM/GLM)|
| GLM-Doc | 335M    |  [Original](https://github.com/THUDM/GLM)|
| GLM-410M | 410M    |  [Original](https://github.com/THUDM/GLM)|
| GLM-515M | 515M    |  [Original](https://github.com/THUDM/GLM)|
| GLM-RoBERTa | 335M    |  [Original](https://github.com/THUDM/GLM)|
| GLM-2B | 2B    |  [Original](https://github.com/THUDM/GLM)|
| GLM-10B | 10B    |  [Original](https://github.com/THUDM/GLM)|
| GLM-10B-Chinese | 10B    |  [Original](https://github.com/THUDM/GLM)|
| GLM-130B | 130B    |  [Original](https://github.com/THUDM/GLM-130B)|


## Contributing

This is an active repository and your contributions are always welcome! 

I will keep some pull requests open if I'm not sure if they are awesome for LLM, you could vote for them by adding 👍 to them.

------

If you have any question about this opinionated list, do not hesitate to contact me chengxin1998@stu.pku.edu.cn.
