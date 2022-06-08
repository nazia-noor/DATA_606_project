![picture1](https://user-images.githubusercontent.com/78176162/172498990-12a62a81-349a-46b5-9818-759a0c6f7edf.jpg)


# Capstone Project

### A Predictive Model Analysis to Identify Human Activity Using Sensor Data


**Name:** Nazia Noor

**Course:** DATA606

**Instructor:** Dr. Chaojie (Jay) Wang

### **Keywords:** *Predictive Analysis, Machine Learning Model, Deep Learning Model, Human Activity Recognition(HAR), Sensor Data*




# Introduction
Scientific breakthroughs have made our lives easier. Image detection, computer vision, pose estimation, etc. are some ground-breaking technologies that have resulted in the recognition of human behavior. 

The method of analyzing human posture using computer and machine vision technology is known as human activity recognition or HAR. Human activities, gestures, or behaviors can be captured by a sensor. The movement data is subsequently converted into action commands, which are then executed and analyzed by computers.[1]
Human Activity Recognition (HAR) has been a difficult topic. With years of research, it started serving as a technology for health monitoring and management.

Although its full potential has yet to be realized, it has already proven effective in a variety of disciplines.
But with this technology, we can serve so many important purposes such as understanding human behavior and developing human-centric innovations.

Because of its usefulness and versatility, human activity recognition has acquired a lot of popularity. Several studies have found that trustworthy posture detection can provide service in healthcare settings. It can assist in better tracking and monitoring patients in hospitals, elder people, and disabled people as assistive technology. It can be integrated with the Internet of Things(IoT) to facilitate the service.

# Importance & Motivation
The current global population of people aged 65 and up is estimated to be around 750 million. T is e figure is predicted to more than double, reaching 1.5 billion seniors by 2050. As a result, the global share of elderly people is expected to rise from 10% to 16%, implying that one out of every six individuals in the globe will be 65 or older.[2]Approximately 650 million individuals or about 10% of the world's population are disabled people.[3]Around 24.8 million children are between the ages of zero to five.[4]

This large group needs extra attention and assistance. Pose estimation promotes automation. Pose estimation tracks human activity, which aids in both prediction and analysis of human behavior, unlocking hidden benefits and removing human labor.

Activity recognition can detect unexpected events. It can also serve as guidance for people's actions to avoid risky behavior for the elder, children, and disabled people who need extra attention and assistance.

Thanks to HAR technology, it will determine the gesture that is unusual from the regular motions or movements. This way it will be able to detect motions such as someone falling from a bed, chair, or wheelchair through its intellectual assistance
Also. HAR can provide the information if someone is getting a heart attack. During a heart attack, people feel restless, so their body movement gets unusual, a hand can be detected on the chest and neck area for a long time, nausea or vomiting, and dizziness will make your body less balanced. 

![picture2](https://user-images.githubusercontent.com/78176162/172498994-41d7b25f-415f-4994-aa6e-d6279f849c6c.jpg)

# Objectives
Since human activity recognition can open door to so many automation services which include life-saving services, I want to predict human activity. 
Human activity can be predicted from sensor data from cellphones and watches, videos, images, etc.

For this project, I will use smartphone sensor data will be analyzed to identify human activities.

Smartphones are widely used devices and can track a person's liveliness. Sensors such as the gyroscope and accelerometer in the smartphone can be used to examine human action, and it is used to assess detecting human environmental changes
raw data from smartphones' sensors will be analyzed by machine learning approaches followed by deep learning approaches to observe the human activity. Using sensor information, machine learning and deep learning algorithms are presented to recognize human motions with reasonable high accuracy.

**Problem statement:** ***The model can predict the particular Human Activity accurately at a given a datapoint***

The objective of this project is to create both machine learning and deep learning model that can predict human actions precisely. The selected dataset has a set of Human Activity Recognition data that includes "Walking," "Walking Upstairs," "Walking Downstairs," "Standing," "Sitting," and "Lying” of a group of participants. In the first part, I plan to employ a pre-engineered dataset to learn from the data and anticipate human activity using machine learning (ML) algorithms. In the second part, I wish to utilize the RAW dataset in conjunction with a deep learning model to learn from the data and forecast human activity.

**EDA question:**

*1. What are participants' activity durations?*

*2. How many numbers of observations per human activity class are in the dataset?*

*3. Can static and dynamic activities of Humans be determined separately?*

*4. Which participant has provided the most and least data points?*

*5. How can the human activity from different data points be interpreted ?*

*6. How do the data points for each activity spread out?*


# Data Source
The dataset has been collected from the Center for Machine Learning and Intelligent Systems at the University of California, Irvine which is commonly known as the UCI machine learning repository. This is a very well-known and recognized primary data source of machine learning data sets for data enthusiastic students, educators, and researchers.

[Click](https://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) for the dataset link

# Data Description
This dataset was collected from the recordings of a group of 30 participants between the age of 19-48 years performing activities of daily living (ADL). They carried a waist-mounted (Samsung Galaxy S II) smartphone with embedded inertial sensors. They performed a protocol of activities composed of six basic activities: three static postures (standing, sitting, lying) and three dynamic activities (walking, walking downstairs, and walking upstairs). The data is recorded with the help of sensors (accelerometer and Gyroscope) in that smartphone. This experiment was video recorded to label the data manually. The dataset consists of data of  3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz using the embedded accelerometer and gyroscope of the device. The obtained dataset was randomly partitioned into two sets, where 70% of the volunteers were selected for generating the training data and 30% for the test data. 

**Dataset characteristic:** *Multivariant, Time series data*

**Number of instances:** *10299*

**Number of attributes:** *561* 

**Dataset size:** *The data is provided as a single zip file that is about 58 megabytes. After unzipping, the test dataset is 77 megabytes and the Train dataset is 269 megabytes*

Since this is a time-series dataset, the entire data is a better representation of the entire series and helps with accurate predictions. Also, every 3-axial linear acceleration and 3-axial angular velocity data is required for prediction. Among the whole dataset, I will drop 1-2 columns that are not required for prediction like “Activity”(code number for activity), and “Subject”(participant number).

# ML and DL Approaches
Human activity recognition is a challenging time series classification or multiclass classification problem. It involves predicting the movement of a person based on sensor data and traditionally involves deep domain expertise and methods from signal processing to correctly engineering features from the raw data to fit a machine learning model. we have to predict the Human Activity for given a datapoint which corresponds to one of the 6 Activities. 
Since I will try to predict the HAR with the most accuracy, I will perform both machine learning and deep learning approaches.

For the machine learning model, I plan to perform Logistic Regression, Linear SVC, SVM Tree, Decision tree, K-Nearest Neighbor, and Random Forest Classifier and find out which one gives the most accuracy.

For the deep learning approach, I plan to execute LSTM based model playing with different layers and hyperparameter tuning.

**Model development steps**
- Since there are a lot of variables, the model might be overfitting. Having redundancy in the data, which makes the model too complex for the given training data and unable to generalize well on unseen data. So, I will check if there is redundancy and if needed, I will reduce the number of features of the dataset via Principal Component Analysis to avoid overfitting.

- The dataset is already divided into train and test datasets, hence data splitting is not required. The training of the models will be done with training data and tested on test data.

- For the learning process, I will play with several algorithms. 

- I will also do cross-validation since it is one of the common ways to find a good model.

- Tuning hyperparameters is one of the best ways to obtain the best predictive power possible. The most common way to find the best combination of hyperparameters is called Grid Search Cross-Validation, so we will use this one.

- All the ML models are selected, trained, validated, and tested throughout the process. Trying multiple algorithms and comparing their performance is a frequent technique for building a successful model. I will calculate the accuracy score and compare the models’ performance. Since this is a classification problem, I will use evaluation metrics such as precision, accuracy, and recall.

# Use of Expected Outcome
The outcome I intend to get is to find a model with the best accuracy score which can recognize Human Activity more precisely. As I have previously mentioned the importance and the benefit we can get from HAR technology like monitoring elder, and disabled people, identifying heart attack symptoms, and predicting the human activity with the highest precision is required. 

The dataset has a column that has the activity labels. These activity labels were done manually from a video recording. This is a lengthy and tedious manual job. That is why the dataset has only 30 participants’ information. If our model can predict human activity more accurately, we can automate the process. We further do not need to manually set our activity label and the activity can be predicted with the sensor data only for further analysis where a large amount of data is required.



# References:

1. https://indatalabs.com/blog/human-activity-recognition

2. https://www.globalissues.org/news/2022/01/05/29746#:~:text=As%20a%20result%2C%20the%20world%E2%80%99s%20proportion%20of%20older,in%20the%20age%20group%2065%20years%20and%20older.

3. https://www.disabled-world.com/disability/statistics/

4. https://www.childstats.gov/AMERICASCHILDREN/tables/pop1.asp

5. **Dataset:** Jorge-L. Reyes-Ortiz, Luca Oneto, Albert SamÃ , Xavier Parra, Davide Anguita. Transition-Aware Human Activity Recognition Using Smartphones. Neurocomputing. Springer 2015.






