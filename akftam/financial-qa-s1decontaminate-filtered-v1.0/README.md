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
    dtype: int64
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
    num_bytes: 34275719
    num_examples: 8605
  download_size: 15397629
  dataset_size: 34275719
configs:
- config_name: default
  data_files:
  - split: train
    path: data/train-*
---
### Dataset Information

- **Total Questions Across All Datasets**: 13,959 (from [akftam/financial-qa-s1decontaminate-v1.0](https://huggingface.co/datasets/akftam/financial-qa-s1decontaminate-v1.0). Choice questions: 5751, Numeric questions: 8208).
- **Correctly Answered**: 5,354
- **Filtered Questions**: 8,605 (This dataset akftam/financial-qa-s1decontaminate-filtered-v1.0)

### Questions Performance (Accuracy)

| **Dataset**            | **Total Questions** | **Mistral-Small-3.1-24B-Instruct-2503** | **Qwen2.5-32B-Instruct** |
|-------------------------|---------------------|-----------------------------------------|--------------------------|
| IDEAFinBench           | 674                 | 63.95%                                  | 52.23%                   |
| TheFinAI/flare-cfa     | 1032                | 78.00%                                  | 79.65%                   |
| Duxiaoman-DI/FinCorpus | 3069                | 38.78%                                  | 48.09%                   |
| Salesforce/FinEval     | 883                 | 16.42%                                  | 5.32%                    |
| KirkHan/FRM_QA100      | 93                  | 66.67%                                  | 73.12%                   |
| ChanceFocus/flare-finqa| 8208                | 19.41%                                  | 18.94%                   |
