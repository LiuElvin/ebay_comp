# eBay 2023 University Machine Learning Competition

- The annual competition asks students to dream up innovative solutions to real-world ecommerce problems in the space of Machine Learning on an e-commerce dataset.

# General Information

- Build a model that can accurately extract and label the named entities in the dataset of item titles on eBay. Named Entities are the semantic strings/words/phrases that refer to people, brands, organizations, locations, styles, materials, patterns, product names, units of measure, clothing sizes, etc.

- Named Entity Recognition (NER) is the machine learning process of automatic labeling and extracting important named entities in a text that carry a particular meaning. In e-commerce, NER is used to process listing or product titles and descriptions, queries, and reviews, or wherever extraction of important data from raw text is desired.

- The data is from listings on eBay’s German site.

- Performance of the model for each aspect name is graded using weighted precision, recall and f1-score. The aspects will be weighted by their count in the quiz or test dataset. The final precision, recall and the final combined f1-score are calculated by adding the individual weighted aspect name f1-scores.

# The Model

- Our team "jookisthebest" placed 12th out of 887 teams.

- The model trains a token classification model using Hugging Face's Transformers library and logs the training process with weights & biases. Here's a summary of what the code does:

1. The datasets library is used to load and handle the dataset.

2. Hugging Face's transformers library is utilized to load a pre-trained token classification model.

3. The AutoTokenizer class from transformers is employed to tokenize the dataset.

4. The model is trained using PyTorch.
  - PyTorch's torch library is used for neural network operations.
  - The training loop is implemented with custom optimization strategies using AdamW optimizer and learning rate schedulers.
  - Training progress is logged using weights & biases (wandb).

5. Model performance metrics like precision, recall, F1-score, and accuracy are computed during training and evaluation.
  - Evaluation metrics are computed using the seqeval library.

6. Training and evaluation data are loaded and processed using PyTorch's DataLoader.

7. Experiment logging is performed using Weights & Biases (wandb).

- Incorporated Facebook's RoBERTa model to tokenize German.

- Includes some manual pre-processing so symbols can be understood.

- The original scripts are stored elsewhere for accessability and privacy reasons (HuggingFace and Wandb logins).

# Miscellaneous Information

1. Named entity recognition (NER) is a fundamental task in Natural Language Processing (NLP) and one of the first stages in many language understanding tasks. It has drawn research attention for a few decades, and its importance has been well recognized in both academia and industry.

3. The extracted entities are also called aspects, and an aspect consists of the aspect name (“Brand name” for the first aspect in the last example above) and the aspect value (“NYX” for the same aspect in the same example above). The objective of this challenge then is to extract and label the aspects in the dataset of item titles listed on eBay. Not all titles have all aspects, and figuring out which aspect is present for a given title is part of the challenge.

# Data

The data set consists of 10 million randomly selected unlabeled item titles from eBay Germany, all of which are from “Athletic Shoes” categories. Among these item titles there will be 10,000 labeled item titles (“labeled” means the aspects have been extracted). There will also be an annexure document provided that describes the dataset. Finally, we will provide the set of aspect names that should be extracted from each item title (as stated before, not all titles have all aspects). Each item title will have a unique identifier (a record number).

The 10,000 labeled item titles will be split into three groups:

Training set (5,000 records)
Quiz set (2,500 records)
Test set (2,500 records)
The 10 million unlabeled title set and the training set is intended for participants to build their models/prediction system. The actual aspects will be provided for each item title in the training set, along with the item title record number to link the aspects to the title.

---

# Contributions

- My teammate, James Ngai, did most of the coding portions for PyTorch and Wandb.

- We were both novices at ML theory, so most of my work was just experimentation with whatever features HuggingFace could provide for Neural Networks.

- I ended up testing the models and modifying hyperparameters based off graphs provided in Wandb.

- Also set up our cloud services for gpu training.

# Learning Outcomes

- Essentially everything was new here. I initially wasn't that familiar with ML at all, from general concepts to coding in the Python packages given.

- Increased familiarity with Neural Networks and their hyperparameters.

- Increased familiarity with HuggingFace, PyTorch, and Wandb.
  - Particularly HuggingFace, as the API was something entirely foreign to me beforehand.

- Use of Google Cloud and AWS for model training.
