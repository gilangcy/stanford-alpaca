# [Reproducing] Stanford Alpaca: An Instruction-following LLaMA Model
This is the repo for reproducing [Stanford Alpaca : An Instruction-following LLaMA Model](https://github.com/tatsu-lab/stanford_alpaca/blob/main/README.md). We finetune some of LLama2-based large language model using medical QA dataset. The repo contains:

- The [5K data](#dataset) conversations between patients and physicians used for fine-tuning the model.
- The code for [preparation data](#data-preparation).
- The code for [Fine Tuning the Model](#fine-tuning).
- The link for [Testing the Model](#testing-the-model).

## Dataset
We using the 5k generated dataset by [Chat Doctor](https://github.com/Kent0n-Li/ChatDoctor). The dataset is a generated conversations between patients and physicians from ChatGPT GenMedGPT-5k and disease database. Dataset also currated and modified to Indonesian Language Based. 

[`GenMedGPT-5k-id.json`](./GenMedGPT-5k-id.json) contains 5K instruction-following data we used for fine-tuning the Llama model.This JSON file is a list of dictionaries, each dictionary contains the following fields:

- `instruction`: `str`, describes the task the model should perform. Each of the 52K instructions is unique.
- `input`: `str`, optional context or input for the task. For example, when the instruction is "Summarize the following article", the input is the article. Around 40% of the examples have an input.
- `output`: `str`, the answer to the instruction as generated by `text-davinci-003`.

## Finetuning the Model
We fine-tune our models based on the step from Stanford Alpaca. We choose to train some LLama-based model. The model that we finetune are Polylm-7B, Llama-2-7B, Internlm-7B

## Testing the Model 

These are link for test the fine-tuned model :

1. [Polylm-7B](https://huggingface.co/spaces/dennyaw/polylm1.7b)
2. [Llama-2-7B](https://huggingface.co/spaces/dennyaw/Llama-2-7b-finetuned)
3. [Internlm-7B](https://huggingface.co/spaces/dennyaw/internlm-7b-finetuned)

### Authors

All interns below contributed equally and the order is determined by random draw.

- [Denny Andriana Wahyu](https://www.linkedin.com/in/denny-aw/)
- [Fadli Aulawi Al Ghiffari](https://www.linkedin.com/in/fadli-aulawi-al-ghiffari-9b4990148/)
- [Gilang Catur Yudishtira](https://www.linkedin.com/in/gilangcy/)

All advised by [Firqa Aqilla Noor Arasyi](https://www.linkedin.com/in/firqaana/)


