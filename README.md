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
  - [Stage Progression](#stage-progression)
- [How Were We Able To Predict The Progression](#how-were-we-able-to-predict-the-progression)
  - [Approach I Machine Learning ](#approach-i-machine-learning)
    - [Feature Engineering](#feature-engineering)
    - [Feature Selection](#feature-selection)
    - [Handling Imbalanced Data](#handling-imbalanced-data)
    - [Model Selection](#model-selection)
  - [Approach II Survival Analysis ](#approach-ii-survival-analysis)
    
- [Evaluation](#evaluation)
  - [Giskard](#giskard)
<!-- tocstop -->

## Our Goal
Using Patient past records we will predict whether a patient will progress in CKD staging or not.

## Notebook File

Here is the link to our [notebook](https://github.com/princyiakov/chronic_kidney_disease_progression/blob/main/chronic_kidkey_disease_progression.ipynb)

## Patient Demographics
We will be understanding the patients demographics based on Gender, Age, Race and Stage Progression

### Gender
<img alt="genderdistribution" src="https://raw.githubusercontent.com/princyiakov/chronic_kidney_disease_progression/main/images/gender.png">

### Age
<img alt="agedistribution" src="https://raw.githubusercontent.com/princyiakov/chronic_kidney_disease_progression/main/images/age.png">

### Race
<img alt="racedistribution" src="https://raw.githubusercontent.com/princyiakov/chronic_kidney_disease_progression/main/images/race.png">

### Stage Progression
#### Overall Stage Progression
<img alt="stageprogression" src="https://raw.githubusercontent.com/princyiakov/chronic_kidney_disease_progression/main/images/stageprogress.png">

#### Stage Progression According To Gender
<img alt="stageprogressiongender" src="https://raw.githubusercontent.com/princyiakov/chronic_kidney_disease_progression/main/images/stageprogressgender.png">

#### Stage Progression According To Race
<img alt="stageprogressionrace" src="https://raw.githubusercontent.com/princyiakov/chronic_kidney_disease_progression/main/images/stageprogressrace.png">

## How Were We Able To Predict The Progression
### Approach I Machine Learning
Since I was trying Survival Analysis first time since college, I wanted to first check how the data reacts with the 
machine learning and explored various models.

### Feature Engineering
- For blood works and blood pressure: 
  - For blood works like glucose, creatine, systolic and diastolic blood pressure, I took mean value of the observations and calculated the duration based on first and last day of observation
- For medicines:
  - I grouped the patient ids and medicines and calculated the total dose by multiplying each mdeicines doses and their start and stop date difference and provided a summation of the doses based on each medicine 