# LLMDataHub: Awesome Datasets for LLM Training
## Introduction
Large language models (LLMs), such as OpenAI's GPT series, Google's Bard, and Baidu's Wenxin Yiyan, are driving profound technological changes. Recently, with the emergence of open-source large model frameworks like LlaMa and ChatGLM, training an LLM is no longer the exclusive domain of resource-rich companies. Training LLMs by small organizations or individuals has become an important interest in the open-source community, with some notable works including Alpaca, Vicuna, and Luotuo. In addition to large model frameworks, large-scale and high-quality training corpora are also essential for training large language models. Currently, relevant open-source corpora in the community are still scattered. Therefore, the goal of this repository is to continuously collect high-quality training corpora for LLMs in the open-source community.



Training a chatbot LLM that can follow human instruction effectively requires access to high-quality datasets that cover a range of conversation domains and styles. In this repository, we provide a curated collection of datasets specifically designed for chatbot training, including links, size, language, usage, and a brief description of each dataset. Our goal is to make it easier for researchers and practitioners to identify and select the most relevant and useful datasets for their chatbot LLM training needs. Whether you're working on improving chatbot dialogue quality, response generation, or language understanding, this repository has something for you.

## Open Access Datasets
#### Tags
- IFT: Instruction Finetune
- DFT: Dialog Finetune
- PT: pretrain
- CoT: Chain-of-Thought Finetune
- RLHF: train reward model in Reinforcement Learning with Human Feedback 

| Dataset name                                                                                                                                                                                                                                                                       | Used by                                                                        | Used for                             | Language                                             | Size                                                                                    | Description                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------------|------------------------------------------------------|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [evol_instruct_70k](https://huggingface.co/datasets/victor123/evol_instruct_70k)                                                                                                                                                                                                   | WizardLM                                                                       | IFT                                  | English                                              |                                                                                         | An instruction finetune dataset derived from Alpaca-52K, using the **evolution** method in [this paper](https://arxiv.org/pdf/2304.12244.pdf)                                        |
| [MOSS SFT data](https://github.com/OpenLMLab/MOSS/tree/main/SFT_data)                                                                                                                                                                                                              | MOSS                                                                           | IFT,<br/>DFT                         | Chinese, English                                     | 1.1M entries                                                                            | A conversational dataset collected and developed by MOSS team. It has usefulness, loyalty and harmlessness labels for every data entries.                                            |
| [ShareGPT52K](https://huggingface.co/datasets/RyokoAI/ShareGPT52K)                                                                                                                                                                                                                 | Koala, Stable LLM                                                              | IFT                                  | Multilingual                                         | 52K                                                                                     | This dataset comprises conversations collected from ShareGPT, with a specific focus on customized creative conversation.                                                             |
| [GPT-4all Dataset](https://huggingface.co/datasets/nomic-ai/gpt4all-j-prompt-generations)                                                                                                                                                                                          | GPT-4all                                                                       | IFT                                  | English, <br/> Might have <br/> a translated version | 400k entries                                                                            | A combination of some subsets of OIG, P3 and Stackoverflow. Covers topics like general QA, customized creative questions.                                                            |
| [COIG](https://huggingface.co/datasets/BAAI/COIG)                                                                                                                                                                                                                                  | /                                                                              | IFT                                  | Chinese,<br/>code                                    | 200K entries                                                                            | A Chinese-based dataset. It contains domains like general purpose QA, Chinese exams, code. Its quality is checked by human annotators.                                               |
| [RedPajama-Data-1T](https://huggingface.co/datasets/togethercomputer/RedPajama-Data-1T)                                                                                                                                                                                            | RedPajama                                                                      | PT                                   | Primarily English                                    | 1.2T tokens <br/> 5TB                                                                   | A fully open pretraining dataset follows the LLaMA's method.                                                                                                                         |
| [OpenAssistant Conversations Dataset (OASST1)](https://huggingface.co/datasets/OpenAssistant/oasst1)                                                                                                                                                                               | OpenAssistant                                                                  | IFT,<br/> DFT                        | Multilingual<br/>(English, Spanish, etc.)            | 66,497 conversation trees                                                               | A large, human-written, human-annotated high quality conversation dataset. It aims at making LLM generates more natural response.                                                    |
| [Alpaca-COT](https://huggingface.co/datasets/QingyiSi/Alpaca-CoT)                                                                                                                                                                                                                  | Phoenix                                                                        | IFT,<br/> DFT,<br/> CoT              | English                                              | /                                                                                       | A mixture a many dataset like classic Alpaca dataset, OIG, Guanaco and some CoT(Chain-of-Thought) datasets like FLAN-CoT. May be handy to use.                                       |
| [CBook-150K](https://github.com/FudanNLPLAB/CBook-150K)                                                                                                                                                                                                                            | /                                                                              | PT, <br/> building dataset           | Chinese                                              | 150K+ books                                                                             | A raw Chinese books dataset. Need some preprocess pipeline.                                                                                                                          |
| [databricks-dolly-15k](https://github.com/databrickslabs/dolly/tree/master/data)                                                                                                                                                                                                   | Dolly2.0                                                                       | IFT                                  | English                                              | 15K+ entries                                                                            | A dataset of **human-written** prompts and responses, featuring tasks such as open-domain question-answering, brainstorming, summarization, and more.                                |
| [AlpacaDataCleaned](https://github.com/gururise/AlpacaDataCleaned)                                                                                                                                                                                                                 | Some Alpaca/ LLaMA-like models                                                 | IFT                                  | English                                              | /                                                                                       | Cleaned version of Alpaca, GPT_LLM and GPTeacher.                                                                                                                                    |
| [GPT-4-LLM Dataset](https://github.com/Instruction-Tuning-with-GPT-4/GPT-4-LLM)                                                                                                                                                                                                    | Some Alpaca-like models                                                        | IFT,<br/> RLHF                       | English,<br/> Chinese                                | 52K entries for English and Chinese respectively <br/> 9K entries unnatural-instruction | NOT the dataset used by GPT-4!! It is generated by GPT-4 and some other LLM for better IFT and RLHF. It includes instruction data as well as comparison data in RLHF style.          |
| [GPTeacher](https://github.com/teknium1/GPTeacher)                                                                                                                                                                                                                                 | /                                                                              | IFT                                  | English                                              | 20k entries                                                                             | A dataset contains targets generated by GPT-4 and includes many of the same seed tasks as the Alpaca dataset, with the addition of some new tasks such as roleplay.                  |
| [HC3](https://github.com/Hello-SimpleAI/chatgpt-comparison-detection)                                                                                                                                                                                                              | Koala                                                                          | RLHF                                 | English,<br/> Chinese                                | 24322 English <br/> 12853 Chinese                                                       | A multi-domain, human-vs-ChatGPT comparison dataset. Can be used for reward model training or ChatGPT detector training.                                                             |
| [Alpaca data](https://github.com/tatsu-lab/stanford_alpaca#data-release) <br/> [Download](https://github.com/tatsu-lab/stanford_alpaca/blob/main/alpaca_data.json)                                                                                                                 | Alpaca, ChatGLM-finetune-LoRA, Koala                                           | DFT,<br/> IFT                        | English                                              | 52K entries<br/>21.4MB                                                                  | A dataset generated by text-davinci-003 to improve language models' ability to follow human instruction.                                                                             |
| [OIG](https://huggingface.co/datasets/laion/OIG) <br/> [OIG-small-chip2](https://huggingface.co/datasets/0-hero/OIG-small-chip2)                                                                                                                                                   | Pythia-Chat-Base-7B, GPT-NeoXT-Chat-Base-20B, Koala                            | DFT,<br/> IFT                        | English,<br/> code                                   | 44M entries                                                                             | A large conversational instruction dataset with medium and high quality subsets *(OIG-small-chip2)* for multi-task learning.                                                         |
| [ChatAlpaca data](https://github.com/cascip/ChatAlpaca)                                                                                                                                                                                                                            | /                                                                              | DFT,<br/> IFT                        | English,<br/> Chinese version coming soon            | 10k entries<br/>39.5MB                                                                  | A dataset aims to help researchers develop models for instruction-following in multi-turn conversations.                                                                             |
| [InstructionWild](https://github.com/XueFuzhao/InstructionWild)                                                                                                                                                                                                                    | ColossalChat                                                                   | IFT                                  | English, Chinese                                     | 10K enreues                                                                             | A Alpaca-style dataset, but with seed tasks comes from chatgpt screenshot.                                                                                                           |
| [Firefly(流萤)](https://huggingface.co/datasets/YeungNLP/firefly-train-1.1M)                                                                                                                                                                                                         | Firefly(流萤)                                                                    | IFT                                  | Chinese                                              | 1.1M entries<br/>1.17GB                                                                 | A Chinese instruction-tuning dataset with 1.1 million human-written examples across 23 tasks, but no conversation.                                                                   |
| [BELLE](https://github.com/LianjiaTech/BELLE) <br/> [0.5M version](https://huggingface.co/datasets/BelleGroup/train_0.5M_CN) <br/> [1M version](https://huggingface.co/datasets/BelleGroup/train_1M_CN) <br/> [2M version](https://huggingface.co/datasets/BelleGroup/train_2M_CN) | BELLE series, Chunhua (春华)                                                     | IFT                                  | Chinese                                              | 2.67B in total                                                                          | A Chinese instruction dataset similar to *Alpaca data* constructed by generating answers from seed tasks, but no conversation.                                                       |
| [GuanacoDataset](https://huggingface.co/datasets/JosephusCheung/GuanacoDataset#guanacodataset)                                                                                                                                                                                     | Guanaco                                                                        | DFT,<br/> IFT                        | English,<br/> Chinese,<br/> Japanese                 | 534,530 entries                                                                         | A multilingual instruction dataset for enhancing language models' capabilities in various linguistic tasks, such as natural language understanding and explicit content recognition. |
| [xP3 (and some variant)](https://huggingface.co/datasets/bigscience/xP3)                                                                                                                                                                                                           | BLOOMZ, mT0                                                                    | IFT                                  | Multilingual,<br/> code                              | 79M entries<br/>88GB                                                                    | An instruction dataset for improving language models' generalization ability, similar to *Natural Instruct*.                                                                         |
| [OpenAI WebGPT](https://huggingface.co/datasets/openai/webgpt_comparisons)                                                                                                                                                                                                         | WebGPT's reward model, Koala                                                   | RLHF                                 | English                                              | 19,578 pairs                                                                            | Data set used in WebGPT paper. Used for training reward model in RLHF.                                                                                                               |
| [OpenAI Summarization Comparison](https://huggingface.co/datasets/openai/summarize_from_feedback)                                                                                                                                                                                  | Koala                                                                          | RLHF                                 | English                                              | ~93K entries<br/>420MB                                                                  | A dataset of human feedback which helps training a reward model. The reward model was then used to train a summarization model to align with human preferences.                      |
| [Natural Instruction](https://instructions.apps.allenai.org/) <br/> [GitHub&Download](https://github.com/allenai/natural-instructions)                                                                                                                                             | tk-instruct series                                                             | IFT, <br/> evaluation                | Multilingual                                         | /                                                                                       | A benchmark with over 1,600 tasks with instruction and definition for evaluating and improving language models' multi-task generalization under natural language instruction.        |
| [hh-rlhf](https://github.com/anthropics/hh-rlhf) <br/> [on Huggingface](https://huggingface.co/datasets/Anthropic/hh-rlhf)                                                                                                                                                         | Koala                                                                          | RLHF                                 | English                                              | 161k pairs<br/>79.3MB                                                                   | A pairwise dataset for training reward models in reinforcement learning for improving language models' harmlessness and helpfulness.                                                 |
| [Common Crawl](https://commoncrawl.org/)                                                                                                                                                                                                                                           | LLaMA (After some process)                                                     | building datasets, <br/> PT          | /                                                    | /                                                                                       | The most well-known raw dataset, rarely be used directly. One possible preprocess pipeline is [CCNet](https://github.com/facebookresearch/cc_net)                                    |
| [The Pile (V1)](https://pile.eleuther.ai/)                                                                                                                                                                                                                                         | GLM (partly), LLaMA (partly), GPT-J, GPT-NeoX-20B, Cerebras-GPT 6.7B, OPT-175b | PT                                   | Multilingual,<br/> code                              | 825GB                                                                                   | A diverse open-source language modeling dataset consisting of 22 smaller, high-quality datasets that includes many domains and tasks.                                                |
| C4 <br/> [Huggingface dataset](https://huggingface.co/datasets/c4) <br/> [TensorFlow dataset](https://www.tensorflow.org/datasets/catalog/c4)                                                                                                                                      | Google T5 Series, LLaMA                                                        | PT                                   | English                                              | 305GB                                                                                   | A colossal, cleaned version of Common Crawl's web crawl corpus. Frequently be used.                                                                                                  |
| [ROOTS](https://huggingface.co/bigscience-data)                                                                                                                                                                                                                                    | BLOOM                                                                          | PT                                   | Multilingual,<br/> code                              | 1.6TB                                                                                   | A diverse open-source dataset consisting of sub-datasets like Wikipedia and StackExchange for language modeling.                                                                     |
| [Pushshift reddit](https://files.pushshift.io/reddit/) <br/> [paper](https://arxiv.org/pdf/2001.08435.pdf)                                                                                                                                                                         | OPT-175b                                                                       | PT                                   | /                                                    | /                                                                                       | Raw reddit data, one possible processing pipeline in [this paper](https://aclanthology.org/2021.eacl-main.24.pdf)                                                                    |
| [Gutenberg project](https://www.gutenberg.org/policy/robot_access.html)                                                                                                                                                                                                            | LLaMA                                                                          | PT                                   | Multilingual                                         | /                                                                                       | A book dataset, mostly novels. Not be preprocessed.                                                                                                                                  |
| [CLUECorpus](https://github.com/CLUEbenchmark/CLUE)                                                                                                                                                                                                                                | /                                                                              | PT, <br/> finetune, <br/> evaluation | Chinese                                              | 100GB                                                                                   | A Chinese pretraining Corpus sourced from *Common Crawl*.                                                                                                                            |

### Potential Overlaps

We consider row items as subject.

|                   | OIG     | hh-rlhf  | xP3     | natural instruct | AlpacaDataCleaned | GPT-4-LLM | Alpaca-CoT |
|-------------------|---------|----------|---------|------------------|-------------------|-----------|------------|
| OIG               | /       | contains | overlap | overlap          | overlap           |           | overlap    |
| hh-rlhf           | part of | /        |         |                  |                   |           | overlap    |
| xP3               | overlap |          | /       | overlap          |                   |           | overlap    |
| natural instruct  | overlap |          | overlap | /                |                   |           | overlap    |
| AlpacaDataCleaned | overlap |          |         |                  | /                 | overlap   | overlap    |
| GPT-4-LLM         |         |          |         |                  | overlap           | /         | overlap    |
| Alpaca-CoT        | overlap | overlap  | overlap | overlap          | overlap           | overlap   | /          |

## Domain-specific Datasets

| Dataset name                                                             | Used by | Used for                   | Language | Size         | Description                                           |
|--------------------------------------------------------------------------|---------|----------------------------|----------|--------------|-------------------------------------------------------|
| [finance-alpaca](https://huggingface.co/datasets/gbharti/finance-alpaca) | /       | IFT                        | English  | 1.3K entries | An Alpaca-style dataset but focus on financial topics |

## Private Datasets
| Dataset name          | Used by            | Used for            | Language                              | Size        | Description                                                                                     |
|-----------------------|--------------------|---------------------|---------------------------------------|-------------|-------------------------------------------------------------------------------------------------|
| ShareGPT-70K          | Vicuna             | Instruction fintune | /                                     | 70K entries | Data shared by user on [ShareGPT](https://sharegpt.com/)                                        |
| WebText(Reddit links) | GPT-2              | PT                  | English                               | /           | Data crawled from Reddit and filtered for GPT-2 pretraining.                                    |
| MassiveText           | Gopher, Chinchilla | PT                  | 99% English, 1% other(including code) |             |                                                                                                 |
| WuDao(悟道) Corpora     | GLM                | PT                  | Chinese                               | 200GB       | A large scale Chinese corpus, Possible component originally open-sourced but not available now. |
