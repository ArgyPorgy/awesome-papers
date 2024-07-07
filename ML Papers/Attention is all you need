##Explanation

Before diving into how transformers work, you gotta understand the basics of RNNs (Recurrent Neural Networks).



##So how does RNN work?

Imagine you have a sentence like "I have a cat," and you want to translate it from English to Hindi. Each word in this sentence is converted into a numerical representation called a word vector. These vectors are fed into an encoder, which processes them step-by-step to generate hidden states (h0, h1, h2, h3). Each hidden state contains information from the previous ones, so by the time you get to h3, it has accumulated context from the entire sentence.

The final hidden state (h3) is passed to a decoder, which translates it into the target language. The decoder produces new hidden states (h4, h5, ...) that help generate the translated output. However, RNNs often struggle to retain context over long sequences because the information are jammed at h3 and then sent to decoder. Also RNN has vanishing gradient problem. These leads to the loss of clarity. This is where transformers come into play.



##Now how does Transformers work?

Transformers do the whole process with their encoder-decoder architecture, focusing on attention mechanisms to handle long-range dependencies better.

Encoder: The encoder in a transformer consists of multiple layers. Each layer has:

Multi-Head Self-Attention Mechanism: This mechanism lets the model look at different positions in the input sentence simultaneously. It's like having multiple lenses to focus on different parts of the sentence at once.

Feed-Forward Neural Network: Applied to each position separately, it processes the data further.


Decoder: The decoder also has multiple layers and works similarly but with a twist:

Masked Multi-Head Self-Attention: This prevents the model from looking ahead in the sequence, ensuring predictions are based only on past and present information.

Encoder-Decoder Attention: This layer allows the decoder to focus on relevant parts of the input sentence, making the translation more accurate.
Attention Mechanism:

Scaled Dot-Product Attention: This is where queries (Q), keys (K), and values (V) come into play. Think of K as detailed information (like a person’s name, height, weight), Q as the question you’re asking (e.g., "What's the name?"), and V as the answer (e.g., "Arghya" for the name). The model calculates attention scores, scales them, and uses a softmax function to get weights. These weights help determine the most relevant parts of the input, which are then used to generate the output.

Positional Encoding: Transformers don't process the sequence step-by-step like RNNs, so they need a way to understand the order of the words. Positional encoding adds this information to the word vectors, giving the model a sense of sequence.

Multi-Head Attention: This involves running multiple attention mechanisms in parallel, allowing the model to attend to different parts of the sentence in various ways. The outputs are then combined and processed together.

In summary, transformers use these attention mechanisms to efficiently capture long-range dependencies and process sequences in parallel. This overcomes the limitations of RNNs, resulting in better performance for tasks like machine translation.




##References:

https://lena-voita.github.io/nlp_course/language_modeling.html (good explanation with images)

https://arxiv.org/abs/1706.03762 (the actual paper)

https://www.youtube.com/watch?v=iDulhoQ2pro (great vid to start with, explained really well)
