Question/need:
- What is the framing question of your analysis, or the purpose of the model/system you plan to build?
	- The use of electronic cigarettes remains popular among teenagers in the United States. About 20% of high school students are current e-cigarette users, and many will continue to use e-cigarettes or other tobacco products into adulthood. The National Youth Tobacco Survey (NYTS), conducted annually by the Centers for Disease Control and Prevention (CDC) and the Food and Drug Administration (FDA),  provides data about middle and high school students’ tobacco-related beliefs, exposure to pro- and anti-tobacco influences, and behaviors (including their use of electronic cigarettes and other tobacco products). I plan to use the most recent survey data (2020, collected in early 2020 just prior to school closures due to COVID-19) to examine the factors associated with difficulty QUITTING tobacco products among teenagers who use electronic cigarettes. 
- Who benefits from exploring this question or building this model/system?
	- Teenagers trying to quit (and their parents/friends/family)
  - Anyone involved in a tobacco prevention or treatment programs

Data Description:
- What dataset(s) do you plan to use, and how will you obtain the data?
	- I have downloaded the 2020 National Youth Tobacco Survey (NYTS) dataset from the cdc website: https://www.cdc.gov/tobacco/data_statistics/surveys/nyts/index.htm 
- What is an individual sample/unit of analysis in this project? What characteristics/features do you expect to work with?
	- The dataset contains 14,000+ data points, each representing an anonymized middle or high school student who completed the survey. I plan to use a subset of those data points, specifically the ~1500 “current” electronic cigarette users (current = use within 30 days). 
  - This dataset has over a hundred columns, each representing a survey question or part of a survey question (many answer choices are represented as dummy variables). I will only be using a subset of these as features. The features I am considering:
    - Age (Q1)
    - Sex (Q2)
    - Race/ethnicity (Q3 & 4)
    - How old were you when you first used an e-cigarette, even once or twice? (Q7)
    - In total, on how many days have you used e-cigarettes in your entire life? (Q8)
    - During the past 30 days, on how many days did you use e-cigarettes? (Q9)
    - When was the last time you used an e-cigarette, even one or two times? (Q10)
    - Which of the following best describes the type of e-cigarette you have used in the past 30 days? (Q11)
    - During the past 30 days, what brand of e-cigarettes did you usually use? (Q13)
    - During the past 30 days, where did you get or buy the e-cigarettes that you have used? (Q15)
    - What are the reasons that you have used e-cigarettes? (Q16)
    - Have you ever vaped marijuana or cannabis? (Q21)
    - Have you ever smoked a cigarette, even one or two puffs? (Q22)
    - How old were you when you first smoked a cigarette, even one or two puffs? (Q23)
    - Calculated field: Age when first used an e-cigarette - Age when first smoked a cigarette (to see if e-cigarette use preceded cigarette smoking)
    - During the past 30 days, on how many days did you smoke cigarettes? (Q25)
    - During the past 30 days, on the days you smoked, about how many cigarettes did you smoke per day? (Q27)
    - Were any of the e-cigarettes that you used in the past 30 days flavored to taste like menthol, mint, clove or spice, alcohol, candy, fruit, chocolate, or any other flavor? (Q59)
    - During the past 30 days, have you had a strong craving or felt like you really needed to use a tobacco product of any kind? (Q61)
    - How soon after you wake up do you want to use a tobacco product? (Q62)
    - During the past 30 days, how did you get your e-cigarettes? (Q69)
    - During the past 30 days, where did you buy your e-cigarettes?  (Q70)
    - During the past 30 days, did anyone refuse to sell you any tobacco products because of your age? (Q71) ? 
    - Does anyone who lives with you ..use e-cigarettes? (Q114)
    - How much do you think people harm themselves when they smoke cigarettes some days but not every day? (Q83)
    - How much do you think people harm themselves when they use e-cigarettes some days but not every day? (Q88)
    - Do you believe that e-cigarettes are (LESS ADDICTIVE, EQUALLY ADDICTIVE, or MORE ADDICTIVE) than cigarettes? (Q89)
- If modeling, what will you predict as your target? 
  - Target would be whether an electronic cigarette user is having “difficulty quitting” or “not”. “Difficulty quitting” would be defined as an answer of “2 or more times” in response to the question:
    - During the past 12 months, how many times have you stopped using all tobacco products for one day or longer because you were trying to quit all tobacco products for good? (Q64)
  - I could add a third class: “Former user”. A “former user” would be someone who has used e-cigarettes +/- other tobacco products in the past, but has not used any tobacco products within 30 days - in other words, the person has successfully quit
	  - Adding this third class would mean broadening the data points to include to the ~3000 “ever used” electronic cigarette users. This would also require dropping any features that ask about patterns within the last 30 days (which could be a problem - many of the relevant features focus on last 30 days)

Tools:
- How do you intend to meet the tools requirement of the project?
	- I will build a classification model in python
- Are you planning in advance to need or use additional tools beyond those required? No

MVP Goal:
- What would a minimum viable product (MVP) look like for this project?
	- A figure of the target versus answer to the question “ In total, on how many days have you used e-cigarettes in your entire life?" (Q8) 

