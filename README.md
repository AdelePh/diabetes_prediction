# diabetes_prediction
1. Run the application 
- step 1: clone the repo
- step 2: cd finalproject
- step 3: docker-compose up

2. Data explanation
The data provided included a vast amount of raw information with many different data types were provided, not all data types were used as features. 

- The first features are common risk factors for diabetes such as : weight, age, BMI. But they were recorded each time the patient met with a doctor for example, there were multiple measurements for BMI for a single patient. to have a single feature, I take the median of all non-zero measurements . 
These features were selected from training_transcript table
- The second group feature : The Medication that the patient was taking
I used training_allMeds table for these features
- The third group feature: Diagnoses of the patient
I used training_diagnosis for these features
- The fourth group feature: Lab tests that the patient received.
I used training_labs table for these features

Data for these three were available in similar formats.
for example: if a patient had a lab test once every six months, it may appear six times in the data. 
the feature used was the count of how many times a specific medication, diagnosis, or lab test occurred in the data.
