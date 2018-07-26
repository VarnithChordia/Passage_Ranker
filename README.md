# Passage_Ranker

This is Module for Passage ranking using DRMM model. This was trained and tested on WikiQA dataset. The metrics used in this model are ndcg@5 and MAP(Mean Average precision). 

To run this model on different dataset, go to -> Data -> WikiQA -> transfer_to_mz_format.py, in this file change the name of the  " basedir + 'WikiQA-test-filtered.txt' " -> "basedir + <Insert_your file name>'
Remeber to follow the format of the files with labels and question answers.

Format of NETGEAR with forum question and answers is available by the name of "test_sample.txt"


To train the model run the following command 

```
python passage_rnkr/main.py --phase train --model_file examples/wikiqa/config/drmm_wikiqa.config
```

To predict the model on your test 

```
python passage_rnkr/main.py --phase predict --model_file examples/wikiqa/config/drmm_wikiqa.config
```
