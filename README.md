# ms-rwd
Data science project using real world data on multiple sclerosis


# Investigating real world data on multiple sclerosis

Data analysis of real world data on multiple sclerosis.
The data can be found here: https://www.floodlightopen.com/en-US/for-scientists .

**January 2020**

## Introduction

**Project Description:**

I will explore this real world dataset to analyse and predict symptoms of multiple sclerosis:
* Which of the collected metrics show differences between people with multiple sclerosis and controls?
* Can we use the dataset to monitor and track symptomatic progresses?
* Does the mood (or self-reported well-being) correlate with some of the gathered metrics?

**Data Description:** 

The data is published by the Floodlight Open project (https://www.floodlightopen.com/en-US/) by Genentech. It can be downloaded through https://www.floodlightopen.com/en-US/for-scientists . The data is collected by a smartphone app that provides questionnaires and collects sensor data when the user performs certain tasks.
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

## Approach


## Modelling


## Results and Conclusions


