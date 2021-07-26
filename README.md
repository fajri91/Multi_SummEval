# Multi_SummEval

## About

While automatic summarization evaluation methods developed for English are routinely applied to other languages, this is the first attempt to 
systematically quantify their panlinguistic efficacy. We take a summarization corpus for eight different languages (EN, ID, FR, TR, ZH, RU, DE, ES), and manually 
annotate generated summaries for focus (precision) and coverage (recall).

## Paper
Fajri Koto, Jey Han Lau, and Timothy Baldwin. [_Evaluating the Efficacy of Summarization Evaluation across Languages_](https://aclanthology.org/2021.findings-acl.71.pdf). 
In Findings of the Association for Computational Linguistics: ACL-IJCNLP 2021.

## Focus and Coverage

We examine content-based summarization evaluation from the aspects of precision and recall, in the form of focus and coverage to 
compare system-generated summaries to groundtruth summaries.

<img src="https://github.com/fajri91/eval_picts/blob/master/foc_cov.png" width="400">

## MTurk 

* We use the customized [direct assessment](https://github.com/ygraham/direct-assessment) method for annotation.
* We use Amazon Mechanical Turk for annotation. You can find the MTurk user interface at `mturk/html`.
* Jupyter notebooks number 0-3 are used to pre- and post-process the MTurk annotation
* In this repository, we only provide annotation process for ID, FR, TR, ZH, RU, DE, ES. Annotation process for EN will be released seperately
because the data is from the [FFCI paper](https://arxiv.org/pdf/2011.13662.pdf).

## Data (Annotation Result)

* You can find **all** annotation result in folder `resulting_data`.
* The provided scores are the normalized z-score.

## Traditional metrics (ROUGE, METEOR, BLEU)

* You can use jupyter notebooks number 5-6 to compute traditional metrics and its Pearson and Spearman correlations.
* Please note that for ZH and RU you need to convert all character/word to its latin form by using jupyter notebook `5. transform_RU_and_ZH.ipynb`.

## BERTScore and MoverScore

* We already provide all of the output of BERTScore and MoverScore in folder `bert_score` and `mover_score`, respectively
* You can use jupyter notebook number 7-8 to compute its Pearson and Spearman correlations.
