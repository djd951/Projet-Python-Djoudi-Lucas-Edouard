# Projet-Python-Djoudi-Lucas-Edouard
To achieve our project, we did serveral step that we are going to introduce.

Step 1 : Data Explanation

The dataset that we used for our Final Project is about Drug Consumption. It was made from a survey where the participants were judged on 12 attributes such are their ages, the country there come from, or more complex attributes like Personality measurements such as being open minded or aggressive.
The participants were also asked about the consumption of drugs like Cannabis, Nicotine, Cocaine, LSD or Caffeine. They had to say when was the last time they consumed it, and then 7 categories were made from "Never used" to "Used over the last day".
The dataset had 1885 respondents, so 1885 lines.

Step 2 : Data cleaning

So, on the website , one part was the explanation of all the values.
Indeed had to clean up the data for several reasons. In addition to making the dataset more readable, we had to modify it because most of the data set values were numerical. On the site, one can find the correspondence between the numerical values and their meaningues.
For example, we can see on the website that Gender can take the value 0.48246 or -0.48246 , which corresponds to Female or Male. SO we had to repeat this process for every columns in the dataset. To achieve it, we used a Maping. We made a list of dictionaries for each of the 12 attributes columns to replace all the numbers by their real values.
In each dictionaries, the first item is the column name and the number of the column associated with this name.
For the drugs consumption columns, we used 2 dictionaries , one with the labels and what they meant, and one for all of the columns.

Step 3 : Visualizations

Once we had a readable dataset, we decided to analyze it by making graphs. We representend serveral parameters such as the distribution of the population studied by Age, Education, Ethnicity, or even Country. We saw that our data is really biased, and that it will make it complicated for doing predictions. Then we have studied the corelation between some consumptions and our attributes such as Alcohol or Cocaine consumption. After analyzing the heatmaps, we noticed that the Cocaine consumption was better to predict because it was more corelated to our attributes.

Step 4 : Modeling

So we encoded our variables for making them numeric with the LabelEncoder().
Then we splited out dataset into Train and Test.
We used 3 algorithms for modelling : Random_Forest, SVM and KNN.

So our purpose was to predict the drugs consumption of people.
We did two different predictions : the first one was to predict every labels (Never Used, Used over a decade ago,...), and the second one was to predict only two labels such as Used in the last month or more recently and Used in the last year or more formerly.
For the first preidction, we tried to predict cocaine consumption, and for the second one, we tried to predict cannabis consumption.

For Cocaine consumption : 
- We only used the attributes in the first modelisation, and in the second modelisation we used the attributes and the other drugs consumption.
- Our metric of comparaison between algorithms and method was the Accuracy
- We tried to predict all of the labels , so Last day or Last Week or Last Year.

We noticed that for the first method using only attributes, the accuracy was almost the same for all the algorithms, and was about 0,5. But, for the second method using the attributes and drugs consumptions, Random_Forest is the one with the best accuracy, which was about 0,65.
And it makes sense that using the other drugs consumption is doing a better prediction because most of the time if someone is taking cocaine, he will take something else.

For Canabis Consumption : 
- We used only the attributes
- We tried to predict only 2 labels, people who consumed Canabis in the last month or more recently, and the people who consumed Canabis in the last year or more formerly
- We compared each algorithm with a Roc Curve

We could see on the Roc Curve that the best prediction model was the Random_Forest one, rather than SVC or KNN. 
Furthermore, we could see that the accuracy for the Random_Forest algorithm was about 0,86, which was better than the accuracy in the first method. We can explain it because because we have less labels to predict.

Step 5 : Conclusion

 This project was very nice to do because we could use the library sklearn, matplotlib, seaborn and pandas.
• The transformation of the raw data to our dataset was really interesting and maybe could have been done more optimaly.
• The biggest problem of our predictions is that the data is really biased and not corelated to Drug consumption, so its really hard to make better prediction.
• The thing to make the prediction better is to change the problem from trying to predict 7 distinct labels as last day, last week , last month , but only 2 labels that you define as over the last year or not.
