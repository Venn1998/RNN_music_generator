# RNN_music_generator
Implementation of a recurrent neural network for the generation of music, following the work presented in [JamBot: Music Theory Aware Chord Based Generation of Polyphonic Music with LSTMs, by Gino Brunner, Yuyi Wang, Roger Wattenhofer and Jonas Wiesendanger](https://arxiv.org/pdf/1711.07682.pdf). Some parts of the code attached is taken from the repository of the authors of the paper. We built a LSTM network to generate chords from MIDI files. Finally, we used the embedding layer of the model to project the chords in 2D (with PCA) and visualize the concept of word2vec: we'll see that the model has learned the Circle of Fifths.

The notebook RNN_music.ipynb is structured in 4 parts:
1) We explore the structure of MIDI (Musical Instrument Digital Interface) files and play with some functionalities of the pretty_midi library.
2) We build a LSTM model that, trained on sequences of chords of different songs, learns which chord is more likely to be played given the list of chords played previously.
3) Our LSTM model has an embedding layer that learns to encode the chords with lower dimensionality. We explore this embedding layer with PCA analysis so that we can observe the effect of word2vec embedding.
4) We concentrate just on the chords of the Circle of Fifths and perform the same analysis: we can clearly see that the embedding layer of our model has learned this sequence of chords (see file learned_5th.png)
