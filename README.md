# Google-Quest-Multilabel-Classification

Computers are really good at answering questions with single, verifiable answers. But, humans are often still better at answering questions about opinions, recommendations, or personal experiences.

Humans are better at addressing subjective questions that require a deeper, multidimensional understanding of context - something computers aren't trained to do well…yet.. Questions can take many forms - some have multi-sentence elaborations, others may be simple curiosity or a fully developed problem. They can have multiple intents, or seek advice and opinions. Some may be helpful and others interesting. Some are simple right or wrong.

![image](https://github.com/sdarjunwadkar/Google-Quest-Multilabel-Classification/assets/59260370/eca40eb8-b4da-429e-9239-a9356d53ca11)


Unfortunately, it’s hard to build better subjective question-answering algorithms because of a lack of data and predictive models. That’s why the CrowdSource team at Google Research, a group dedicated to advancing NLP and other types of ML science via crowdsourcing, has collected data on a number of these quality scoring aspects.

The data includes questions and answers from various StackExchange properties. The task is to predict target values of 30 labels for each question-answer pair.

The list of 30 target labels are the same as the column names in the sample_submission.csv file. Target labels with the prefix question_ relate to the question_title and/or question_body features in the data. Target labels with the prefix answer_ relate to the answer feature.

Each row contains a single question and a single answer to that question, along with additional features. The training data contains rows with some duplicated questions (but with different answers). The test data does not contain any duplicated questions.

This is not a binary prediction challenge. Target labels are aggregated from multiple raters, and can have continuous values in the range [0,1]. Therefore, predictions must also be in that range.

There are two folders:

1) codes
2) data

The codes folder contains three python notebooks (Google Colab):

1) Abbrevations Analysis: To check if there are any slangs
2) Multi-Label Classification BERT-Linear: This is a Sequential Model, 2 Dense Layer on stacked input (Baseline Model)
3) Multi-Label Classification BERT-BiLSTM: This is a BiLSTM Model, Classifier with 2 Hidden Dense Layer

The data folder contains two files:
1) train.csv
2) test.csv
