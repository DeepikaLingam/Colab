This is the code for predicting rating by analyzing the review text.

Problem Statement:
Given the Board Game reviews, the below snippets of code attempts to predict the rating of the review.

Test and Train data are divided in the ratio of 3:7.

30% of the entire data belongs to test and 70% of data belongs to train.

How did I overcome challenges?
The size of the data was too large to process in reasonable time. To overcome this, whenever I have used sklearn predefined functions, I let the parameters have default values. For custon functions, I have taken only some part of the data.
This is a very classic text classification problem. Comments have null values that were affecting the input of the classifiers. I have removed all the null values because there of no importance. While vectorizing the data, I have removed extra white spaces.
Due to limited RAM, I have grouped my code into blocks that are dependent. Example: For ensemble methods, I have taken voting from 3 different classifiers and made sure that all the 3 classifiers and ensemble are ran together. Remaining snippets of code are independent of each other, thus running them in different sessions did not affect
Considering the size of the data, the execution time of each classifier is reasonably high. To overcome this, I have made used of pipeline functions in sklearn instead of executing all the elements separately.
Distribution of values for different class labels(Rating values) is very random and not uniform. This was the main reason affecting the accuracy. This was one challenge that taught me how real world data is. I have tried different kinds of models to observe what fits better.
The rating column in the data have continous values. For classification, continuous values are difficult to deal. It is almost impossible to classify in continuous values. To overcome this, I have converted it into integers thus obtaining discret values for rating.

Web Server and deployment of the model

Step1: Choosing the right model. I have choosen to do ensembling the best 3 models with highest accuracy.

Step2 : Deployment. Having selected the right model, I have converted my phython file to JOBLIB format for deployment of AWS.

Step3: Train the model with all the data available.

Step4: Set up Front end. My front end is written in jQuery and AJAX that calls the model.

Step5: Sending the input to trained model.

Step6: Displaying output.

Link to page: "http://ldeepika.uta.cloud/MyPortfolio/predict.html"
