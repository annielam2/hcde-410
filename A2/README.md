HCDE 410 A2: Exploring Sources of Bias in the Wikipedia Talk Corpus
This repository holds my Assignment 2 for HCDE 410 (Human Data Interaction), Autumn 2026. The notebook hcde410-a2.ipynb examines the Wikipedia Talk Corpus, which was used to train Google Jigsaw's Perspective API toxic-speech classifier. It looks for limitations in the data and reasons about how they could bias a general-purpose toxic-speech detector.

What the notebook does
Data preparation (Part 1). Loads and checks the three crowdworker demographic files. It finds that two of them are identical, and that worker IDs are reused across datasets for different people. It then combines the files into one de-duplicated table with truly unique IDs.
Demographic analysis (Part 2, Q1–Q8). Describes the workers by gender, first language, age and education. It measures missing data, shows how leaving the duplicate file in skews the results, and compares the workers to internet users overall.
Bias reasoning (Part 3, Q9–Q12). Joins the 1.6 million toxicity labels to worker demographics to see whose judgments shaped the labels.
Key findings
attack_worker_demographics.tsv and aggression_worker_demographics.tsv are identical, which the documentation doesn't mention.
1,858 worker_id values appear in both the toxicity and the attack/aggression files but belong to different people.
The labellers are 63.6% male, 81.5% non-native English speakers, and 86% under 45.
Only 83.5% of the workers who labelled toxicity comments have demographic data, so 15.7% of labels come from unknown workers.
Among labels with known demographics, about 66% came from men and about 83% from non-native English speakers.
A summary table at the end of the notebook lists each limitation, the evidence for it, and a hypothesis about how it could skew the model.

Data
The data comes from the Wikipedia Detox project, released by Wikimedia and Jigsaw:

Wikipedia Talk Labels: Toxicity
Wikipedia Talk Labels: Aggression
Wikipedia Talk Labels: Personal Attacks
Documentation and schema
The datasets are released under CC0 (public domain).

Wulczyn, E., Thain, N., & Dixon, L. (2017). Ex Machina: Personal Attacks Seen at Scale. Proceedings of the 26th International Conference on World Wide Web, 1391–1399. https://doi.org/10.1145/3038912.3052591

How to run it
Put these files in a folder called wikipedia_datasets/, next to the notebook:
toxicity_worker_demographics.tsv
attack_worker_demographics.tsv
aggression_worker_demographics.tsv
toxicity_annotations.tsv (from the Toxicity download)
Install the Python libraries: pip install pandas matplotlib
Open hcde410-a2.ipynb in Jupyter and choose Kernel → Restart & Run All.

License
The code and writing in this repository are under the MIT License; see LICENSE.md. The data files are CC0, as described above.

