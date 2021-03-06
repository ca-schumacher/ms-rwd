# ms-rwd
Data science project using real world data on multiple sclerosis


# Investigating real world data on multiple sclerosis

Data analysis of real world data on multiple sclerosis.
The data can be found here: https://www.floodlightopen.com/en-US/for-scientists .

**January 2020**

## Introduction

**Project Description:**

In this project, I explore the mentioned real world dataset to analyse symptoms of multiple sclerosis:
* Which of the collected metrics show differences between people with multiple sclerosis and controls?
* Does the mood (or self-reported well-being) correlate with some of the gathered metrics?

Further research questions are:
* Is it possible to classify, if a particular result was generated by diagnosed or control group?
* Which modelling approach works best for this classification problem?
* Which metric is most important to predict the participant group?
* Can we use the dataset to monitor and track symptomatic progresses?

**Data Description:** 

The data is published by the Floodlight Open project (https://www.floodlightopen.com/en-US/) by Genentech. It can be downloaded through https://www.floodlightopen.com/en-US/for-scientists . The data is collected through a smartphone app that provides questionnaires and collects sensor data when the user performs certain tasks.
According to the project website, data of the following tests was collected:
* **Mood:** A quick daily question about how you feel
* **Matching Symbols:** Matching symbols to digits measures how quickly you process information 
* **Squeeze a Tomato:** This task is designed to measure changes in hand-eye coordination and fine motor skills.
* **Draw a Shape:** Drawing a shape measures the speed and accuracy of hand and finger movements
* **U-Turn:** This task measures how you walk and your ability to change direction
* **2 Min Walk:** Walking quickly for 2 minutes measures your stamina and mobility
* **Balance:** Standing still for 30 seconds measures posture and stability
* **Passive Monitoring:** Gathering information on activity to understand how your health affects your life

However, after inspecting the data, I concluded that instead the following metrics are reported (explanations are taken from: https://medically.roche.com/content/dam/pdmahub/non-restricted/neurology/aan-2018/AAN%202018%20FLOODLIGHT%20Poster_Global_Montalban%20et%20al.pdf):

* **Mood:** A quick question about how you feel (scale 1 to 5).
* **Cognition:** Symbol Digit Modalities Test that evaluates the number of correct responses.
* **Hand & Arm:** (1) In the **_Pinching Test_**, subjects are asked to "pinch as many tomatoes as possible in 30 seconds". The time between two consecutive pinches is evaluated. (2) In the **_Draw a Shape Test_**, subjects are asked to draw six prewritten alternating shapes of increasing complexity (linear, rectangular, circular, figure 8-shape and spiral) on the touchscreen of the mobile device with the second finger of the tested hand; as fast and as accurately as possible within 30 seconds, and passing through all indicated waypoints. The overall mean celerity (derived from the accuracy to connect all waypoints relative to the time to complete the test) is evaluated
* **Gait & Posture:** (1) In the **_Static Balance Test_**, subjects are asked to stand still for 30 seconds. The sway, as the total length of accelerometer trajectory, is evaluated. (2) In the **_Five U-Turn Test_**, subjects are asked to perform U-turns while walking a short distance at a comfortable pace. The U-Turns are evaluated by a turn detection algorithm that calculates the average turn speed (rad/ second). (3) In the **_Two-Minute Walk Test_**, subjects are asked to walk for two minutes. The Step power, the integral of variance in accelerometer radius for step spans using a setp detection algorithm, was avaluated. 

For a more detailed overview of the tests, see https://www.jmir.org/2019/8/e14863/pdf.

## Approach
After cleaning and feature engineering of the dataset, I trained different classification models on the data (Logistic Regression, k-Nearest Neighbors, Naive Bayes, Random Forest). To evaluate the performance of these models, the ROC curve (receiver operating characteristic curve), which assesses the rate of True Positive and False Positive classifications, was used. I performed cross-validation to further check if the obtained results were robust or if the applied models overfitted. 

## EDA & Modelling
To access the explorative data analysis (EDA) open the Notebook: https://github.com/ca-schumacher/ms-rwd/blob/master/EDA.ipynb.  
To see the implementation of the models and classification results open this notebook: https://github.com/ca-schumacher/ms-rwd/blob/master/Classification_model.ipynb.

## Results and Conclusions
in the dataset, people with a MS diagnosis are generelly older, smaller and with similar weight. Additionally, participants with MS responded with lower mood than controls. Appart from that, no clear difference could be found. However, the mood of the particpants did not correlate to any of the test metrics. Also, I could not find correlations between test results. 
From all classification models (Logistic Regression, k-Nearest Neighbors, Naive Bayes, Random Forest), Random Forest was the best-performing model to classify, if a particular test result was generated by diagnosed or controls. Still, from all predictions (n = 50195), the best model created 3563 false negative (actual MS were predicted as controls) and 473 false positive predictions (actual controls were predicted as MS). These results can be improved in future models, if e.g. subject-specific progresses (over time should) are included in the model, e.g. by feature engineering. 

