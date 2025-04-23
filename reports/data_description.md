https://www.kaggle.com/competitions/widsdatathon2025

The WiDS Datathon was developed with Ann S. Bowers Women’s Brain Health Initiative (WBHI) in collaboration with Cornell University and UC Santa Barbara. Datasets and support are provided by the Healthy Brain Network (HBN), the signature scientific initiative of the Child Mind Institute, and the Reproducible Brain Charts project (RBC).


## **Dataset Folders**

---

### The training folder **TRAIN_NEW** consists of three types of information about the 1,200+ subjects. They are:

a) the targets (ADHD diagnosis and sex)

b) functional MRI connectome matrices

c) socio-demographic information, e.g., subject’s “handedness” or “parent’s education level”, emotions (“Strength and Difficulties Questionnaire”), and parenting information (“Alabama Parenting Questionnaire”). These include both quantitative and categorical metadata.

Friendly hint: Participants will need to process the categorical data (perhaps create dummy variables) and then combine this processed dataset with the functional connectome dataset to create a final training dataset to use in their models.

---

### The test folder **TEST** consists of unseen data frames for 300+ subjects. These data frames are as follows:

a) functional MRI connectome matrices

b) socio-demographic, emotions, and parenting information


---
## Demographics

Demographics include demographic and administrative information about participants including age, sex, protocol completion status, and commercial use of the data. Age and sex are calculated when the participant is enrolled in the study. 

## Pre-Interview- Demographics/Family

Intake Interview is completed by a clinician at the first visit. Parent(s) of participants are asked detailed questions about their family demographics and language, and the child's developmental, educational, and treatment history.

## Edinburgh Handedness Questionnaire

Edinburgh Handedness Inventory is a measurement scale used to assess the dominance of a person's right or left hand in everyday activities. The inventory can be used by an observer assessing the person, or by a person self-reporting hand use.

## MRI Information

Information about the MRI sessions

## Ishihara Color Vision Test

Ishihara Color Vision Test is a color perception test for red-green color deficiencies. The test consists of either 24 plates containing a circle of dots in various sizes and colors. Within the pattern are dots that form a number visible to those with normal color vision and invisible, or difficult to see, for those with red-green color vision defect.

## Alabama Parenting Questionnaire - Parent Report

Alabama Parenting Questionnaire is a 42-item questionnaire measuring five domains of parenting that are relevant to the etiology and treatment of child externalizing problems: positive involvement, supervision/monitoring, use of positive discipline, consistency in the use of such discipline, and use of corporal punishment. 

## Barratt Simplified Measure of Social Status

Barratt Simplified Measure of Social Status is built on the work of Hollingshead (1957, 1975) who devised a simple measure of Social Status based on marital status, retired/employed status (retired individuals used their last occupation), educational attainment, and occupational prestige. This is a measure of social status, which is a proxy for socio-economic status. This is not a measure of social class, which is best seen as a cultural identity.  

## Strength and Difficulties Questionnaire

Strengths and Difficulties Questionnaire is a brief behavioral screening questionnaire with 25 items on psychological attributes divided between 5 scales. The extended version includes an impact supplement that asks the caregiver if the participant has experienced a problem and the degree of chronicity, distress, social impairment, and burden to others. 

---

## Quantitative Metadata

* **Edinburgh Handedness Questionnaire**
    * `EHQ_EHQ_Total`: Laterality Index (Score) (float)
        * -100 = 10th left
        * −28 ≤ LI < 48 = middle
        * 100 = 10th right
* **Ishihara Color Vision Test**
    * `ColorVision_CV_Score`: Color vision test score (int)
* **Alabama Parenting Questionnaire - Parent Report**
    * `APQ_P_APQ_P_CP`: Corporal Punishment Score (int)
    * `APQ_P_APQ_P_ID`: Inconsistent Discipline Score (int)
    * `APQ_P_APQ_P_INV`: Involvement Score (int)
    * `APQ_P_APQ_P_OPD`: Other Discipline Practices Score (Not factored into total score but provides item level information) (int)
    * `APQ_P_APQ_P_PM`: Poor Monitoring/Supervision Score (int)
    * `APQ_P_APQ_P_PP`: Positive Parenting Score (int)
* **Strength and Difficulties Questionnaire**
    * `SDQ_SDQ_Conduct_Problems`: Conduct problems scale (int)
    * `SDQ_SDQ_Difficulties_Total`: Total Difficulties Score (int)
    * `SDQ_SDQ_Emotional_Problems`: Emotional Problems Scale (int)
    * `SDQ_SDQ_Externalizing`: Externalizing Score (int)
    * `SDQ_SDQ_Generating_Impact`: Generating Impact Scores (int)
    * `SDQ_SDQ_Hyperactivity`: Hyperactivity Scale (int)
    * `SDQ_SDQ_Internalizing`: Internalizing Score (int)
    * `SDQ_SDQ_Peer_Problems`: Peer Problems Scale (int)
    * `SDQ_SDQ_Prosocial`: Prosocial Scale (int)
* **MRI Information**
    * `MRI_Track,Age_at_Scan`: Age at time of MRI scan (float)

## Categorical Metadata

* **Demographics**
    * `Basic_Demos_Enroll_Year`: Year of enrollment (int)
    * `Basic_Demos_Study_Site`: Site of phenotypic testing (categorical int)
        * 1 = Staten Island
        * 2 = MRV
        * 3 = Midtown
        * 4 = Harlem
        * 5 = SI RUMC
* **Pre-Interview- Demographics/Family**
    * `PreInt_Demos_Fam_Child_Ethnicity`: Ethnicity of child (categorical int)
        * 0 = Not Hispanic or Latino
        * 1 = Hispanic or Latino
        * 2 = Decline to specify
        * 3 = Unknown
    * `PreInt_Demos_Fam_Child_Race`: Race of child (categorical int)
        * 0 = White/Caucasian
        * 1 = Black/African American
        * 2 = Hispanic
        * 3 = Asian
        * 4 = Indian
        * 5 = Native American Indian
        * 6 = American Indian/Alaskan Native
        * 7 = Native Hawaiian/Other Pacific Islander
        * 8 = Two or more races
        * 9 = Other race
        * 10 = Unknown
        * 11 = Choose not to specify
* **MRI Information**
    * `MRI_Track_Scan_Location`: Scan location (categorical int)
        * 1 = Staten Island
        * 2 = RUBIC
        * 3 = CBIC
        * 4 = CUNY
* **Barratt Simplified Measure of Social Status**
    * `Barratt_Barratt_P1_Edu`: Parent 1 level of education (categorical int)
        * 3 = Less than 7th grade
        * 6 = Junior high/Middle school (9th grade)
        * 9 = Partial high school (10th or 11th grade)
        * 12 = High school graduate
        * 15 = Partial college (at least one year)
        * 18 = College education
        * 21 = Graduate degree
    * `Barratt_Barratt_P1_Occ`: Parent 1 occupation (categorical int)
        * 0 = Homemaker, stay at home parent.
        * 5 = Day laborer, janitor, house cleaner, farm worker, food counter sales, food preparation worker, busboy.
        * 10 = Garbage collector, short-order cook, cab driver, shoe sales, assembly line workers, masons, baggage porter.
        * 15 = Painter, skilled construction trade, sales clerk, truck driver, cook, sales counter or general office clerk.
        * 20 = Automobile mechanic, typist, locksmith, farmer, carpenter, receptionist, construction laborer, hairdresser.
        * 25 = Machinist, musician, bookkeeper, secretary, insurance sales, cabinet maker, personnel specialist, welder.
        * 30 = Supervisor, librarian, aircraft mechanic, artist and artisan, electrician, administrator, military enlisted personnel, buyer.
        * 35 = Nurse, skilled technician, medical technician, counselor, manager, police and fire personnel, financial manager, physical, occupational, speech therapist.
        * 40 = Mechanical, nuclear, and electrical engineer, educational administrator, veterinarian, military officer, elementary, high school and special education teacher.
        * 45 = Physician, attorney, professor, chemical and aerospace engineer, judge, CEO, senior manager, public official, psychologist, pharmacist, accountant.
    * `Barratt_Barratt_P2_Edu`: Parent 2 level of education (categorical int)
        * 3 = Less than 7th grade
        * 6 = Junior high/Middle school (9th grade)
        * 9 = Partial high school (10th or 11th grade)
        * 12 = High school graduate
        * 15 = Partial college (at least one year)
        * 18 = College education
        * 21 = Graduate degree
    * `Barratt_Barratt_P2_Occ`: Parent 2 occupation (categorical int)
        * 0 = Homemaker, stay at home parent.
        * 5 = Day laborer, janitor, house cleaner, farm worker, food counter sales, food preparation worker, busboy.
        * 10 = Garbage collector, short-order cook, cab driver, shoe sales, assembly line workers, masons, baggage porter.
        * 15 = Painter, skilled construction trade, sales clerk, truck driver, cook, sales counter or general office clerk.
        * 20 = Automobile mechanic, typist, locksmith, farmer, carpenter, receptionist, construction laborer, hairdresser.
        * 25 = Machinist, musician, bookkeeper, secretary, insurance sales, cabinet maker, personnel specialist, welder.
        * 30 = Supervisor, librarian, aircraft mechanic, artist and artisan, electrician, administrator, military enlisted personnel, buyer.
        * 35 = Nurse, skilled technician, medical technician, counselor, manager, police and fire personnel, financial manager, physical, occupational, speech therapist.
        * 40 = Mechanical, nuclear, and electrical engineer, educational administrator, veterinarian, military officer, elementary, high school and special education teacher.
        * 45 = Physician, attorney, professor, chemical and aerospace engineer, judge, CEO, senior manager, public official, psychologist, pharmacist, accountant.

## Targets

* **Diagnosis:ADHD_type**
    * `ADHD_Outcome`: Type of Diagnosis (str)
        * 0 = Other/None, 1 = ADHD
* **Demographics:Basic_Demos,Sex**
    * `Sex_F`: Sex of participant (categorical int)
        * 0 = Male
        * 1 = Female




*Functional Connectomes

In our Tutorial & Resources, we have provided material that introduces the idea of functional connectivity. 

After functional MRI (fMRI) data is collected using a resting-state scan (a scan where the participant is not performing a specific task), the raw fMRI data undergoes several preprocessing steps (www.biorxiv.org/content/10.1101/2025.02.24.639850v1), such as: 

- Motion correction to adjust for head movement during scanning; 

- Realignment to align to anatomical scans; 

- Segmentation to divide the brain into regions of interest (ROIs), which are defined by either anatomical or functional criteria; 

- Spatial normalization to align the brain data to a standard template (e.g., MNI space); 

- Temporal filtering to remove noise and physiological signals (like heartbeats or respiration). 

To compute connectivity maps, the time series of fMRI signals (i.e., changes of brain signal over time) for each ROI are extracted and the connections between different brain regions are computed. There are different ways to compute correlations (or connections) among regions, for instance by computing partial or Pearson correlations, and both those methods are equally valid. 



Pearson Correlation:

Pearson correlation is a statistical measure of the linear relationship between two time series of two brain regions. Pearson correlation coefficients are calculated between pairs of regions of interest, yielding a matrix of connectivity strengths. This measure is simple, computationally efficient, and easy to interpret but it assumes that the relationship between regions is linear and is sensitive to global signal fluctuations, such as movement artifacts or physiological noise. 

