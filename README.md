# Project Overview <br />

# Links<br />

>>Trello - https://trello.com/b/S3r1D66S/final-project-movies <br />
>>Tableau - https://public.tableau.com/app/profile/ashton.walker/viz/FinalProjectOverview_16765963190680/Dashboard1?publish=yes <br />


#Summary<br />


# Our Question
## We wanted to see what affected a movies rating. 
### With this question we could explore many variables, such as genre, budget, release date, and runtime.

# Data Cleaning
### When we first took a look at the data, there was a ton present in the csv. About 46.6k rows were present in the data, and upon inspection there were an untold amount of cells that had bad or corrupted data
> This can be due to a variety of formatting issues, or issues with non-english characters
![image](https://user-images.githubusercontent.com/112450151/220477095-7918ffa9-bf22-4613-a6c9-13b4f842a0d7.png)
## What We Cleaned
##### We began by deciding to limit the amount of data we were using by deciding to only use movies released after 1970, as many movies from before then had no information on budget or revenue. We then decided to eliminate any movies whos language was not in English. This removed a good chunk of rows that had character that excel could not make sense of. Once that was finished, we noticed that many movies generated 0 reveneu. Upon inspection and some googling, many of these movies were Netflix specials, so there was technically no revenue to be gained from the release; Although new paying subscribers who joined for just that movie would be able to be counted as revenue, the csv did not have that information. Average rating was changed to rating for simplification. and language as a column was removed as it is all now in english. Other coloumns removed include things like adult rating, poster path, etc. 
> There are now only 4362 rows
![image](https://user-images.githubusercontent.com/112450151/220478483-1f31c3db-7379-4707-8dcc-6781207b1fa2.png)

# Tableau
![image](https://github.com/kindaoriginal/final_project/blob/main/Resources/pics/chrome_iPf7B3Hafb.png)
### In our tableau dashboard we wanted to show the overall revenue gain/loss from certain months or by specific genres. But also wanted to be able to see exactly what a specific movie brought in during those months by applying a filter to be able to select from a list of all movies released in the U.S. after 1970.
## What we noticed
#### During the months of May/June/July specifically when school is out for most kids/adults, is when movies tend to produce higher revenue. The same can be said for the month of December (everybody loves Christmas Day movies). So if you are looking to start directing movies, release them in the summer. But also thats when all the best movies come out so you'll have some big competition.
![image](https://github.com/kindaoriginal/final_project/blob/main/Resources/pics/chrome_1nMuvw5G0I.png)

# Machine Learning
##### We tried using machine learning to see if we could get a predictive model from our data. 
### We decided to use Linear Regression to try and make predictions on if budget was a deciding factor on a movies rating
> The line of fit seems to have much more dots on the lower end of budget. It seemed to only predict one or two dots on the higher end of budget above a 6 rating, which is our cutoff for a decent movie.
![image](https://user-images.githubusercontent.com/112450151/221037023-3d4b97f4-5a82-4f81-af78-f18265b10164.png)
### Our confusion matrix was not the best predictor, with an accuracy score of .52 or 52%. Just above half, a coin flip would be just as good on whether or not budget affects a movies rating
> The confusion matrix could not adequately correctly predict if a movies rating was affected by the budget
![image](https://user-images.githubusercontent.com/112450151/221038454-6f7f1211-9ca8-4682-8abd-b2e8a60f88aa.png)
#### We also tried to do a logistic model on month vs rating, but tableau proved to be a much better tool to see that correlation. 
![image](https://user-images.githubusercontent.com/112450151/221038909-c082e7f8-ecb3-42d9-a4f8-cd6f7a8e40ba.png)
#### Finally we used a Random Forest model to try and get a better prediction, but it was still 52%
![image](https://user-images.githubusercontent.com/112450151/221125690-ad2086d2-c42e-4110-aa78-628e36a7cf6a.png)
![image](https://user-images.githubusercontent.com/112450151/221125816-715127e8-51a3-4581-9965-c35a10b32673.png)


