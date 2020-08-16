# Topic Aware Chatbot Using Transformers
# Can we build a neural net based chatbot to produce responses that are relevant and aware of the current context?
# Concept - Pay Attention to Attention
Context relationships are build between the input and output words based on modifiedWord embedding vectors
# Pay Attention to Attention - additional context
Additional context relationships are build between the topic words and encoder-decoder outputs based on modified word embedding vectors from the topic
# Current Research - Seq2Seq Model with Topic Attention
### Current Research - Limitations
We rely solely on the context vector to encode the entire input sequence meaning, it is likely that we will have information loss. 
Long input sequences suffer considerably using this mechanism
# Proposed TA-Transformer Architecture
### Embedding layer with positional encoding
- Encoder Layer - Self Attention, Feed Forward 
- Decoder Layer - Self Attention, Encoder Decoder Attention, Topic Attention, Feed Forward 
- Linear layer projects vectors to logits vector
- Final softmax layer will generate the probability values for the vocabulary
### Topic Creation - Tf-idf scoring process
- NMF
- LDA
### Transformer Model Topic Attention Processing

Q = Encoder-Decoder Attention Output vectorK = V = Weighted Topic Word Embedding Vector

### Evaluation MetricsLoss Function : Sparse Categorical Cross Entropy
### BLEU Score : Bleu score was used to evaluate the generated sentence to the expected sentence
# Future work
- Use transfer learning with BERT encoder pre-trained outputs and integrating it with the LSTM decoder model.
- Try other formulas to compute the values of topic embedding matrix to see if we can get better results and analyze them
- Use perplexity scores to see if the comparison results are better
