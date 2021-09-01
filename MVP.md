**MVP**

So far, I have cleaned my data/performed EDA and completed a baseline model. My (revised) target is whether or not a middle or high school student who completed the 2020 National Youth Tobacco Survey (NYTS) has ever used an electronic cigarette.  Out of the 13,000+ students, 24.4% have used e-cigarettes. 

The baseline model uses 5 of the 25 features:
- the student’s grade in school (6th through 12th)
- whether or not they have ever:
  - smoked a cigarette
  - smoked a cigar or cigarillo
  - used any other tobacco product
  - vaped marijuana

For the baseline model, I used KNN with k=5. The F2 score is 0.591 on the training set and 0.582 on the testing set. I am using F2 score as my primary metric because identifying all students who may be at risk of e-cigarette use (i.e. recall) is more important than having confidence that every one of them is actually at risk (i.e. precision). The confusion matrix for this baseline model demonstrates a large number of false negatives (see attached) - hopefully I can reduce this number with additional features/models. 

<img width="506" alt="Confusion matrix baseline model" src="https://user-images.githubusercontent.com/79233614/131613253-f110cfde-0e8a-48a4-82d1-f9769ddef42b.png">

Ideally, I would like to prioritize interpretability over performance - in order to shed light on the factors most associated with e-cigarette use. I plan to try as many models as I can. I will, of course, try a logistic model, but I’m aware that it may perform poorly because my data has many binary features (0s/1s). I’ll be curious to see if a random forest performs better, although I know I’ll lose out on interpretability.  
