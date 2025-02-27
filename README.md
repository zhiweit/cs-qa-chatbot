# Computer Science Question Answering (CS QA) Chatbot

The primary goal is to develop a chatbot that answers computer science related questions.

## Demo
Telegram deployment on model using LSTM architecture with dot product attention mechanism.


https://github.com/user-attachments/assets/53e6e95c-1511-4718-85b5-ce038754103f




Three different approaches were tried to develop this chatbot: **LSTM-LSTM RNN Architecture**, **DistilRoberta-LSTM Hybrid Architecture** and **GPT-2 Transformer Architecture**.

**Datasets:**
For this project, we sourced Computer-Science related Question-Answer data from 4 origins:

1. [Github repository by Kunal Kumar (Kunal, n.d.)](https://github.com/kunal164107/Interview-Chatbot/blob/master/data/twitter/final1.txt)
2. [Hugging Face - data-science-qa (Team Bay, n.d.)](https://huggingface.co/datasets/team-bay/data-science-qa)
3. [Kaggle - Software Engineering Interview Questions Dataset (Syed, n.d.)](https://www.kaggle.com/datasets/syedmharis/software-engineering-interview-questions-dataset)
4. [Kaggle - Computer Science Theory QA Dataset (Matin, n.d.)](https://www.kaggle.com/datasets/mujtabamatin/computer-science-theory-qa-dataset)

## Implementation Overview

### Architectures

1. **LSTM-LSTM RNN Architecture**:

   - A traditional sequence-to-sequence approach with Luong Attention to improve response coherence.

2. **DistilRoberta-LSTM Hybrid Architecture**:

   - Combines DistilRoberta for contextual embeddings with LSTM for sequential decoding.
   - Features a fine-tuned encoder with Luong Attention for dynamic focus on inputs.

3. **GPT-2 Transformer Architecture**:
   - A fully Transformer-based model with self-attention mechanisms for robust language understanding and generation.

## How to Run the Project

### Preprocessing

1. Run `preprocessing.ipynb` to clean and unify the dataset into a CSV file (`combined_data.csv`).
   - **Required Files**: `final1.txt`, `intents.json`, `SoftwareQuestions.csv`

### Training

2. Run 'LSTM-LSTM_training.ipynb' to train RNN model
3. Run 'DistilRoberta-LSTM_training.ipynb' to train Hybrid model
4. Run 'GPT2_Training.ipynb' to train Transformer model

Note: Instructions on how to run the models are included in the notebooks

### Hosting on Telegram

5. Deploy the chatbot on Telegram:
   - Each `.ipynb` file (`LSTM-LSTM_training.ipynb`, `DistilRoberta-LSTM_training.ipynb`, `GPT2_Training.ipynb`) includes a Telegram hosting block of code at the end.
   - To deploy the chatbot, simply run the Telegram block, ensuring you replace `YOUR_TOKEN` with the API token obtained from BotFather on Telegram.
   - To get Token: Search for @BotFather on Telegram and Start a Chart. Type /newbot and follow the instructions to name your bot and set a username (it must end with "bot", e.g., my_test_bot). Thereafter, BotFather would provide the API token
   - This block integrates the trained model with a Telegram bot, allowing real-time interaction with users.

---

## Performance Evaluation

### Evaluation Metrics

- **BERTScore**: Measures semantic similarity between responses and ground truth.
- **BLEU**: Evaluates precision of n-grams in generated responses.
- **ROUGE**: Assesses overlap of unigrams and sequences between generated and reference answers.

### Key Findings

#### LSTM-LSTM Model

- **BERTScore**: 0.95
- **BLEU**: 0.75
- **ROUGE-1**: 0.84
- **ROUGE-L**: 0.82

#### DistilRoberta-LSTM Hybrid

- **BERTScore**: 0.97
- **BLEU**: 0.71
- **ROUGE-1**: 0.79
- **ROUGE-L**: 0.77

#### GPT-2 Transformer

- **BERTScore**: 0.87
- **BLEU**: 0.18
- **ROUGE-1**: 0.38
- **ROUGE-L**: 0.34

### Observations

- **GPT-2 Transformer** performed well in generating coherent and semantically meaningful answers.
- **DistilRoberta-LSTM Hybrid** excelled in contextual understanding, and had the highest BERTScore.
- **LSTM-LSTM RNN** provided satisfactory results but sometimes lacked depth/relevance to the question.

---

## Future Improvements

- **Advanced Inference Techniques**:
  - Implement Beam Search to enhance response coherence.
- **Parameter Optimisation**:
  - Use Grid Search for fine-tuning hyperparameters.
- **Fallback Mechanisms**:
  - Integrate BERTScore for real-time similarity checks and provide alternative resources for low-confidence responses.
- **Dataset Expansion**:
  - Include diverse interview topics beyond computer science, such as behavioural questions and case studies.

---

## Contributors

- **Bryan Chua Jiaheng**
- **Leck Yan Qing Elvy**
- **Syahmim Chukhan Bin Shamsudin**
- **Thean Zhi Wei**

---

## Academic Context

**Course**: CS425: Natural Language Communication  
**Instructor**: Dr. Wei Gao  
**Institution**: Singapore Management University, AY 2024-2025 T1

---
