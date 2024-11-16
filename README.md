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
- **PEFT_Model**: Contains code for fine-tuning `Llama2-chat-13B-hf` and `Llama2-chat-7B-hf` using the same train sets as the original paper, using PEFT with LoRA. Also includes code of generating responses for evaluation on the same test set as the original paper.
  - **Models Included**:
    - **Finetuned-13B-absolute**
      - HF Checkpoint: [🤗 SiqiiWa/llama2-13b-ft-absolute_p1-full](https://huggingface.co/SiqiiWa/llama2-13b-ft-absolute_p1-full)
      - Size: 13B
    - **Finetuned-13B-confidence-num**
      - HF Checkpoint: [🤗 SiqiiWa/llama2-13b-ft-confidence-num_p2-full](https://huggingface.co/SiqiiWa/llama2-13b-ft-confidence-num_p2-full)
      - Size: 13B
    - **Finetuned-13B-confidence-verb**
      - HF Checkpoint: [🤗 SiqiiWa/llama2-13b-ft-confidence-verb_p3-full](https://huggingface.co/SiqiiWa/llama2-13b-ft-confidence-verb_p3-full)
      - Size: 13B
    - **Finetuned-13B-multisample**
      - HF Checkpoint: [🤗 SiqiiWa/llama2-13b-ft-multisample_p1-1k](https://huggingface.co/SiqiiWa/llama2-13b-ft-multisample_p1-1k)
      - Size: 13B
    - **13B-Baseline**: Llama-2-13b-chat-hf baseline model for performance comparison.
      - Llama2-Chat-13b [meta-llama/Llama-2-13b-chat-hf](https://huggingface.co/meta-llama/Llama-2-13b-chat-hf)
      - Size: 13B
    - **Finetuned-7B-absolute**
      - HF Checkpoint: [🤗 SiqiiWa/llama2-7b-ft-absolute_p1-full](https://huggingface.co/SiqiiWa/llama2-7b-ft-absolute_p1-full)
      - Size: 7B
    - **Finetuned7B-confidence-num**
      - HF Checkpoint: [🤗 SiqiiWa/llama2-7b-ft-confidence-num_p2-full](https://huggingface.co/SiqiiWa/llama2-7b-ft-confidence-num_p2-full)
      - Size: 7B
    - **Finetuned-7B-confidence-verb**
      - HF Checkpoint: [🤗 SiqiiWa/llama2-7b-ft-confidence-verb_p3-full](https://huggingface.co/SiqiiWa/llama2-7b-ft-confidence-verb_p3-full)
      - Size: 7B
    - **Finetuned-7B-multisample**
      - HF Checkpoint: [🤗 SiqiiWa/llama2-7b-ft-multisample_p1-1k](https://huggingface.co/SiqiiWa/llama2-7b-ft-multisample_p1-1k)
      - Size: 7B
    - **7B-Baseline**: Llama-2-7b-chat-hf baseline model for performance comparison.
      - Llama2-Chat-7b [meta-llama/Llama-2-13b-chat-hf](https://huggingface.co/meta-llama/Llama-2-7b-chat-hf)
      - Size: 7B
