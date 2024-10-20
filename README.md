# Classification-of-Arrhythmia-Based-on-ML-Algorithms
An arrhythmia is a condition characterized by irregularities in the heart's rate or rhythm, where the heart may beat too quickly, too slowly, or with an abnormal pattern. To diagnose arrhythmias, the most commonly used test is the electrocardiogram (ECG). The ECG captures electrical activity of the heart and displays key points, known as fiducial points, labeled P, Q, R, S, T, and U, along with segments and intervals. Variations in these points, segments, and intervals can indicate the presence of arrhythmia. Various types of arrhythmias can be detected through ECG signals. Machine learning techniques are often employed to analyze these patterns, helping to identify the specific type of arrhythmia a patient may have.
<p align="center">
<img src="https://github.com/Atshayasankaran/Classification-of-Arrhythmia-Based-on-ML-Algorithms/blob/main/Img/ECG signal_1.JPG" width="400" height="400">
</p>

# Model Architecture
<p align="center">
<img src="https://github.com/Atshayasankaran/Classification-of-Arrhythmia-Based-on-ML-Algorithms/blob/main/Img/Model.png">
</p>

# Dataset
The MIT-BIH Arrhythmia Dataset is used in this project. It containing both training and testing data. In total, there are 109446 instances across the dataset, which are categorized into five classes: 'N': 0, 'S': 1, 'V': 2, 'F': 3, and 'Q': 4. Class 'N' represents normal or non-ectopic beats, 'V' refers to ventricular ectopic beats (VEB), 'S' represents supraventricular ectopic beats (SVE), 'Q' indicates unknown beats, and 'F' represents fusion beats.

<p align="center">
<img src="https://github.com/Atshayasankaran/Classification-of-Arrhythmia-Based-on-ML-Algorithms/blob/main/Img/training.JPG" class="center">

<img src="https://github.com/Atshayasankaran/Classification-of-Arrhythmia-Based-on-ML-Algorithms/blob/main/Img/testing.JPG" class="center">
</p>

<h3 align="center">ECG signal for different classes<h3>
<p align="center">
<img src="https://github.com/Atshayasankaran/Classification-of-Arrhythmia-Based-on-ML-Algorithms/blob/main/Img/Signals.png">
</p>

# Preprocessing 
The samples are not equally distributed across the target labels. To make the dataset balanced two techniques were used, upsampling and downsampling. 

Upsampling :
<ul>
  <li>Process of duplicating the randomly selected samples in each class which has the minimum instances.</li>
  <li>After upsampling there are 35000 instances in training dataset and 15000 instances testing dataset in each target classes.</li>
</ul>
Downsampling :
<ul>
  <li>Process of reducing the samples in the classes which has the maximum number of samples.</li>	
  <li>After downsampling there are 370 instances in training dataset and 160 instances testing dataset in each target classes.</li>
</ul>

# Machine Learning and Ensemble Models
Both upsampled and downsampled data are used as input for various machine learning algorithms, including k-Nearest Neighbor, Naive Bayes, Decision Tree, and Support Vector Machine (SVM) with different kernels, such as Polynomial, Gaussian Radial Basis Function (RBF), and Sigmoid kernels. Since the upsampled data gives better accuracy, it is given as input for ensemble models like Adaptive Boosting, Gradient Boosting, XGBoost, Bagging Classifier, Random Forest, and ExtraTrees Classifier.

# Results
<ul>
<li>Among all the machine learning and ensemble techniques applied, the Radial Basis Function (RBF) kernel in SVM achieves the highest accuracy of 91% on upsampled data.</li>
<li>For normal beats, Random Forest performs the best, with a sensitivity of 99%.</li>
<li>For supraventricular ectopic beats, the RBF kernel in SVM delivers the best result, with a sensitivity of 82%.</li>
<li>For Ventricular ectopic beats, KNN algorithm works well with sensitivity of 94%.</li> 
<li>For fusion beats, the RBF kernel performs the best, with a sensitivity of 93%.</li>
<li>For unknown beats, XGBoost gives best performance with the sensitivity of 97%.</li> 
</ul>



