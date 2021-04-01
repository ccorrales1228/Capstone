# Loan Default Modeling for Lending Club

Note to vistors:
This is intended for academic purposes. 

Please note, this is a Machine Learning Classification project using Lending Club datasets.


Datasets were sourced via Kaggle:

* https://www.kaggle.com/wordsforthewise/lending-club
* https://www.kaggle.com/ethon0426/lending-club-20072020q1

![Screen Shot 2021-03-25 at 9 14 28 AM](https://user-images.githubusercontent.com/61753153/112478567-87c71680-8d4a-11eb-8f37-c2e416bb74ac.png)


## The Business: Lending Club

### Overview
Lending Club is a peer to peer lending company based in the United States, in which investors provide funds for potential borrowers and investors earn a profit depending on the risk they take (the borrowers credit score). The company also registers its offerings as securities with the Securities and Exchange Commission (SEC), and to offer loan trading on a secondary market. Lending Club provides the "bridge" between investors and borrowers

![7510721-15592751779598007](https://user-images.githubusercontent.com/61753153/112480714-af1ee300-8d4c-11eb-8e28-8b34cb4245ff.png)



### Business Interest
The client (Lending Club) wants to capture applicants that would be able to repay the loan and also identify potentially high-risk borrowers that are likely to default. In turn, the client wants to reduce the potential loss of business of applicants that are likely to not default and identifying applicants that are likely to default. 

![Screen Shot 2021-04-01 at 7 31 14 AM](https://user-images.githubusercontent.com/61753153/113287980-50adb380-92bc-11eb-9aba-0a76736b34c4.png)


### Social Implication
Historically, there is a stigma that lending/loan services have neglected, segregated, and also marginalized applicants from the ability to qualify for a loan will be considered throughout the analysis and within the outlook of the project. Although, the aim is to identify patterns which indicate if a person will likely default based on historical data. The goal is also to help make the application process both inclusive and ethically sound—be it in the form of identifying patterns of exclusion or recommending new product types to open the doors to help future applicants gain an opportunity to qualify for a loan. 

![Screen Shot 2021-04-01 at 7 33 09 AM](https://user-images.githubusercontent.com/61753153/113288150-8fdc0480-92bc-11eb-9138-d2e06571b62e.png)



## The Data

Throughout this iniative we will occassionally refer to the dataset as "the asset". 

Based on the data profile of the Lending Club dataset, there is enough sufficient features to work with to understand our target: fully paid (non-defaulter) and charged-off (default). Please see below for further descriptions based on the Loan Accepted data set.
 
•	Fully paid: Applicant has fully paid the loan (the principal and the interest rate)

•	Charged-off: Applicant has not paid the instalments in due time for a long period of time, client has defaulted on the loan

![Screen Shot 2021-03-25 at 7 33 14 AM](https://user-images.githubusercontent.com/61753153/112477666-a24cc000-8d49-11eb-9359-e2845322a404.png)

Initally, there were over two million observations and 151 variables within the asset. In the first two notebooks, NB1 and NB2, these were used primarily for reducing the asset, sanity checking, lite data exploration. In NB2 were were able to reduce the asset to roughly over 240k of observations and around 27 variabiales with the new asset. 

![Screen Shot 2021-04-01 at 7 11 42 AM](https://user-images.githubusercontent.com/61753153/113286081-b3518000-92b9-11eb-8e4a-a5994100fe68.png)

The CSV process-flow: accepted_2007_to_2018Q4 >> clean_accepted >> clean_accepted_2 >> clean_accepted_3

The primary reason for this the data reduction was due to low memory issues and intensive computing processing limitations. However, in the second iteration of the initiative we will implement possible external dependencies, change of workflow management, and poach for possible external GPU/memory server management systems.



## Notebook Repository Reference

(1) Asset (data) Reduction and Data Wrangling: 
* NB1_ Data_Volume_Reduction 
* NB2_Cleaning_Lite_EDA.ipynb


(2) MVP (Minimum Viable Product):
EDA (univariant) and Additional Data Clensing 
* NB3_Data_Wrangling_EDA1

EDA (bivariant analysis with respect to our response (target) variable), Modeling, and Analysis 
* NB4_EDA2_Modeling_Analysis


(3) Final Pre-Processing, Modeling, Model Analysis, and Project Report
* FinalNB_Modeling_Evaluations_Analysis



## Modeling
* Subject to change based on performance benchmarks or recommendation(s) regarding requirements.

![Screen Shot 2021-04-01 at 7 27 09 AM](https://user-images.githubusercontent.com/61753153/113287548-bc435100-92bb-11eb-9cbc-9229cf292539.png)

In regard to the target variable (default and non-default), this project will be a classification problem. The baseline model will be logistic regression classifier. After baseline analysis I will then apply various classification models: Decision Tree Classifier, Random Forest Classifier, to name a few examples. Following un-tuned model evaluation (recall, precision, F-1, and confusion matrix), the application of GridSearch CV, and some bespoke hyperparameter tuning will follow. Also, at this point, stacking, blending, and boosting as modalities to help with optimization will be considered. Again, throughout the modeling process, the application on model evaluation will aid in determining which model will be best in respect to a minimum viable product. 

![Screen Shot 2021-04-01 at 7 16 34 AM](https://user-images.githubusercontent.com/61753153/113286450-3b378a00-92ba-11eb-832a-32e6a046dac9.png)


If successful, the model will be able to correctly classify clients who will be at risk of defaulting. It is imperative to focus on the mission of this project is to mitigate misclassification, as the client wants to reduce the likelihood of not identifying high-risk applicants that may default and not capturing possible clients who would be an ideal candidate for their services. Additionally, our client will gain a better understanding of enhancing their application process to be more inclusive of applicants with lower FICO score, economic demography (such as lifestyle, occupation, and education), and financial need use cases. 



## Next Steps

![Screen Shot 2021-04-01 at 7 14 00 AM](https://user-images.githubusercontent.com/61753153/113286203-dda33d80-92b9-11eb-91b2-6e50aec874a3.png)

Lastly, addressing deployment, if viable within our given deadline—I intend to deploy the model and business intelligence analysis via a dashboard. This will be showcasing the initial user interface and be used for UAT (user acceptance testing). This will help in testing functionalities of the user/customer interface and a dashboard for internal use for our client to aid their product management and risk operation teams to better understand the customer journey. Further, the dashboard deployment can also assist the marketing analytics teams storyboard for future campaigns. Moreover, in terms of understanding the customer journey, it is imperative to also be mindful of developing a customer story that reflects inclusion, diversity, and access. Therefore, this initiative, is tailored not only for our client’s internal stakeholders, but it is also to help Lending Club lead the charge in potentially creating new product offerings (or enhancing their current model) that support a variety of candidates from various socio-economic backgrounds. 



