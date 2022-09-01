# Classification-of-Accident-Narratives-for-Occupational-Injuries
: We have used injury surveillance data to help inform injury prevention efforts by identifying the most common causes of injury
Abstract
Through injury surveillance, different elements of an injury event can be captured. These elements can help decision makers prioritize the major causes of concern and work on them accordingly. Injury surveillance usually involves capturing different aspects of an injury event through injury codes based on accident narratives which is usually done by humans. Previous studies have explored the use of different machine learning (ML) models to assign these codes to accident narratives. Taking inspiration from this, this study aims to classify accident narratives into different meaningful classes and examine the effectiveness of these ML models for the classification. Based on pervious similar studies, three different ML models were used: Logistic Regression, Support Vector Machine, and Long-Short-Term-Memory based Recurrent-Neural-Network. These approaches were evaluated for a dataset extracted from the website of Occupational Safety and Health Administration (OSHA) which was manually grouped after extraction. These models showed good results for binary classification but weren’t satisfactory for multiclass classification due to severely imbalanced data. 

Introduction

Workplace safety is an integral part of the working of any industry. And despite the continuous efforts to reduce workplace injuries, the nature of certain workplaces requires constant monitoring and if any element poses danger to any worker or machine, it needs to be taken care of immediately. Health, Safety, and Environment (HSE) is a discipline centred on implementing practices for environmental protection and worker safety in a workplace. However, for large enterprises, monitoring and managing HSE is a major challenge. 

Injury surveillance data is often utilised to help inform injury prevention efforts by identifying the most common causes of injury. Usually, such information is collected from accident narratives in an unstructured form. Injury codes like E-code, Major-Injury-Factor (MIF) and Intent are assigned depending on different elements of the narrative which is manually coded by triage nurses or doctors. However, manual coding is time consuming and subject to accuracy and consistency issues as the background of the coder, experience level and complexity of the incident can cause substantial variation. Previous studies have experimented with developing Machine Learning (ML) models trained on coded accident narratives to assign these injury codes and automate the process.

Injury codes fail to be of use for injuries occurring in hazardous as majority of cases will be limited to just a few codes. Moreover, the end goal of classifying injury reports in relation to workplace differs from the general injury codes. An organization may be interested in identifying the most hazardous elements that poses immediate danger and help the decision makers prioritize or to identify the most commonly cause of injuries to the workers. 
This study aims to classify accident narratives by use of various state-of-the-art ML models and examine their performance.

The report is organized as follows. The Literature Review section discusses the findings from previous studies that have used different ML models for predicting injury codes. In the Dataset section, challenges associated with collecting and processing data is described. The Methodology section discusses different methodologies used for this study. The performance of difference ML models are evaluated for different classifications in the Results section. The Conclusion section presents our findings and discusses the future scope of the project.

Dataset

Previous studies have used injury datasets from several sources to examine the performance of ML models. Data collected in hospital emergency departments (Queensland Injury Surveillance Unit, n.d.), workplace injuries reported by organizations – Survey of Occupational Injuries and Illnesses (SOII) (“Occupational Safety and Health Statistics Program”, 2014) and injury surveys conducted by the US government – National Health Interview Survey (NHIS). Developed by the World Health Organization (WHO) for classifying mortality and morbidity data worldwide, one of the most accepted injury coding schemes is the International Classification of Diseases (ICD).

In this study, injury surveillance data consisting of 4847 injury cases collected between 2015 and 2017 from the website of Occupational Safety and Health Administration (OSHA) were used. The dataset consisted of various fields of which, the narrative field which contained the injury description was used to classify into several groups.

Due to unavailability of labelled datasets, the OSHA data was manually coded into different classes that can help understand the narrative without having to read the complete accident narrative. The different classes are: 
a.	Degree of Injury
b.	Frequency of Task Assigned 
c.	Nature of Injury 
d.	Environmental Factor
e.	Human Factor
f.	Part of Body affected
g.	Event Type

Among these classes, for the purpose of this study, three classes were considered – Degree of Injury, Frequency of Task Assigned and Nature of Injury. The Degree-of-Injury class indicates the fatality of the accident narrative. This is a binary class with two values: ‘Fatal’ and ‘Non-Fatal’. The narratives which resulted in a fatality will be given the utmost priority to address the issue that may be an immediate cause of concern, neglecting which may lead to further loss of life. The Frequency-of-Task-Assigned is a binary class which indicates the regularity of the work which the worker was indulged in. The two values in this class are: ‘Regularly Assigned’ and ‘Not Regularly Assigned’. The events which are regular will be given preference as the possibility of that event recurring is higher due to which another person can be affected. Nature-of-Injury is a multiclass with 19 values which can be assigned to a certain injury narrative. The labels are: Amputation/Crushing, Dislocation, Fire Burn, Serious Fall/Strike, Bruising/Contusion, Fracture/Broken Bones, Head Trauma, Heat Exhaustion, Laceration, Electrocution, Asphyxiation/Drowning, Chemical Burn, Puncture, Fall/Strike, Eye Injury, Freezer burn, Poison, Fall from Elevation, and Illness. 





