# Event Driven Surge Pricing
Building a predictive framework that can forecast ride-hailing surge probabilities 1–2 hours in advance using event metadata, temporal signals, and historical trip activity.

## Problem Statement

Major events (sports games, concerts, parades) in NYC trigger sudden, highly localized spikes in ride-hailing demand.

These spikes often cause:
- Extended passenger wait times,
- Driver shortages, and
- Price surges that frustrate customers and harm brand reputation.

Currently, surge detection is reactive (after the event ends).
We aim to build a predictive framework that can forecast ride-hailing surge probabilities 1–2 hours in advance using event metadata, temporal signals, and historical trip activity.

## Business Objectives

1. Predict Surge Events: Estimate the probability and intensity of a surge in each zone near an event venue for a specific time window
    a. Estimate attendance
    b. Estimate number of taxi availability
2. Quantify Latent Demand: Estimate the Gap between trip requests and available drivers 
    a. Weather can be a multiplier factor to increase the demand estimation. If its raining after an event demand may be higher than if its not raining after an event
3. Recommend Pre-deployment zone: Identify when and where extra driver incentives or positioning could minimize wait times
    b. There could be multiple events happening  - how do you rank or split the drivers that are recommended to go there
4. Evaluate Revenue Impact: Estimate lost or excess revenue due to under or over supply

## Machine Learning Models Applied
1. Base Model - Class weighted Gradient Boosting Trees Classifer
2. Advanced Model - Spark MultiLayer Perceptron Classifier