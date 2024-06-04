# Analysis of BERT for WSD in Russian
This repository contains code and datasets for running the main experiments covered in RD project "What works best for Russian WSD: models and strategies".  
A significant portion of the code was influenced by the research and methodologies presented in ["Analysis and Evaluation of Language Models for Word Sense Disambiguation" (Computational Linguistics, 2021).](https://watermark.silverchair.com/coli_a_00405.pdf?token=AQECAHi208BE49Ooan9kkhW_Ercy7Dm3ZL_9Cf3qfKAc485ysgAAAzswggM3BgkqhkiG9w0BBwagggMoMIIDJAIBADCCAx0GCSqGSIb3DQEHATAeBglghkgBZQMEAS4wEQQM8sx8B70p11Fhmhx8AgEQgIIC7jpCSKZW7RzHJO9NxSKnVcFMzxC1aiY1wYQrkfp1iyKm8nGxkS4IJ_HsXNd9vLSTRxJEw8L13XXN3ozoJhI3o5rv04Nue4QUzCMTxFRAgL-joP4XKMYi5b9k7Y-BLq72DNo9myT4HJZr4X4LbJBjb5iifRfDUJN8w9rQZsJb9OH_6Jv_srxd42dA_pP8s58oLw8IhLiiyerflrzTOF6ZCgAMe40KqjYtt-gohbBxUgU-84C3fr1a4PTyvY1pk_vvNkZ16aZtPiKem5pn_bPUXlA1J_l0Q9SNIf0Sn2GyW1RRLcJorZ3NQEIHvwcwH91Nv7iJ0OgoThFXl9T0t6gnBixOJssn4ingyH2BkbEa0-fRbp2SRNq0xkRzwvOGlPU1ee0yQlLhF8aiVe2XfXmdvvvLbhZ6j8hNVwsTOusuyk9ixGWp3AGcaLc72qsrcsg_3IKQok357jeucSTmCjei3Tv4VPrellecHnIMBEFgmcNh-mDREJabmzkF8_c5TLWmySnSbRNVEDhafw_C_vZnDNa7ehxKE-iqitRNHze3mbRShTYoZS4Yps2sn5oGsbt7gAL9kzkMSaU8lk2T5Yb-MadVkvQKNGb5Ypgi7h5gIQC-KbD_97c_tYFsjUk5axT00VujPPFaNYYF7rpsFjSjQkvhKr5z6-CpqbfqaISECl5Hm9zIIEqVzQ340fhLyITZmp9AjcQsODVZMt9yWqf0xSoPtmF8N-ZRjzdyT6eTW7Oc9LhTzj6YHig4N5FnGfOXgbp66ZIedEyBvsCFvkY0jy_qQJmTVo_BsmH5nAHcaLVz5ko_H9w_JIrmgnKA4cekl_8T3jUo7fauNn5k4Vxiy4S1cicwb-elg5u61s8b4vPodgn6sjw4jDbnO8lkoWx3BqcRonCB19ZxTwktSSEUN3Jfie8n21ZcZ4IHu67bkoloyLWUD9Z6LT_JIArBYCtPqIhcRNg_hE2e_LycuS9DlQEVrbiA8okjArrjh2uuOg). The original code can be found [here](https://github.com/danlou/bert-disambiguation)

## MERGED DATA:
MERGED DATA set is a WSD benchmark targetting 2 to 5 senses of 21 ambiguous nouns. It was specifically compiled from benchmark for two datasets (RUSSE and Corpus-1000), to provide an ideal setting for evaluating WSD models (e.g. no senses in test sets missing from training), both quantitavely and qualitatively.
An individual dataset for each word contains files with a standard 70/30 train-test split, and classes map with uniformed senses from both corpora according to RuWordNet:

- classes_map.txt
- test.data.txt
- test.gold.txt
- train.data.txt
- train.gold.txt

The formate of train.data.txt: [idx of target word] [sample sentence containing the target word]

The formate of train.gold.txt: [idx of gold sense from calsses_map]
___________________________________________________________________________________________________________

_All methods are written in jupyter notebook and adopted for the use in Google colab._
## Feature Extraction:

You may use the [BERT_for_WSD_1NN](https://github.com/alanev52/WSD/BERT_for_WSD_1NN.ipynb) to create sense embeddings from a particular set from our MERGED DATA and evaluate the predictions.
## Fine-Tuning:

You may use the [BERT_for_fine-tuning](https://github.com/alanev52/WSD/BERT_for_fine-tuning.ipynb) to fine-tune BERT models within a set from our MERGED DATA and evaluate the predictions.
To compute F1 scores we supply a separate [F1-score for FT](https://github.com/alanev52/WSD/blob/main/F1_score_for_FT.ipynb))

## Results:
F1-scores can be merged in one CSV file by [Merge_CSV_F1_scores](https://github.com/alanev52/WSD/blob/main/Merge_CSV_F1_scores_file.ipynb)
You can fine an excel format document with the main [results](https://github.com/alanev52/WSD/blob/main/results.xlsx)
