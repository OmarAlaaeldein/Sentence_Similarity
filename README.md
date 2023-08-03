# Sentence_Similarity
A hobby experiment to investigate possibility of using word embeddings to analyze sentence similarity using a novel approach that does not necessitate using a whole transformer encoder block

## To-Do List

- [ ] Train the word2vec model on larger corpus.
- [ ] Experiment with different sizes of word embeddings.
- [ ] Modify the sentence_vector function to normalize vectors at each step.
- [X] Test the sentence similarity function with various sentences.
- [ ] Evaluate the performance of the model.
- [ ] Implement the model with FastText and compare the performance.
- [ ] Explore possibilities of parallelizing operations for faster computation.

## Important

- The pertrained embedding model is trained on an aggregation of text corpuses locally
- For the objective of comparing sentences similiarty this approach is not currently performing optimally
