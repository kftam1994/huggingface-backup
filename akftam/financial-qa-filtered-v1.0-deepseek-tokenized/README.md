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
  - name: thinking_trajectories
    dtype: string
  - name: attempt
    dtype: string
  - name: extracted_answer
    sequence: string
  - name: is_correct
    dtype: bool
  - name: question_hash
    dtype: string
  splits:
  - name: train
    num_bytes: 155005790
    num_examples: 6447
  download_size: 65415340
  dataset_size: 155005790
configs:
- config_name: default
  data_files:
  - split: train
    path: data/train-*
---
### Dataset Information

- Generate Deepseek R1 thinking traces for dataset akftam/financial-qa-s1decontaminate-filtered-v1.0
- Verified attempt by rules for numeric answer and gemini-2.0-flash for choice answer
  - Correct: 6447/8605 (74.92%)
  - Incorrect: 2158/8605 (25.08%)
- This dataset only keeps those correct examples
- A "text" column is added by using the script similar to [s1 tokenization](https://github.com/simplescaling/s1/blob/main/data/tokenization.py)

Dataset background refers to [akftam/financial-qa-s1decontaminate-filtered-v1.0](https://huggingface.co/datasets/akftam/financial-qa-s1decontaminate-filtered-v1.0)