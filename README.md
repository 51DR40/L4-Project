# L4-Project

# Evaluating the Effectiveness of LLM-driven Code Refactoring Suggestions in Enhancing Python Readability and Comprehension for Novice Programmers

## Introduction

This project explores the application of Large Language Models (LLMs) in optimizing the learning curve for novice programmers and assessing the effectiveness of AI-assisted learning compared to self-paced learning environments. The report investigates the ability of LLMs to refactor human-written code, improving its readability and maintainability. To ensure efficient deployment of LLMs on lower-resource systems, two fine-tuning techniques, LoRA and basic fine-tuning, are compared to create a smaller language model that retains most of its performance. Through a user study involving novice programmers, the impact of an AI-assisted learning environment on code comprehension is evaluated and compared to a self-paced learning approach.

## Methodology

The methodology consists of two main parts:

1. **RQ1 - Refactoring/Maintainability**: A larger model is selected and used to refactor code from a chosen dataset. Prompt engineering and hyperparameter tuning are employed to optimize the model's ability to refactor code and provide explanations. The maintainability and readability of the LLM-refactored code are assessed using standard metrics such as the maintainability index and Pylint, and compared to the original human-written code.

2. **RQ2 - Fine-tuning and User Testing**: A smaller model is fine-tuned specifically for refactoring and explaining code to novices. User tests are conducted under timed conditions, where novice programmers explain the problem, solution, and comprehension of their code in two settings: a self-learning environment using online resources and an environment with assistance from the fine-tuned model. The model's outputs and novices' experiences are tracked to validate the impact of the AI-assisted environment on code comprehension.

## Files

- `AugmentedData.ipynb`: This script generates refactored code outputs and explanations for each code snippet in the dataset, augmenting the dataset with these new features and storing it in JSON format as `augmented_dataset.json`.

- `maintainabilitytest.py`: This file computes the maintainability and readability scores for each original code and refactored code pair from the augmented dataset, creating a new dataset called `MI_pylint.csv` containing the maintainability index and Pylint PEP8 style score for each pair.

- `deepseek_7b_LoRA.ipynb`: This notebook implements the LoRA technique for fine-tuning the DeepSeek-Coder-7B model.

- `deepseek_finetuned.ipynb`: This notebook performs basic fine-tuning on the DeepSeek-Coder-7B model.

- `user_testing.ipynb`: This notebook sets up the interactive testing environment using the Oobabooga/text-generation-webui platform, enabling users to engage in conversations with the AI model and evaluate its performance in code refactoring and explanation tasks.
