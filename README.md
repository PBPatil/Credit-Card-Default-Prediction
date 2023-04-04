# Predicting default on Credit Card Applications for Taiwanese Credit Card Customers


### Hackathon Date: April 22, 2018 


### GreyAtom Team for Hackathon (Team-3):
+ Mr.Vinayak  
+ Ms.Shravani
+ Mr.Sagar
+ Mr.Amrinder
+ Mr.Raviraj
+ Mr.Nikhil
+ Mr.Prasad

### DataSet Reference: 
The <a href="https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients">Defaulters on Credit Card Payment</a> Dataset is taken from UCI Machine learning repository.

### Citation Reference
Yeh, I. C., & Lien, C. H. (2009). The comparisons of data mining techniques for the predictive accuracy of probability of default of credit card clients. Expert Systems with Applications, 36(2), 2473-2480.

### Background:
<hr/><span style="color:black; font-family: 'calibri'; font-size: 1.2em;">Taiwanese financial institutions offered credit card to their customers as part of their business growth and business marketing strategy. It was found that the credit card customers have defaulted on their payments. These defaults can pose risks to future of the bank's financial models and growth. The bank has collected some demographical information and also has access to financial information in terms of transactions, amount due etc. along with the whether customer has defaulted or not. With this historical information, bank would like to build model which can help in identifying the patterns and classify if customer will default on his payments given these patterns. These models will identify the defaulters and build proactive risk controls to prevent future losses. More information about this can be found <a href='https://sevenpillarsinstitute.org/case-studies/taiwans-credit-card-crisis'/>here</a></span>

### Business Goal:
<hr/><span style="color:black; font-family: 'calibri'; font-size: 1.2em;">
We need to build a model which will help business 
<ol>
<li>To predict if the customer will default on his payment given the his transactions and demographical information (as described in the Dataset description section.</li>
<li>Analyze which information helps the most in such decision making and in future build some policies around it.</li>
</ol>
<i>There can also be the other factors which are like credit scores, regularities of payment transactions on utility bills, consumer employment rate and market inflations in Taiwan etc. that  may influence or contribute to this analysis and improve the model efficiency.</i></span> 

### Our Approach
<hr/><span style="color:black; font-family: 'calibri'; font-size: 1.2em;">We are using standard approach / steps for any Machine Learning lifecycle project or some of the steps mentioned in  <a href="https://en.wikipedia.org/wiki/Cross-industry_standard_process_for_data_mining">CRISP-DM (Cross Industry Standard Process Data Mining)</a> model. 
<ol>
<li>About the dataset</li>
<li>Analyze the dataset and transform it using
<ul>
<li>Exploratory Data Analysis</li>
<li>Feature Engineering</li>
<li>Feature Selection</li>
<ul>
<ul>
<li>RFE</li>
<li>PCA</li>
<li>SelectFromModel</li>
<li>SelectKBest</li>
</ul>
</ul>
</ul>
<li>Model Building</li>
<ul>
<li>Logistic Regression (LR)</li>
<li>Decision Tree (DT)</li>
<li>Random Forest (Boostrap Ensemble of DT)</li>
<li>Stacking Ensemble</li>
<li>XgBoost</li>
</ul>
</li>
<li>Performance Evaluation at each step of Model Building</li>
<li>Model Selection</li>
</ol></span>

### Considerations for Model Selection
<hr/><span style="color:black; font-family: 'calibri'; font-size: 1.2em;">Based on the problem statement and goal to be achieved, we need to predict the customer payment defaults in yes or no. This indicates that this is classification problem. We have used classification algorithms such as We will be exploring following performance metrics for a model/models based on following: 
<ol>
<li>Accuracy: Accuracy Score</li>
<li>AUROC Score of the model.</li>
<li>F1 Score.</li>
<li>Precision/Recall Score</li>
<li>Matthew's Correlation Coefficient</li>
<li>Top feature importances predicted by each model</li>
<li>Cost Factor</li>
</ol>
while doing so we will explore several models and try to evaluate the performance each model using these metrics to come up with our suitable recommended model as well as important features/attributes to look at for effectiveness of predictions. The selection of threshold value to decide the decision boundary is based on our intuition. </span>
