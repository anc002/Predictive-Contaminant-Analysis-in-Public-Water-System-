# Public Water System Contamination Prediction

## Overview
This project focuses on developing a logistic regression model to predict the presence of various contaminants in public water systems. 
Our aim is to enhance the effectiveness of water safety measures and compliance with the Safe Drinking Water Act by leveraging data collected under the Fifth Unregulated Contaminant Monitoring Rule.
The contaminants are primarily PFAs or 'forever chemicals', for which the U.S. government has also allocated an additional $1 billion to states for public water testing specifically to look at the “cancer-causing chemicals” that occur in water.

## Problem Statement
Ensuring water quality in public water systems is a complex and resource-intensive task governed by stringent regulations such as the Safe Drinking Water Act. 
The Fifth Unregulated Contaminant Monitoring Rule requires testing for 30 chemical contaminants, a process that can be time-consuming and costly. 
Our project seeks to streamline this process using data science, potentially saving government time and resources.

## Dataset
The dataset is obtained from the Environmental Protection Agency and encompasses results from water quality tests conducted as per the guidelines of the Fifth Unregulated Contaminant Monitoring Rule. 
It includes various attributes related to water systems and the contaminants tested, with regular updates to reflect the latest findings.

## Methodology
- **Data Cleaning**: Implemented pandas data frames to structure the raw data, dropping irrelevant administrative IDs and creating a binary column to indicate contaminant detection.
- **Visualizations**: Used `plt.pyplot` library to visualize the frequency of contaminant detection by water source and to display the number of detections for the contaminants.
- **Logistic Regression**: Trained individual models for each contaminant to predict the presence above the MRL, using `LogisticRegression` from scikit-learn, addressing class imbalance with the 'balanced' class weight option.
- **Model Evaluation**: Employed confusion matrices and classification reports to evaluate model performance, focusing on metrics like precision, recall, and F1-scores.

## Results
Our models demonstrate the ability to predict contaminant presence with varying degrees of accuracy, challenged by significant class imbalances. Precision is consistently high for the majority class, but low for the minority class, indicating room for improvement, especially in reducing false positives.

## Future Work
- **Data Update**: A continued effort to update the model with new data to improve accuracy.
- **Budget Analysis**: Investigate the impact of EPA funding on the detection rate of contaminants to suggest optimal allocation of resources.
- **In-depth Financial Analysis**: Cross-analysis with budget breakdowns to optimize the use of government funds at a granular level.

## References
Occurrence Data from the Unregulated Contaminant Monitoring Rule: https://www.epa.gov/dwucmr/occurrence-data-unregulated-contaminant-monitoring-rule
US sets first standard to curb 'forever chemicals' from drinking water: https://www.reuters.com/world/us/us-sets-first-standard-curb-forever-chemicals-drinking-water-2024-04-10/

