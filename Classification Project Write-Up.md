# Classification Project Write-Up

#### Scone or Biscuit?

### Abstract:

The goal of this project was to use classification models to determine whether a recipe was for a scone or a biscuit. Biscuits and scones are two types of quick breads that are very similar to each other and often made of the exact same ingredients. I scraped data from Allrecipes.com to get biscuit and scone recipes and ended up with 154 recipes for scones and 131 recipes for biscuits. I create a voting ensemble comprised of a logistic regression, random forrest classifier, and k-nearest neighbor models that performs with 81% accuracy on a hold out set of 57 recipes. I find that generally biscuits are less sweet, use less wet ingredients, and use fewer add ins than their scone counterparts. 



### Design:

This project aims to classify if a recipe is for a scone or an American biscuit. In the UK biscuits are what Americans call cookies and they would likely call an American biscuit a scone. In the US one can find recipes for both biscuits and scones, but the distinguishing features between them can at times be a bit murky. In 2015 Dawn Perry wrote an article in bon appetite discussing the subtle differences between scones and biscuits www.bonappetit.com/recipes/article/scone-is-not-a-biscuit. The aim of this project is to see if we can differentiate the two categories of bread using data. This work would be useful to food bloggers who may want data to back their arguments, or organizations that house recipes so that they can better categorize them. Herein I look at a logistic regression, random forrest classifier, and k-nearest neighbor model to see which can best classify the data. I ultimately settle on a voting ensemble classifier to classify the data. 



### Data:

The data comes from Allrecipes.com, which is a recipe sharing social network. I collect 154 scone and 131 biscuit recipes, which is every biscuit and scone recipe Allrecipes has. Features I collect from the recipes include baking temperature, baking time, number of steps, number of ingredients, prep time, baking yield, calories, as well as the amount of a number of common ingredients found in the recipes. 



### Algorithms:

* k-nearest neighbors
* Logistic regression
* Random forrest classifier
* Voting ensemble
* Lasso logistic regression

I look at a number of different metrics, but ultimately settle on accuracy being the metric I wanted to focus on. I split the data into a 60:20:20 train, validate, test dataset and don't touch the test dataset until the final performance evaluation. I mostly do single fold cross validation, though in part of my modeling to reduce the number of features I use 5-fold cross validation on the combined training and validation sets to determine which features I could eliminate. 

The final ensemble voting method, which was equally weighted between the k-nearest neighbor, logistic regression, and random forrest classifier, had an accuracy of .81 on the test dataset. 



### Tools

* Numpy and Pandas for data manipulation
* Recipe-scraper and beautiful soup for scraping recipe data
* Scikit-learn for modeling
* Matplotlib and Seaborn for plotting



### Communication

There is a powerpoint slide to go along with this write up. 













