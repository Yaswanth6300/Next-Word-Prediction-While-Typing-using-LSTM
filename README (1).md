# Next Word Prediction using LSTM

A deep learning project that predicts the next word while a user types, using a Long Short-Term Memory (LSTM) network trained on a text corpus.

## Overview
Next-word prediction is a language-modeling task. The model reads the words typed so far and outputs the most likely next words, similar to keyboard suggestions on a phone.

## How it works
1. **Preprocessing:** Tokenize the text and build input sequences, using the previous words as input and the following word as the label.
2. **Embedding layer:** Maps each word index to a dense vector that captures meaning and similarity.
3. **LSTM layer(s):** Learns context from the sequence of previous words, using memory cells and gates to retain relevant information over longer ranges.
4. **Dense + softmax layer:** Outputs a probability distribution over the vocabulary. The top 1-3 words are shown as suggestions.
5. **Training:** Categorical cross-entropy loss with the Adam optimizer.

## Tech stack
- Python
- TensorFlow / Keras
- NumPy
- NLTK

## Project structure
```
.
├── data/              # training text corpus
├── train.py           # builds sequences and trains the LSTM model
├── predict.py         # loads the model and suggests next words
├── requirements.txt
└── README.md
```

## Installation
```bash
git clone https://github.com/<your-username>/next-word-prediction-lstm.git
cd next-word-prediction-lstm
pip install -r requirements.txt
```

## Usage
```bash
python train.py      # train the model
python predict.py    # type text and get next-word suggestions
```

Example:
```
Input:  "i want to"
Output: ["go", "be", "see"]
```

## Results
Add your training accuracy, loss, and a few sample predictions here.

## Future improvements
- Train on a larger and more diverse dataset
- Compare against a Transformer-based model
- Build a simple web or keyboard UI for live suggestions

## License
MIT
