# Analysis of BERT for WSD in Russian
This repository contains code and datasets for running the main experiments covered in "What works best for Russian WSD: models and strategies"

# MERGED DATA:
MERGED DATA set is a WSD benchmark targetting 2 to 5 senses of 21 ambiguous nouns. It was specifically compiled from benchmark for two datasets (RUSSE and Corpus-1000), to provide an ideal setting for evaluating WSD models (e.g. no senses in test sets missing from training), both quantitavely and qualitatively.
An individual dataset for each word contains files with a standard 70/30 train-test split, and classes map with uniformed senses from both corpora according to RuWordNet:

classes_map.txt
test.data.txt
test.gold.txt
train.data.txt
train.gold.txt

The formate of train.data.txt: [idx of target word] [sample sentence containing the target word]
The formate of train.gold.txt: [idx of gold sense from calsses_map]

all methods are written in jypiter notebook and adopted for the use in Google colab

# Feature Extraction

You may use the [BERT_for_WSD_1NN] (https://github.com/alanev52/WSD/BERT_for_WSD_1NN.ipynb) to create sense embeddings from a particular set from our MERGED DATA and evaluate the predictions.
# Fine-Tuning:

You may use the [BERT_for_fine-tuning] https://github.com/alanev52/WSD/BERT_for_fine-tuning.ipynb to fine-tune BERT models within a set from our MERGED DATA and evaluate the predictions.
To compute F1 scores we supply a separate [F1-score for FT](https://github.com/alanev52/WSD/blob/main/F1_score_for_FT.ipynb))

# Results:
F1-scores can be merged in one CSV file by []()
You can fine an excel format document with the main [results] ()
