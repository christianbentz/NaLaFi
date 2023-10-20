# NaLaFi
This repo contains data and code to work on Natural Language Fingerprints (NaLaFi), and to replicate the results in Bentz (2023). The code should be run in the following order:

Data Generation
- randomStringGenerator.Rmd: generates random strings for comparison to natural languages and other sign strings.
- shuffledTextGenerator.Rmd: takes the files in folder NaLaFi/data/writing and shuffles the characters randomly.

Simple Stats for the Data
- simpleStats.Rmd: this gives an overview of the files in NaLaFi/data in terms of number of files per subcorpus and number of characters per file.

Sampling of Character Strings
- sampler.Rmd: samples chunks of UTF-8 characters of pre-defined length (e.g. 10, 100, 1000) and stores them in NaLaFi/samples. Note that this folder should be emptied before re-running the code.

Estimations of Feature Values
- estimations.Rmd: calculating the feature values (TTR, unigram entropy, entropy rate, repetition measure) for each string of UTF-8 characters (one per line) in the files of NaLaFi/samples. The output is a csv file stored in NaLaFi/results/features.csv. Note that this file should be deleted before re-running the code.
- estimationPlots.Rmd: provides plots for the estimated feature values.
- stabilizationAnalyses.Rmd: estimates feature values for stepsizes (i.e. given number of characters), and creates plots of ``stabilization'', i.e. how feature values change with the number of characters. 

Classification
- classificationKnn.Rmd: classifies the character strings into "writing" and "non-writing" based on the feature values (TTR, unigram entropy, entropy rate, repetition rate) with the k-nearest neighbor method, and stores the results in results/KNN.
- classificationLR.Rmd: classifies the character strings with logistic regression model (LR), and stores the results in results/LR. 
- classificationSVM.Rmd: classifies the character strings with a support vector machine (SVM), and stores the results in results/SVM. 
- classificationMLP.Rmd: classifies the character strings with different Multilayer Perceptron (MLP) architectures, and stores the results in results/MLP.

Hyperparameters:
- HyperParamTuning.Rmd: gives diagnostic plots for hyperparameter values and model performance.

Reference

Bentz (2023). The Zipfian Challenge: Learning the statistical fingerprint of natural languages. CoNLL, Singapore.
