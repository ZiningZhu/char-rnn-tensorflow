#Notes for navigating within char-rnn-tensorflow#

- How do we control the dimension of hidden layers within models?
  `args.rnn_size`

- How is the char-level model embedded?
  `tf.get_variable("embedding")`.

- Where does the embedding come from? Text file -> TextLoader -> Preprocess!
  TODO - What is the input to `tf.nn.embedding_lookup()?` List of characters?
  TODO - confirm that the model loss is calculated from predicted char and

- Does this model have something like beam search decode? Or is it just brutal char-by-char decoding?
  TODO

- In sampling, does the model sample using a random initial state or a fixed character as initial state? How does the batch 

- Modify input dataset and train them; specify the input-output dimensions. Run tensorboard to see the visualized data.
  Looks good

- How does the dropout work? Where does the model apply it? Why use a `RNNDropoutWrapper` in addition to a `tf.nn.dropout` on the inputs?

- Possibility of modifying into a Bi-directional RNN?
