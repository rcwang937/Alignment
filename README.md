# alignment

This repository is a reimplementation of the paper [Alignment for Honesty](https://arxiv.org/abs/2312.07000). We reproduce the fintuning approaches and evaluations presented in the paper to assess the alignment of large language models toward honest responses.

## Repository Structure

- **Evaluation**: Contains code for evaluating model performance based on honesty alignment. Key scripts include:
  - `alignment_eval.ipynb`: Main script for evaluating model alignment.
  - `remove_utility.ipynb`: Utility functions for handling alignment-related operations.

- **Original_Model**: Contains code for reimplementing the two best-performing models from the original paper, along with a baseline model for comparison.
  - **Models Included**:
    - **confucius-confidence-verb**
      - HF Checkpoint: [🤗 GAIR/confucius-confidence-verb](https://huggingface.co/GAIR/confucius-confidence-verb)
      - Size: 13B
      - License: Llama2-Chat
    - **confucius-multisample**
      - HF Checkpoint: [🤗 GAIR/confucius-multisample](https://huggingface.co/GAIR/confucius-multisample)
      - Size: 13B
      - License: Llama2-Chat
    - **Baseline**: Llama-2-13b-chat-hf baseline model for performance comparison.
      - Llama2-Chat-13b [meta-llama/Llama-2-13b-chat-hf](https://huggingface.co/meta-llama/Llama-2-13b-chat-hf)
      - Size: 13B
