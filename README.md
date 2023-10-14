# NaLaFi
This repo contains data and code to work on Natural Language Fingerprints (NaLaFi), and to replicate the results in Bentz (2023). The code should be run in the following order:

- randomStringGenerator.Rmd: generates random strings for comparison to natural languages and other sign strings.
- shuffledTextGenerator.Rmd: takes the files in folder NaLaFi/data/writing and shuffles the characters randomly.
- simpleStats.Rmd: this gives an overview of the files in NaLaFi/data in terms of number of files per subcorpus and number of characters per file.
- sampler.Rmd: samples chunks of UTF-8 characters of pre-defined length (e.g. 10, 100, 1000) and stores them in NaLaFi/samples. Note that this folder should be emptied before re-running the code.
- estimations.Rmd: calculating the feature values (TTR, unigram entropy, entropy rate, repetition measure) for each string of UTF-8 characters (one per line) in the files of NaLaFi/samples. The output is a csv file stored in NaLaFi/results/features.csv. Note that this file should be deleted before re-running the code.


Reference

Bentz (2023). The Zipfian Challenge: Learning the statistical fingerprint of natural languages. CoNLL, Singapore.
