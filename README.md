## Taylor Series ~ Evaluation Test

### Problem Statement:
Task 1: Generate datasets of functions with their Taylor expansions up the fourth order. Tokenize the dataset.

Task 2: Train an LSTM model to learn the Taylor expansion of each function.

Task 3: Similarly Train a Transformer model to learn the Taylor expansion of each function.

---

We have implemented two neural network architectures namely LSTM and Transformer designed to translate mathematical expressions into their Taylor series expansions. The system works with mathematical expressions in prefix notation for efficient computation.

The first part of the code focuses on data generation, using a custom MathExpression class that handles mathematical operations in prefix notation. This class can generate random expressions, convert between notations, and work with the SymPy library for symbolic mathematics. It creates training data pairs consisting of original expressions and their corresponding Taylor series expansions.

The second part implements two neural network architectures:

+ An LSTM-based encoder-decoder model with embedding layers for sequence-to-sequence translation
+ A Transformer model with positional encoding and multi-head attention mechanisms

Both models are trained on the generated dataset with appropriate loss functions and optimizers, evaluating their performance on mathematical expression translation tasks. The code also includes training loops and evaluation functions for both architectures.

+ At the end of 100 epochs LSTM model acheives an excellent accuracy of 100%. Similarly Transformer also acheives a good accuracy of 97.15%

### References

+ https://github.com/hbprosper/symbolic-ai
+ Deep Learning for Symbolic Mathematics: https://arxiv.org/pdf/1912.01412
+ Attention is all you need: https://arxiv.org/pdf/1706.03762
+ https://github.com/tm4roon/pytorch-seq2seq
