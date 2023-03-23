# Intent classification in a banking domain 
HSE Neural Networks in NLP Course

[Link](https://www.kaggle.com/soimmarylanabanana/nnlp-project-EDA) to EDA.
[Link](https://www.kaggle.com/soimmarylanabanana/nnlp-project-catboost2) to CatBoost training on Kaggle.

## Task
Multiclass classification.

## Dataset
Previous intent detection datasets such as Web Apps, Ask Ubuntu, the Chatbot Corpus or SNIPS are limited to small number of classes (<10), which oversimplifies the intent detection task and does not emulate the true environment of commercial systems. Although there exist large scale multi-domain datasets (HWU64 and CLINC150), the examples per each domain may not sufficiently capture the full complexity of each domain as encountered "in the wild". The [Banking77](https://huggingface.co/datasets/banking77) dataset tries to fill the gap and provides a very fine-grained set of intents in a single-domain i.e. banking. It consists of 77 classes.

## Dataset statistics        

Number of examples: 10 003 in train, 3 080 in test
Average character length: 59.5 in train, 54.2 in test
Number of intents: 77

## Solution

**CatBoost (~30 text features)**

- Accuracy: 0.8282467532467532
- Weighted F1: 0.8288142169280499
- Micro F1: 0.8282467532467532
- Macro F1: 0.8276792895654566

**CatBoost (~30 text features) + Sentence Transformer (nq-distilbert-base-v1)👍🏻**

- Accuracy: 0.8844155844155844
- Weighted F1: 0.8846075063246825
- Micro F1: 0.8844155844155844
- Macro F1: 0.884223662506486

**CatBoost (~30 text features) + Sentence Transformer (all-MiniLM-L6-v2)👍👍🏻**

- Accuracy: 0.9149350649350649
- Weighted F1: 0.915300248802941
- Micro F1: 0.9149350649350649
- Macro F1: 0.9145698810671887

## Team
- Maria Bocharova
- Kseniya Danilova
