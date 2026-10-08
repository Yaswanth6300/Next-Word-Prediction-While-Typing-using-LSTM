# Next Word Prediction using LSTM

A deep learning project that predicts the next word while a user types, using a Long Short-Term Memory (LSTM) network trained on a text corpus.

## How it works
1. **Preprocessing:** Tokenize text and build input sequences with the next word as the label.
2. **Embedding layer:** Maps words to dense vectors.
3. **LSTM layer(s):** Learns context from the sequence of previous words.
4. **Dense + softmax layer:** Outputs probabilities over the vocabulary; the top 1-3 words are suggested.

## Tech stack
Python, TensorFlow/Keras, NumPy, NLTK

## Usage
```bash
pip install -r requirements.txt
python train.py      # train the model
python predict.py    # type text and get next-word suggestions
```

## Future improvements
- Train on a larger dataset
- Add a Transformer-based comparison
- Build a simple web or keyboard UI
