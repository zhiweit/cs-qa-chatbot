# CSInterviewChatbot
Computer Science Interview Chatbot to help you ace your technical interviews!

The primary goal is to develop a Telegram chatbot designed to assist users in preparing for technical interviews. This user-friendly platform will allow candidates to ask computer science-related questions and receive relevant, real-time answers. By leveraging the accessibility and convenience of Telegram, our chatbot will provide an interactive and immediate resource, enhancing users’ preparation and confidence.

To achieve this, we will be leveraging a sequence-to-sequence (Seq2Seq) approach for the chatbot’s architecture. By employing this approach, we aim to develop a chatbot that can provide coherent and relevant responses, making it a valuable tool to help candidates prepare for technical interviews.  

In this project, we will be experimenting with 3 different approaches: **LSTM-LSTM RNN Architecture**, **DistilRoberta-LSTM Hybrid Architecture** and **GPT-2 Transformer Architecture**.

**Datasets:**
For this project, we sourced Computer-Science related Question-Answer data from 4 origins:
1. [Github repository by Kunal Kumar (Kunal, n.d.)](https://github.com/kunal164107/Interview-Chatbot/blob/master/data/twitter/final1.txt)
2. [Hugging Face - data-science-qa (Team Bay, n.d.)](https://huggingface.co/datasets/team-bay/data-science-qa)
3. [Kaggle - Software Engineering Interview Questions Dataset (Syed, n.d.)](https://www.kaggle.com/datasets/syedmharis/software-engineering-interview-questions-dataset)
4. [Kaggle - Computer Science Theory QA Dataset (Matin, n.d.)](https://www.kaggle.com/datasets/mujtabamatin/computer-science-theory-qa-dataset)

**To run:**
1. Run preprocessing.ipynb to preprocess dataset (cleaned dataset: combined_data.csv)
2. Run 'LSTM-LSTM_training.ipynb' to train RNN model
3. Run 'DistilRoberta-LSTM_training.ipynb' to train Hybrid model
4. Run 'GPT2_Training.ipynb' to train Transformer model
5. Run 'TelegramHosting.py' to host on Telegram - Syahmim pls help to update
