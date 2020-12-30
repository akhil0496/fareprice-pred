# fareprice-pred

#step1 : Read the Data

#step2 : Feature Engineering

-Python timedelta() function is present under datetime library which is generally used for calculating differences in dates and also can be used for date manipulations in     python. 
-It is one of the easiest ways to perform date manipulations.
-Indian Standard Time is 5 hours and 30 minutes ahead of Universal Time Coordinated. changed time to IST. 
-Extracted Year, Month, Day, Hour, Minute
-further hours are distinguished as 0-for morning, 1-for night

-Implemented Haversine distances to calculate total distance
-reference:https://scikit-learn.org/stable/modules/generated/sklearn.metrics.pairwise.haversine_distances.html#:~:text=The%20Haversine%20(or%20great%20circle,the%20data%20must%20be%202
#Calculating The Haversine Distance:
-The haversine formula determines the great-circle distance between two points on a sphere given their longitudes and latitudes. Important in navigation, it is a special case of a more general formula in spherical trigonometry, the law of haversines, that relates the sides and angles of spherical triangles.

-Drop unwanted variables

#step3: Model Building - Regression model 
-Target variable is a fare_amount 
-Checked Feature Importance 
-Done modelling with xgboost, ANN, TPOTRegressor Automated Library 
Got best score and best pipeline given by tpot was ElasticNetCV-ExtraTreesRegressor 

###TPOT:
-->The Tree-Based Pipeline Optimization Tool (TPOT) was one of the very first AutoML methods and open-source software packages developed for the data science community.
-->The goal of TPOT is to automate the building of ML pipelines by combining a flexible expression tree representation of pipelines with stochastic search algorithms such as         genetic programming. TPOT makes use of the Python-based scikit-learn library as its ML menu.

###genetic programming:
-->Genetic Programming (GP) is a type of Evolutionary Algorithm (EA), a subset of machine learning. EAs are used to discover solutions to problems humans do not know how to solve, directly. Free of human preconceptions or biases, the adaptive nature of EAs can generate solutions that are comparable to, and often better than the best human efforts.*
-->With the right data, computing power and machine learning model you can discover a solution to any problem, but knowing which model to use can be challenging for you as there  are so many of them like Decision Trees, SVM, KNN, etc. That's where genetic programming can be of great use and provide help. Genetic algorithms are inspired by the      Darwinian process of Natural Selection, and they are used to generate solutions to optimization and search problems in computer science.
-->Broadly speaking, Genetic Algorithms have three properties:
-Selection: You have a population of possible solutions to a given problem and a fitness function. At every iteration, you evaluate how to fit each solution with your fitness     function.
-Crossover: Then you select the fittest ones and perform crossover to create a new population.
-Mutation: You take those children and mutate them with some random modification and repeat the process until you get the fittest or best solution.
 
 Reference: http://geneticprogramming.com/
 
