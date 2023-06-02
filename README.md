# Text-generation-using-GPT-and-Transformers

**Overview**

This blog is all about how AI will generate a bunch of text lines from a given input sequence. For text generation, we are using two things in python. As a language model, we are using GPT-2 Large Pre-trained model and for the Text Generation pipeline, we are using Hugging Face Transformers pipelines.

**GPT-2*

GPT-2 is a large transformer-based language model with 1.5 billion parameters, trained on a dataset of 8 million web pages. GPT-2 is trained with a simple objective: predict the next word, given all of the previous words within some text. The diversity of the dataset causes this simple goal to contain naturally occurring demonstrations of many tasks across diverse domains. GPT-2 is a direct scale-up of GPT, with more than 10X the parameters and trained on more than 10X the amount of data.
Basically, GPT-2 is a language model used to generate the next text from given text.

**Hugging Face Transformers**

🤗(Hugging Face) Transformers (formerly known as PyTorch-transformers and PyTorch-pretrained-bert) provides general-purpose architectures (BERT, GPT-2, RoBERTa, XLM, DistilBert, XLNet…) for Natural Language Understanding (NLU) and Natural Language Generation (NLG) with over 32+ pre-trained models in 100+ languages and deep interoperability between TensorFlow 2.0 and PyTorch.
Basically Hugging Face Transformers is the mega python package that has some pre-defined or pre-trained functions, pipelines, and models. which we can use for our natural language processing tasks.

**Build the model**

We create our scaled down GPT model with the following layers:

* One keras_nlp.layers.TokenAndPositionEmbedding layer, which combines the embedding for the token and its position.
* Multiple keras_nlp.layers.TransformerDecoder layers, with the default causal masking. The layer has no cross-attention when run with decoder sequence only.
* One final dense linear layer

**Inference**

* Greedy search
* Beam search
* Random search
* Top-K search
* Top-P search
