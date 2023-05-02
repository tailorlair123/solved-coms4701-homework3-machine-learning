Download Link: https://assignmentchef.com/product/solved-coms4701-homework3-machine-learning
<br>
We ask you to implement three small and separate machine learning models. We provide sample input/output file pairs for your reference. The file v​ isualize.py c​ ontains two functions for plotting data which you may choose to use, modify, reference and steal ideas from at will.

<ol>

 <li>Perceptron</li>

 <li>Linear Regression</li>

</ol>

<ul>

 <li>Clustering</li>

</ul>

Note: The Python <u>​</u><u>Pandas</u> <u>​ </u>library helps simplify a lot of the intermediate steps we ask from you below. Key functions include ​<u>reading</u> ​ and <u>w</u>​ <u>riting</u>​  to CSVs, matrix operations, and visualizing data. Examples are provided in ​visualize.py​.

<h1>I.    Perceptron</h1>

Implement the perceptron learning algorithm (PLA) for a linearly separable dataset. Your starter code includes ​input1.csv​, where each line contains ​feature_1,feature_2,label​. All values are numeric with labels 1 or -1. Take a look at the data input file. We suggest using matplotlib or <u>pandas.DataFrame.plot</u>​ (in ​visualize.py​) to view data, and ​<u>pandas.DataFrame.describe</u><u>​</u> to see stats.

Write your PLA in p​ roblem1.py ​ in python 3. Your program takes a csv of input data and a location to write the output csv with the weights from each iteration of your PLA, written as w​ eight_1,weight_2,b.​ The weights in the last line of your output csv defines the <strong>d</strong>​ <strong>ecision boundary</strong> ​computed for the given dataset. Formatting is shown in o​ utput1.csv.​ NOTE: o​ utput1.csv ​ values are purely filler and not representative of the values you should get. Feel free to visualize and include a screenshot of your final decision boundary in your README, like the one below:

We will execute your code as follows:  ​$ python problem1.py input1.csv output1.csv

<h1>II.     Linear Regression</h1>

Use gradient descent to build a linear regression model for predicting height (m) using age (yr) and weight (kg), using data derived from CDC growth charts data.




<strong>Data Preparation and Normalization</strong>​. Load and understand the data from i​ nput2.csv ​ [age(years), weight(kg), height(m)]  remembering to add a vector column for the intercept at the front of your matrix. You’ll notice the features are not on the same scale. What is the mean and standard deviation of each feature? Scale each feature (i.e. age and weight) by its standard deviation, so each scaled feature has a mean of zero. You do not need to scale the intercept. For each feature column, x, use the following formula:




<strong>Gradient Descent.</strong>​ Implement gradient descent to find a regression model in p​ roblem2.py.​ Initialize your β’s to zero. Recall the empirical risk and gradient descent rule as follows:




You will run gradient descent with these nine learning rates: α ∈ {0.001, 0.005, 0.01, 0.05, 0.1, 0.5, 1, 5, 10}, ​<strong>exactly 100 iterations per α</strong>-​ <strong>v</strong>​ <strong>alue</strong>,​ plus a tenth rate and number of iterations of your choice. To pick the tenth rate and loop count, observe how α affects the rate of convergence for the nine rates listed, then pick a rate and loop count you believe will perform well. Briefly explain your choice in your README.




The program should generate an output file containing ten lines, one for each (α, num_iters) hyperparameter pair. Each line contains: ​α,num_iters,bias,b_age,b_weight​, expressed to your choice of decimal places (see example o​ utput2.csv ​ in your starter code). Each line of this file defines the regression model your gradient descent method computed on the given data and hyperparameters.




We will execute your code as follows:

$ python problem2.py input2.csv output2.csv




<strong>Optional.</strong>​ Visualize the result of each linear regression model in three-dimensional space. You can plot each feature on the xy-plane, and plot the regression equation as a plane in xyz-space. Ex:




<h1>III.      K-Means Clustering</h1>

We will segment and group the pixels of ​trees.png​  according to their RGB values with k-means. You can read about image segmentation here: <u>​</u><u>https://en.wikipedia.org/wiki/Image_segmentation</u><u>​</u>.

Experiment with the k-means algorithm. Choose 3 representative k values and use <u>s</u><u>​ </u><u>klearn.cluster.</u> <u>KMeans</u><u>​</u> to process the image file. Thoroughly record (screenshots, short annotations) and explain your results in your README.

Save your work as ​problem3.py.


