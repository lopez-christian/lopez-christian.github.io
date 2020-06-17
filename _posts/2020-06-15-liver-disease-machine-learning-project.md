---
layout: post
published: true
title: 'Liver Disease Machine Learning Project'
date: '2020-06-15'
---
## Implementing Various Machine Learning Algorithms and Hyperparameter Tuning On The Indian Liver Patient Records Dataset

<p align="center">
<img width="661" alt="Screen Shot 2020-06-15 at 6 39 33 PM" src="https://user-images.githubusercontent.com/53641091/84722268-910f9100-af37-11ea-8950-8210f5ccd481.png">
</p>

For this project I went ahead and implemented a number of machine learning algorithms on the dataset: Indian Liver Patient Records - Patient records collected from North East of Andhra Pradesh, India [click here](https://www.kaggle.com/uciml/indian-liver-patient-records). The goal was to better predict whether an individual is likely to develop liver disease given certain features which included the age, gender, total bilirubin, direct bilirubin, alkaline phosphotase, alamine aminotransferase, aspartate aminotransferase, total proteins, albumin, and albumin and globulin ratio of the individual.  

<p align="center">
<img width="992" alt="Screen Shot 2020-06-15 at 6 53 26 PM" src="https://user-images.githubusercontent.com/53641091/84723028-881fbf00-af39-11ea-8587-dd7ddfc2bd72.png">
</p>

The data mining and exploration step dealt some interesting insights regarding the data. There were some compelling countplots and undelying correlations that I came across. I won't list them all, but I will say that most of the people that were tested were male patients. The description of the dataset did not provide any background as to why this is so. Also, most of the patients that tested positive were male. The discrepencies were astonishing. Adults aged 24-63 were also significantly impacted by this liver disease, as opposed to young patients, and the elderly. There were also high correlations between certain features like direct bilirubin v. total bilirubin, alamine aminotransferase v. aspartate aminotransferase, total proteins v. albumin, and albumin v. albumin and globulin ratio. 

<p align="center">
<img width="1010" alt="Screen Shot 2020-06-16 at 12 04 03 PM" src="https://user-images.githubusercontent.com/53641091/84817262-7dad0600-afc9-11ea-97eb-69f1247040e7.png">
</p>

<p align="center">
<img width="390" alt="Screen Shot 2020-06-15 at 6 43 31 PM" src="https://user-images.githubusercontent.com/53641091/84722596-7e498c00-af38-11ea-98d9-e2f37bdc8d3f.png">
</p>

<p align="center">
<img width="407" alt="Screen Shot 2020-06-15 at 6 44 23 PM" src="https://user-images.githubusercontent.com/53641091/84722714-d7b1bb00-af38-11ea-9a34-19eae2d874ce.png">
</p>

<p align="center">
<img width="413" alt="Screen Shot 2020-06-15 at 6 45 09 PM" src="https://user-images.githubusercontent.com/53641091/84723213-f1073700-af39-11ea-9605-0669de096780.png"><img width="413" alt="Screen Shot 2020-06-15 at 6 45 23 PM" src="https://user-images.githubusercontent.com/53641091/84723256-03817080-af3a-11ea-9f8b-2f76894e8fd7.png">
</p>

<p align="center">
<img width="413" alt="Screen Shot 2020-06-15 at 6 45 32 PM" src="https://user-images.githubusercontent.com/53641091/84723265-08debb00-af3a-11ea-8882-97e73fc99734.png"><img width="413" alt="Screen Shot 2020-06-15 at 6 45 42 PM" src="https://user-images.githubusercontent.com/53641091/84723270-0d0ad880-af3a-11ea-97f9-caa1e19aa704.png">
</p>

The dataset was manipulated and cleaned using an assortment of libraries that included Pandas and Matplotlib. There was quite some feature engineering to do that included renaming certain columns, dealing null values, handling outliers, and log-transforming and min-max scaling the continous features. There was also some binning that had to be done regarding the age column in order to make the results easier to interpret and visualize. One-hot encoding was performed on any discrete features. 

<p align="center">
<img width="945" alt="Screen Shot 2020-06-15 at 7 00 05 PM" src="https://user-images.githubusercontent.com/53641091/84723466-80ace580-af3a-11ea-802d-6208f2238b56.png">
</p>

<p align="center">
<img width="461" alt="Screen Shot 2020-06-15 at 7 00 20 PM" src="https://user-images.githubusercontent.com/53641091/84723512-98846980-af3a-11ea-9173-c6840cae4520.png"><img width="461" alt="Screen Shot 2020-06-15 at 7 00 27 PM" src="https://user-images.githubusercontent.com/53641091/84723515-9a4e2d00-af3a-11ea-8be1-821557d4d1b0.png">
</p>

After creating our machine learning-ready-dataset we went ahead and applied our machine learning algorithms. These were classification algorithms that included Support Vector Machines (SVM), K-Nearest Neighbors, Decision Tree, Random Forest, Gradient Boosting Machines (GBM), eXtreme Gradient Boosting (XGBoost), and AdaBoost. These produced varying test metrics, and AUC measures. The. highest ranking proved to be the Random Forest algorithm with Accuracy Score: 0.7678571428571429 and AUC: 0.64140625. The AUCs were used to create and ROC/AUC Curve plot that compared all the algorithms. Having arrived at the conlusion that Random Forest was the best-performing out of the bunch, I went ahead and executed some hyperparameter tuning and optimizations using RandomizedSearchCV. Another ROC/AUC Curve plot was generated to show the newly incorporated Random Forest + Optimization AUC. The Random Forest + Optimization algorithm had Accuracy Score: 0.7440476190476191 and AUC: 0.55703125. This algorithm did slightly worse on both measures when compared to the Random Forest on default parameters. 

<p align="center">
<img width="843" alt="Screen Shot 2020-06-15 at 7 51 54 PM" src="https://user-images.githubusercontent.com/53641091/84726443-b0abb700-af41-11ea-8e2d-d4d62b7b028e.png">
</p>

## Key takeways:

*1. There is evidence of correlations between certain features. What this tells us is that certain features can be indicative of other features being elevated as well. An example of this would be the high positive correlation between direct bilirubin and total bilirubin. If a patient were to come in with high levels of direct bilirubin, we would be safe to assume that the likelihood that they also have a high incidence of total bilirubin is quite high. The health care practitioner could choose to only administer certain tests and not others, which could potentially save a both the healthcare practitioner and patient vasts amounts of time and resources.*

*2. Males comprised most of the dataset by a vast amount. There are many more males than there are females affected by the liver disease as well. We are not made aware of how the data was acquired, but the disparity between genders is astonishing. The measures for all features associated with the disease were much greater in males than in females. These types of discoveries can lead to targeted preventive care for male subjects when they come in for rudimentary check-ups or health issues. Healthcare facilities and various other organizations can take a step in addressing the issue-at-hand and make the public aware of the consequences that are associated with liver disease.*

*3. Adults between the ages of 24-63 years old seem to be the most in danger. This can be attributed to these adults being tested more often for liver disease than are young people and the elderly. We may need to focus more on testing these other demographics. There is a strong possibility that we are missing the greater picture here. If we were to focus on testing the youth and improving their dietary intake, decreasing alcohol consumption, addressing pollution, decontaminating food, and eradicating drug use, we may arrive at a stage where we can prevent our youth from developing liver disease later in their lives.*

<p align="center">
<img width="412" alt="Screen Shot 2020-06-15 at 7 10 22 PM" src="https://user-images.githubusercontent.com/53641091/84726546-f9fc0680-af41-11ea-95c8-a270c3616f42.png"><img width="486" alt="Screen Shot 2020-06-15 at 7 17 35 PM" src="https://user-images.githubusercontent.com/53641091/84726580-0f713080-af42-11ea-8c9c-636995ff2acf.png">
</p>

[Liver Disease Machine Learning Project](https://github.com/lopez-christian/Liver-Disease-Machine-Learning-Project)
