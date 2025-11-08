#  Bilingual Translation Using LSTM Seq2Seq Architecture

This project implements a **Sequence-to-Sequence (Seq2Seq)** deep learning model using **Long Short-Term Memory (LSTM)** networks for **English-to-French language translation**. The model learns from bilingual text pairs and demonstrates how encoder–decoder architectures can perform neural machine translation effectively.

---

## Project Overview

The project uses a **Neural Machine Translation (NMT)** approach based on **LSTM Encoder–Decoder architecture** to translate sentences from **English to French**.  
The dataset consists of bilingual text pairs extracted from the `fra.txt` file containing English–French sentence mappings.

---

##  Dataset Details

- **Dataset name:** `fra.txt` (French-English bilingual pairs)  
- **Number of samples:** 10,000  
- **Number of unique input tokens:** 71  
- **Number of unique output tokens:** 93  
- **Maximum input sequence length:** 16  
- **Maximum output sequence length:** 59  

Each line in the dataset contains a pair of sentences separated by a tab (`\t`)

---

##  Workflow

1. **Import Libraries**  
   Import required libraries such as NumPy, TensorFlow/Keras, and Matplotlib for modeling and visualization.

2. **Data Preprocessing**  
   - Read the dataset (`fra.txt`)  
   - Clean and normalize text data  
   - Tokenize the input (English) and target (French) texts  

3. **Vectorize the Data**  
   Convert sentences into one-hot encoded tensors suitable for model training.

4. **Define Encoder–Decoder Data**  
   Prepare input and target sequences for encoder and decoder components.

5. **Build the LSTM Seq2Seq Model**  
   - Encoder: Processes English input sequence and outputs hidden states.  
   - Decoder: Takes encoder states and generates French output sequence.  

6. **Model Summary & Visualization**  
   View model architecture and visualize the encoder–decoder connection using Keras utilities.

7. **Train and Compile the Model**  
   - Compile with **RMSprop** or **Adam** optimizer  
   - Train using teacher forcing  
   - Evaluate loss convergence  

8. **Define Sampling Models**  
   Create inference models for encoder and decoder to perform predictions on unseen data.

9. **Decode Sequence**  
   Implement decoding logic to convert model output (token indices) into readable French sentences.

10. **Translate Sentences**  
    Input English sentences → Output predicted French translations.

---

##  Model Architecture

Encoder (LSTM) ---> Context Vector ---> Decoder (LSTM)
↑ ↓
English Input French Output

##  Results

- Successfully trained a Seq2Seq LSTM model for English–French translation.  
- The model effectively converts short English sentences into corresponding French translations.  
- Example:

| English Input | Predicted French Output |
|----------------|--------------------------|
| How are you? | Comment ça va ? |
| I love you. | Je t’aime. |
| What is your name? | Comment tu t’appelles ? |


