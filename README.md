# Final Project

**Draft**  
**Due by:** Friday night of finals week  
**Late Policy:** 5 percent for the first day and 10 percent for each day afterwards  
Single person project for the basic version. If you have your own idea that aligns with the basic project, discuss it with the instructors beforehand.

## Report Format

Write a report with more than 1,000 words (excluding references). Include these sections:

- abstract
- introduction
- method
- experiment
- conclusion
- references

You may follow formats from leading ML journals or conferences such as:

- JMLR: http://www.jmlr.org/
- IEEE TPAMI: http://www.computer.org/web/tpami
- NeurIPS: https://papers.nips.cc/
- ICML: https://icml.cc/

There is no page limit.

### Templates

- NeurIPS: https://neurips.cc/Conferences/2023/PaperInformation/StyleFiles
- ICML: https://media.icml.cc/Conferences/ICML2023/Styles/icml2023.zip
- ICLR: https://github.com/ICLR/Master-Template/raw/master/iclr2024.zip

## Bonus Points

You may add a **Bonus Points** section if you believe your work deserves extra credit due to:

- novel ideas or applications
- substantial data collection or preparation
- state of the art classification results
- new algorithms

## Project Description

Choose **three classifiers** from those tested in Caruana and Niculescu-Mizil and evaluate them on **three datasets** from the UCI repository:  
http://archive.ics.uci.edu/ml/

Notes:

- Different kernels do not count as different classifiers.
- Read the Caruana and Niculescu-Mizil paper carefully.
- For each classifier, train and test it on at least three datasets (minimum 3 x 3 = 9 experiments).
- Use cross validation to select hyperparameters for each classifier.

The basic project focuses on **two class classification**. If your dataset has multiple classes, merge them into two groups (positive and negative). You may experiment with multiclass settings if you have time.

Train your classifiers following the empirical study setup in the paper. You only need one evaluation metric such as accuracy. Report cross validated results and learned hyperparameters.

Expect variations due to using different implementations or subsets of features. Trends should still be consistent such as:

- random forests perform well
- more training data improves results
- knn is not necessarily poor

### Expected Experiments

If computing accuracy with 3 classifiers and 3 datasets, you will run:

- 3 trials
- x 3 classifiers
- x 3 datasets
- x 3 partitions (20/80, 50/50, 80/20)

Report the best accuracy for each hyperparameter search.  
For grading, accuracy is averaged across trials. Report:

- 3 classifiers
- x 3 datasets
- x 3 partitions
- x 3 accuracies (train, validation, test)

Use training accuracy as a sanity check while debugging. Hyperparameter search heatmaps are not the focus.

You do not need to try every hyperparameter in the paper. Try a few reasonable ones.  
If using MLPs, you may need deeper or wider networks to get good results.

You may also use datasets and classifiers from Caruana et al., ICML 2008.

## Allowed Classifiers

You may use Python or any language. Options include:

1. Boosting family  
   http://www.mathworks.com/matlabcentral/fileexchange/21317-adaboost  
   https://github.com/dmlc/xgboost

2. Support vector machines  
   http://www.csie.ntu.edu.tw/~cjlin/libsvm/

3. Random forests  
   http://www.stat.berkeley.edu/~breiman/RandomForests/

4. Decision tree  
   http://www.rulequest.com/Personal/

5. K nearest neighbors  
   http://www.mathworks.com/matlabcentral/fileexchange/19345-efficient-k-nearest-neighbor-searchusing-jit

6. Neural networks  
   http://www.cs.colostate.edu/~anderson/code/  
   http://www.mathworks.com/products/neural-network/code-examples.html

7. Logistic regression

8. Bagging family

You may implement your own classifiers or use reliable online versions.  
Write a formal report that includes results and code.

## Grading

Meeting the minimum requirement (3 classifiers x 3 datasets with cross validation) earns a solid score but not full credit. Full credit requires deeper insight and effort.

### What to Compare

a. For each dataset and each partition, compare classifiers and show consistency with trends from the paper.  
b. For each classifier and each partition, compare performance across partitions with the expected pattern that more training data improves test accuracy.

Implementation differences may impact results, but trends should still be explainable.

## Evaluation Criteria

1. How challenging and large are the datasets? (10 points)
2. Novelty in algorithms, data, or applications? (10 points)
3. Experimental design rigor: hyperparameter tuning, cross validation, multiple partitions, repeated trials, training and testing errors, optional curves. (50 points)
4. Report quality with required sections. (30 points)
5. Bonus points for significant novelty or extensive empirical work (such as at least 5 classifiers and 4 datasets).
