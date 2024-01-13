# Story Generation using LSTM & GRU

## Project Overview
Machines, powered by advancements in Natural Language Processing (NLP), can now autonomously weave stories with contextual understanding. This project leverages NLP tools and libraries to build a model capable of automatically generating rich stories. Text generation, a branch of NLP, finds applications in various domains such as automatic documentation systems, letter writing, and report generation.

## Dataset
The project utilizes a dataset obtained from a website filled with stories. You can find the dataset [here](http://www.classicshorts.com/bib.html).

## Methodology
- Data preprocessing involves removing punctuation and using sentences with 7 or more words for training.
- Training sets are limited to 100,000 instances to manage compute memory space.
- Input and output training instances are generated from the dataset.
- All words are vectorized using one-hot coding.
- The model uses a bidirectional LSTM network with 256 hidden units, "relu" activation in the inner layer, and "softmax" activation in the outer layer.
- Keras library is employed for training the model.
- Implementation is done in Python using libraries such as Scikit-learn, NumPy, and Gensim.

## Model Configuration
- Input sequence length (excluding context vector): 8
- Context vector: V-dimensional vector (size of vocabulary)
- Configuration: All-to-one configuration, where the input contains a context vector, and the output contains the next word in the sequence.

## Prediction Phase
- Two sets of input from the user: sequence of seed words and context word(s).
- The network assembles input and predicts subsequent words.
- The process continues until the sentence is completed, indicated by dots.
- The next context word is then used for generating the next sentence.

## Evaluation
- The model minimizes drag loss by adjusting parameters like the number of neurons, layers, stack size, and sequence length.
- Human evaluation achieved 79% accuracy.
- Further improvements can be made by considering the meaning of words in context and incorporating synonyms.

## Future Extensions
The system can be extended for automatic generation of news, news articles, jokes, or posts.

## Dependencies
- Python
- Scikit-learn
- NumPy
- Gensim

## How to Use
1. Install the required dependencies.
2. Download the dataset from [here](http://www.classicshorts.com/bib.html) and place it in the appropriate directory.
3. Run the code to train the model.
4. Provide seed words and context words during the prediction phase.

Happy Story Generation!
