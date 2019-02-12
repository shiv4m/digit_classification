# digit_classification
Classify the handwritten numbers from MNIST and USPS data set. Use different algorithms and perform a majority voting. Also, support "No free lunch Algorithm".

#DATASET
The data is the famous MNIST data. It is a bunch of handwritten images of digits from 0 to 9. The goal is to successfully predict the handwritten digit. Additionally, there is one more data set which was developed at UB. The USPS dataset, also consists of handwritten images of digits from 0 to 9. The plan of work is that, there are 4 different algorithms to be implemented and trained using the MNIST training data and tested on both MNIST and USPS dataset to see how it performs. Algorithms to be implemented are –  a. Logistic Regression b. Neural Network c. Support Vector Machine (SVM) d. Random Forest

#Why the accuracy on USPS data is low?
The “No Free Lunch” theorem states that there is no model that works best for a specific problem. For every other problem, one needs to find what model works best for it, especially for supervised problems where predictions, accuracy, loss are important factors.  
 
In this case, we train all the models using the MNIST data set and then test on both MNIST and USPS data. This resulted in high accuracy for MNIST data and low accuracy on USPS data. This holds true for the No free lunch theorem that why one model for a specific problem does not works for another problem even though they are of same type.  
 
#Classifier with best performance
For this problem, based on the observations of confusion matrix, the best classifier seems to be is the Neural Network and Random forest. Bothe classifiers are almost capable of achieving a perfect accuracy with very less number of miss classifications. The worst accuracy was achieved by SVM with the configuration of ‘rbf’ kernel and gamma=1 which essentially lead to overfitting of data due to high value of gamma. 

#Majority Voting
Majority Voting is an ensemble technique which is used to compare the performance of multiple classifiers. Infact, Random Forest is a type of ensemble model. For a majority voting task, we compare the predicted outputs of all the classifiers and select the label with most number of occurrences. This is called as hard voting. For a soft voting, we use probability to do the same.  I have implemented a hard voting method where the outputs from all the classifiers are compared and then one with highest number of votes is selected. If the votes are equal for two labels, then either of them are selected.  We then compare the selected labels from all the classifiers and calculate its accuracy which turns out to be pretty good and better than half of the classifiers.
