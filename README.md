# Part-of-Speech-Tagger

This project is an implementation of part-of-speech tagger in Python, using Bayesian networks based on skeleton code by Prof.David Crandall

-label.py, is the main program (skeleton code by Prof. David Crandall)
-pos scorer.py, has the scoring code, (skeleton code by Prof. David Crandall)
-and pos solver.py, contains the actual part-ofspeech estimation code.(implemented as part of project based on skeleton code).

The files bc.train and bc.test are large corpus of labeled training and testing data, consisting of nearly 1 million words 
and 50,000 sentences. The file format of the datasets is quite simple: each line consists of a word, followed by a space, 
followed by one of 12 part-of-speech tags: ADJ (adjective),ADV (adverb), ADP (adposition), CONJ (conjunction), DET (determiner), NOUN, 
NUM (number), PRON(pronoun), PRT (particle), VERB, X (foreign word), and . (punctuation mark). Sentence boundaries are
indicated by blank lines.

Using the above datasets, the following steps are performed:
1. learning
2. naive inference
3. sampling
4. Approximate marginal inference(MCMC)
5. Exact maximum a posteriori inference(Viterbi algorithm)

The program label.py takes as input two filenames:a training file and a testing file(ex.bc.train,bc.test). 
The program uses the training corpus for Step 1, and then displays the output of Steps 2 through 6 on each sentence in the testing file. 
It also displays the logarithm of the posterior probability for each solution it finds, as well as a running evaluation showing the percentage
of words and whole sentences that have been labeled correctly according to the ground truth.
