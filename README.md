# Sentence_Similarity

This project explores the use of word embeddings for sentence similarity analysis using a novel approach, with the ability to handle sentences with different word orders. The approach stands out as it does not necessitate the use of a full transformer encoder block, offering a more lightweight method for sentence similarity tasks.

## Approach

The method involves generating sentence vectors from word embeddings obtained from a FastText/Word2Vec/GloVe model, then calculating the cosine similarity between these sentence vectors to estimate the similarity between different sentences.

The unique aspect of this approach is the mathematical procedure to form sentence vectors. Instead of simply averaging/aggregating the word embeddings, this method alternates between performing the outer product (for even indexed vectors) and inner product (for odd indexed vectors) of the word vectors in a sentence, normalizing the resultant vectors at each step.

By considering the sentence structure and applying normalization at each step, this method mitigates the issue of vectors converging to zero as the sentence length increases, a problem common in many other methods. Additionally, this approach can handle changes in the word order, making it robust against the variations in sentence construction.

## Progress

The current state of the project includes:

- A FastText model trained locally on a diverse corpus of texts gathered from Reddit, Twitter, and other online sources.
- A function to convert sentences into vectors using the FastText model's word embeddings.
- A function to measure the cosine similarity between sentence vectors.

## To-Do List

- [ ] Further train the FastText model on a larger corpus for better generalization.
- [ ] Experiment with different dimensions for word embeddings.
- [X] Adjust the sentence vector function to normalize vectors at each step, preventing the issue of vectors converging to zero.
- [X] Test the sentence similarity function with a variety of sentences for robustness.
- [ ] Evaluate the model performance using standard NLP evaluation metrics.
- [ ] Implement and compare the performance of the model with Word2Vec and GloVe embeddings.
- [ ] Explore possibilities for parallelizing operations to enhance computational speed and scalability.

## Note

The pretrained FastText model was trained on various text corpora gathered from the internet, ensuring its capability to generalize across different text types. Although the project is in the experimental phase, the method's simplicity and lightweight nature make it a compelling alternative for sentence similarity computation tasks.
