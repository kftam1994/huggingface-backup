---
dataset_info:
  features:
  - name: question
    dtype: string
  - name: answer
    sequence: string
  - name: dataset
    dtype: string
  - name: split
    dtype: string
  - name: solution
    dtype: string
  - name: question_type
    dtype: string
  - name: text
    dtype: string
  - name: meta
    struct:
    - name: source
      dtype: string
  - name: A
    dtype: string
  - name: B
    dtype: string
  - name: C
    dtype: string
  - name: D
    dtype: string
  - name: E
    dtype: string
  - name: explanation
    dtype: string
  - name: id
    dtype: int32
  - name: subject
    dtype: string
  - name: exam_type
    dtype: string
  - name: dataset_subset
    dtype: string
  - name: cot
    dtype: 'null'
  splits:
  - name: train
    num_bytes: 53239869
    num_examples: 13959
  download_size: 24087760
  dataset_size: 53239869
configs:
- config_name: default
  data_files:
  - split: train
    path: data/train-*
---
### Dataset Information
Target to select Q&A dataset related to financial domain and have hard enough difficulty for generating thinking trajectory traces from reasoning models (such as Deepseek R1)

| Dataset                                   | Total Examples | Contaminated Questions | Contamination Rate | Clean Examples |
|-------------------------------------------|----------------|------------------------|--------------------|----------------|
| FinAI_flare <br>├── TheFinAI/flare-cfa (1032) <br>└── ChanceFocus/flare-finqa (8281) | 9313 | 0 | 0.00% | 9313 |
| Duxiaoman-DI/FinCorpus (fin_exam.jsonl.gz and filter for questions >500 CHN chars)| 5334           | 0                      | 0.00%              | 5334           |
| [IDEAFinBench](https://github.com/IDEA-FinAI/IDEAFinBench/tree/main/datasets) (cfa_l2)                     | 714            | 40                     | 5.60%              | 674            |
| Salesforce/FinEval                        | 886            | 3                      | 0.34%              | 883            |
| KirkHan/FRM_QA100                         | 100            | 4                      | 4.00%              | 96             |

**Notes:**

- Decontamincation based on [s1's procedure](https://github.com/simplescaling/s1/blob/main/data/decontaminate_util.py)
- For **IDEAFinBench**, examples of matching n-grams include:
  - the excess of the purchase price over the
  - excess of the purchase price over the fair
  - of the purchase price over the fair value
  - the purchase price over the fair value of
  - change in the us consumer price index for
- For **FinEval**, examples of matching n-grams include:
  - of the following is least likely to be
  - the following is least likely to be a
  - exhibit 1, which of the following statements is
  - more than offset the negative effects of higher
- For **FRM_QA100**, examples of matching n-grams include:
  - the standard error of the sample mean is
  - standard error of the sample mean is closest
  - a decline in the value of the euro
  - which of the following is closest to the

