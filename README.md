# WORDS PREDICTOR MODEL
Deep Learning model which is using bidirectional RNN LSTM to predict the next word in the sentence.


## INTRODUCTION
### Recurrent Neural Networks
Recurrent Neural Network(RNN) are a type of Neural Network where the output from
previous step are fed as input to the current step. In traditional neural networks, all the
inputs and outputs are independent of each other, but in cases like when it is required to
predict the next word of a sentence, the previous words are required and hence there is a
need to remember the previous words. Thus RNN came into existence, which solved this
issue with the help of a Hidden Layer. The main and most important feature of RNN
is Hidden state, which remembers some information about a sequence. They are networks
with loops in them, allowing information to persist.
These loops make recurrent neural networks seem kind of mysterious. However, if you think a
bit more, it turns out that they aren’t all that different than a normal neural network. A
recurrent neural network can be thought of as multiple copies of the same network, each
passing a message to a successor.
And they certainly are used! In the last few years, there have been incredible successes
applying RNNs to a variety of problems: speech recognition, language modeling, translation,
image captioning… The list goes on.
Essential to these successes is the use of “LSTMs,” a very special kind of recurrent neural
network which works, for many tasks, much much better than the standard version. Almost
all exciting results based on recurrent neural networks are achieved with them. It’s these
LSTMs that this essay will explore.

### LSTM Networks
Long Short Term Memory networks – usually just called “LSTMs” – are a special kind of
RNN, capable of learning long-term dependencies. They were introduced by Hochreiter &
Schmidhuber (1997), and were refined and popularized by many people in following
work.1 They work tremendously well on a large variety of problems, and are now widely used.
LSTMs are explicitly designed to avoid the long-term dependency problem. Remembering
information for long periods of time is practically their default behavior, not something they
struggle to learn!
All recurrent neural networks have the form of a chain of repeating modules of neural
network. In standard RNNs, this repeating module will have a very simple structure, such as a
single tanh layer.
LSTMs also have this chain like structure, but the repeating module has a different structure.
Instead of having a single neural network layer, there are four, interacting in a very special
way.
The key to LSTMs is the cell state. The LSTM does have the ability to remove or add
information to the cell state, carefully regulated by structures called gates.
Gates are a way to optionally let information through. They are composed out of a sigmoid
neural net layer and a pointwise multiplication operation. The sigmoid layer outputs numbers
between zero and one, describing how much of each component should be let through. A
value of zero means “let nothing through,” while a value of one means “let everything
through!” An LSTM has three of these gates, to protect and control the cell state.

### METHODOLOGY TO BE FOLLOWED
What is the neural network task in our case?
LSTM (Long Short-Term Memory) are very good for analyzing sequences of values and
predicting the next one. For example, LSTM could be a good choice if you want to predict the
very next point of a given time series.
The phrases (sentences) are basically sequences of words. So, it is natural to assume LSTM
could be useful to generate the next word of a given sentence. In summary, the objective of
our LSTM neural network will be to guess the next word of a given sentence (i.e. a sequence
of words).
1. Read Data - Here we use Spacy library to retrieve the words using its tokenizer, keep
them in small letters, and removing all carriage returns
2. Create the dictionary - The dictionary is the list of all words contained in texts,
without duplicates. In addition, for each word, we will assign it an index.
3. Create Sentences List - Now, we have to create the training data for our LSTM. We
create two lists: Sequences: this list contains the sequences of words (i.e. a list of words)
used to train the model, Next words: this list contains the next words for each sequences of
the sequences list.

4. Build the LSTM Model - We are using Keras that provides a very good abstraction to
design a Neural Network architecture.
5. Train the Model
6. Generate Sentences


## Implementation

How does the keyboard on your phone know what you would like to type next? Language prediction is a Natural Language Processing - NLP application concerned with predicting the text given in the preceding text. Auto-complete or suggested responses are popular types of language prediction. The first step towards language prediction is the selection of a language model. This article shows different approaches one can adopt for building the Next Word Predictor you have in apps like Whatsapp or any other messaging app.


![Image](https://github.com/shivang1305/words_predictor/blob/main/img.png) 


Word Prediction or Text Generation is a Language modeling problem, A classic ideation in Machine Learning and Deep Learning. In here, we are trying to do the word prediction using LSTM Recurrent Neural Network or RNN. Neural Network is actually said to be a design, inspired by how human brains work. They recognize patterns and clusters and use them to give us powerful insights and terrific applications of different kind of levels.


## Model Information
![Model Information](https://github.com/shivang1305/words_predictor/blob/main/Screenshot%20(203).png) 
#
## Model Accuracy
![Model Information](https://github.com/shivang1305/words_predictor/blob/main/Screenshot%20(205).png) 
