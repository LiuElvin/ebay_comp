# eBay 2023 University Machine Learning Competition

- The annual competition asks students to dream up innovative solutions to real-world ecommerce problems in the space of Machine Learning on an e-commerce dataset.

# The Challenge

Named entity recognition (NER) is a fundamental task in Natural Language Processing (NLP) and one of the first stages in many language understanding tasks. It has drawn research attention for a few decades, and its importance has been well recognized in both academia and industry.

While NER is applied in many different settings, for this challenge, we will only be using eBay listing titles for NER. A few examples of NER labeling of listing titles are shown below (these examples are in English to illustrate the concept, the challenge data will have German language listing titles).

The extracted entities are also called aspects, and an aspect consists of the aspect name (“Brand name” for the first aspect in the last example above) and the aspect value (“NYX” for the same aspect in the same example above). The objective of this challenge then is to extract and label the aspects in the dataset of item titles listed on eBay. Not all titles have all aspects, and figuring out which aspect is present for a given title is part of the challenge.

# Data

The data set consists of 10 million randomly selected unlabeled item titles from eBay Germany, all of which are from “Athletic Shoes” categories. Among these item titles there will be 10,000 labeled item titles (“labeled” means the aspects have been extracted). There will also be an annexure document provided that describes the dataset. Finally, we will provide the set of aspect names that should be extracted from each item title (as stated before, not all titles have all aspects). Each item title will have a unique identifier (a record number).

The 10,000 labeled item titles will be split into three groups:

Training set (5,000 records)
Quiz set (2,500 records)
Test set (2,500 records)
The 10 million unlabeled title set and the training set is intended for participants to build their models/prediction system. The actual aspects will be provided for each item title in the training set, along with the item title record number to link the aspects to the title.

---

# Contributions

- My teammates James Ngai did most of the coding.

- I ended up testing the models and hyperparameters, looking at graphs of loss.

# Learning Outcomes

- Placed 12th out of 887 teams and 1439 students
