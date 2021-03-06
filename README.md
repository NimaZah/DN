<h1 style="color:blue;">Diagnosis Alzheimer With handwriting Dataset</h1>



The 'Diagnosis Alzheimer With Handwriting' dataset is a unique collection of handwriting samples from patients with Alzheimer's disease and a control group. The data was collected from 174 individuals while performing handwriting activities according to a technique designed for the early identification of Alzheimer's disease. The dataset contains elements that aid in identifying Alzheimer's disease by capturing the unique aspects of handwriting.
The use of graphics tablets for administering handwriting tests has shown promise in decreasing the time taken to perform clinical assessments, and machine learning methods can be used to record the kinematic and dynamic information of performed movements. To this end, the data was collected from 37 patients with Parkinson's disease and 38 healthy people using a tablet with a white template and a traditional ink pen. They took handwriting samples from 174 people, including 89 Alzheimer's sufferers and 85 healthy people, and examined their abilities in the categories of graphic tasks, copy tasks, memory tasks, and dedications tasks.

## The objective

The goal of the my model building in this experiement is to demonstrate that handwriting analysis provides a novel approach of describing the symptoms of Alzheimer's disease.

## Experiment with algorithms

I performed experiments with decision tree, tandom forest, Multi-layer Perceptron, Support Vector Machine, KNN, and Gaussian Naive Bayes to validate a feature set that can discriminate between AD patients and healthy people. The results of the experiment show that nearly all the classifiers performed well (77.51%), and the variance of 1.16%.

## Report on model building and accuracy test

I initially used the default parameters for the Decision Tree Classifier to estimate the model accuracy (which resulted in 0.77.) I then used GridSearchCV to tune the hyperparameters of the model. The accuracy of the tuned model was 0.83. Among the ensemble methods, I used the Bagging classifier and AdaBoost. The Bagging Classifier performed better than AdaBoost (0.86 v.s 0.77) Afterwards, the Random Forest classifier was used with RandomizedSearchCV to tune the hyperparameters. The achieved accuracy was 0.87. KNN was also used with GridSearchCV to tune the hyperparameters with an accuracy of 0.86. I applied the nonparametric method of the K-Nearest Neighbor and performed an exhaustive search. The metric, 'manhattan,' and weight, 'distance,' were the best parameters. The accuracy of the model was 0.73. The Gaussian Naive Bayes with 1e-06 as the smoothing parameter showed promise with an accuracy of 0.85. The Multi-layer Perceptron Classifier was another model that I employed (accuracy 0.86.) The best parameters were hidden_layer_sizes = (100, ), activation = 'logistic', solver = 'lbfgs', and 'alpha': 0.05. Finally, the Support Vector Machine was used with GridSearchCV for hyperparameters tuning. The algorithm performed poorly compared to all other models with an accuracy of 0.51. I eventually used the Voting Classifier to combine the results with the best models, and arrived at an accuracy of 94.29%.
