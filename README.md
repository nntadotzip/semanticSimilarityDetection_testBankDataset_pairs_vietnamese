# semanticSimilarityDetection_testBankDataset_pairs_vietnamese
Dataset for Data Augmentation Methods for Semantic Similarity Detection in Vietnamese Questionnaire 

The dataset is created to serve the augmentation for question pairs.

## Motivation
Finetuning a pretrained model to detect semantic similarity in educational examination.

## Data Details:
- 01 csv file with 06 attributes:
    + sentence1, sentence2: a pair of questions.
    + correct_option_sen1, correct_option_sen2: correct option of the corresponding question.
    + cosine_usingSBert: cosine simiarity of the corresponding pair (sentence1 and sentence2) using SBert model.
    + label: manual labeling.
- length: 10,205 pairs.

## Crawling Details:
- Source: https://vietjack.com
- Subject: Geography (from 0 to 8000th row), Literature (from 8001th row)
- Language: Vietnamese

## Pairing Details:
- To deliver a dataset contains pairs with high possibility of being similar, the combination is not applied to all sentences, instead, only quesionnaires within a lesson (categorized by Vietjack) are paired among others.

## Labeling Details:
- Important note: The pairs with label=1 is not exactly 100% the same in meaning, it is because the target of this study is to deliver a model with the ability of filtering out "similar questions" or "question infers to others" in a actual exam.
- The persons who are in charge of labeling questions have the domain knowledge that can distinguish questions satisfied the above requirements.
