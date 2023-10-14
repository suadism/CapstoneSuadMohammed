# Introduction

The triage of incoming Emergency Room Patients has always been challenging due to resource constraints and inefficient allocation of resources. When a patient arrives at the ER a rapid assessment of the severity of their condition is conducted and a severity score is assigned to them which determines how long they need to wait to receive medical attention. The score ranges from 1 (most critical) to 5 (least critical). However due to resource constraints and differences in how different healthcare personnel assign severity scores, over triage occurs. Over triage is the overestimation of the severity of non-critically ill patients which diverts resources from critically ill patients leading to over-crowding and delayed care. The purpose of this project is to develop a model that assigns a triage score to a patient using patient data in order to speed up triage time and act as a tool to allow healthcare personnel to make better decisions


# Impact 
This tool will help with the burden on the emergency departments and increase efficiency of resource
management. A faster triage process using the expertise of health care professionals and the assistance of a
machine learning tool that classifies patients into categories will improve patient flow in the ER. Low risk patients
will be directed to facilities outside the ER and the bulk of the resources in ER will be focused on patients who are
very sick.


# Data Science Solution
The objective is to develop a model that assists healthcare personnel with triaging incoming ER patients to reduce
the time spent on triaging and better equip healthcare professionals in making decisions. The tool will classify incoming patients and assign them a triage score based on inputs such as the patients’ vital signs and symptoms within seconds. The tool will be developed using a machine learning algorithm that analyzes historical patient data and identifies patterns in the data and then applies the pattern to new data.

# Data Set 
A dataset that will be used to develop the model contains ER data of over 1200 patients from two emergency
departments in Korea between October 2016 and September 2017. The dataset is sourced from Kaggle and includes the patients’ age, sex, symptoms, vitals, complaint and the triage score (between 1 and 5) that was assigned by healthcare professional upon initial patient assessment. The goal is to use the patient vital signs, chief complaint etc as the independent variables to predict the dependent variable which is the triage score. The dataset contains a mixture of numerical data (Blood Pressure, Heart rate etc) and categorical data (chief complaint, Gender, Injury Status etc) with some columns containing numerical coding (for e.g Pain column contains either ‘1’ which stands for pain or ‘2’ which stands for no pain). The data dictionary is as below
| Group                    | Hospital where records were collected                                                                                                                  |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
|                          | 1: Local ED , 2: Regional ED                                                                                                                           |
| Sex                      | Gender of patient 1: Female / 2: Male                                                                                                                  |
| Age                      | Age (Years)                                                                                                                                            |
| Patients number per hour | Incoming Patients number/hours when triage conducted                                                                                                   |
| Chief Complaint          | Main patient complaint                                                                                                                                 |
| Arrival mode             | How patient arrived                                                                                                                                    |
|                          | 1: Walking / 2: 119 use / 3: Private car / 4: Private ambulance / 5: Public transportation (Police etc) /6: Wheelchair / 7: Others                     |
| Injury                   | 1: Non-injury / 2: Injury                                                                                                                              |
| Mental                   | Mental status of patient                                                                                                                               |
|                          | 1: Alert / 2: Verval response / 3: Pain response / 4: Unconciousness                                                                                   |
| Pain                     | 1: Pain / 2: Non-pain                                                                                                                                  |
| NRS_pain                 | Numeric rating scales of pain                                                                                                                          |
| SBP                      | Systolic blood pressure                                                                                                                                |
| DBP                      | Diastolic blood pressure                                                                                                                               |
| HR                       | Heart rate                                                                                                                                             |
| RR                       | Respiration rate                                                                                                                                       |
| BT                       | Body temperature                                                                                                                                       |
| Saturation               | Saturation to use pulse oxmeter                                                                                                                        |
| KTAS_RN                  | KTAS result of nuses in ED                                                                                                                             |
| Disposition              | Disposition of patient                                                                                                                                 |
| Diagnosis in ED          | Diagnosis in ED                                                                                                                                        |
| KTAS_expert              | KTAS result of experts                                                                                                                                 |
| Error_group              | 1: Vital sign / 2: Physical exam / 3: Psychatric /4: Pain / 5: Mental / 6: Underlying disease / 7: Medical records of other ED / 8: On set / 9: Others |
| Length of stay_min       | Length of stay (minutes)                                                                                                                               |
| KTAS duration_min        | KTAS duration (minutes)                                                                                                                                |
| Mistriage                | 0: Correct / 1: Over triage / 2: Under triage                                                                                                          |


