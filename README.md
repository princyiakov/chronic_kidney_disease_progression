# Chroninc Kidney Disease Progression 
Chronic kidney disease (CKD) is a condition in which your kidneys gradually lose their ability to help your body remove
waste and fluid from your blood. When this happens, harmful wastes and fluids begin to build up in your body, making
you feel unwell and out of balance. Although chronic kidney disease (CKD) is not curable, treatment can help slow its 
progression, control symptoms and enable you to live a full life.

<!-- toc -->
- [Our Goal](#our-goal)
- [Notebook File](#notebook-file)
- [Patient Demographics](#patient_demographics)
  - [Gender](#gender)
  - [Age](#age)
- [How Were We Able To Predict The Progression](#how-were-we-able-to-predict-the-progression)
  - [Approach I Machine Learning ](#approach-i-machine-learning)
    - [Data Cleaning](#data-cleaning)
    - [Handling Imbalanced Data](#handling-imbalanced-data)
    - [Feature Engineering](#feature-engineering)
    - [Feature Selection](#feature-selection)
    - [Model Selection](#model-selection)
  - [Approach II Survival Analysis ](#approach-ii-survival-analysis)
    
- [Evaluation](#evaluation)
  - [Giskard](#giskard)
<!-- tocstop -->

## Our Goal
Using Patiesnt past records we will predict whether a patient will progress in CKD staging or not.

## Notebook File

Here is the link to our [notebook](https://github.com/princyiakov/chronic_kidney_disease_progression/blob/main/chronic_kidkey_disease_progression.ipynb)

## Patient Demographics
We will be understanding the patients demographics based on Gender, Race, Age, and Stage Progression

### Gender
<img alt="genderdistribution" src="https://raw.githubusercontent.com/princyiakov/chronic_kidney_disease_progression/main/images/gender.png">

### Age
<img alt="genderdistribution" src="https://raw.githubusercontent.com/princyiakov/chronic_kidney_disease_progression/main/images/age.png">
