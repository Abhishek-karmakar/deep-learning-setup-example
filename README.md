Deeplearning Intro and Quick-definition

- In Machine Learning, we define the outcome and the algorithm learns to reach there.
- There are a lot of Machine Learning models. One of them is Artificial Neural Network. 
- When we go not only one or two level deep by many many level deep while creating our ANN. Its called Deep learning models. 
- Input values proess through all these hidden layers. 
- So in summary : Building Machine Learning Models with Deep Neural Network = Deep Learning 
- Deeplearning can be used to solve many problems like Classification problems or for Computer Vision or Recommendation systems using Deep Boltzman Machines. 


How to get the Dataset

	- get the dataset from https://drive.google.com/file/d/0BwxlRNfHWeNkTWw0VVlkb245aEk/view?usp=sharing

Dataset explaination. 

	- Example dataset of a bank. 
	- Bank can see a increadible churn rate.i.e lot of people leaving the bank. 
	- Bank measured various datas for 6 months for various customer. 
	- Exited value means 1 = left , 0 = still with bank
 

		+-----------+------------+----------+-------------+-----------+--------+-----+--------+----------+---------------+-----------+----------------+-----------------+--------+
		| RowNumber | CustomerId | Surname  | CreditScore | Geography | Gender | Age | Tenure | Balance  | NumOfProducts | HasCrCard | IsActiveMember | EstimatedSalary | Exited |
		+-----------+------------+----------+-------------+-----------+--------+-----+--------+----------+---------------+-----------+----------------+-----------------+--------+
		| 1         | 15634602   | Hargrave | 619         | France    | Female | 42  | 2      | 0        | 1             | 1         | 1              | 101348.88       | 1      |
		+-----------+------------+----------+-------------+-----------+--------+-----+--------+----------+---------------+-----------+----------------+-----------------+--------+
		| 2         | 15647311   | Hill     | 608         | Spain     | Female | 41  | 1      | 83807.86 | 1             | 0         | 1              | 112542.58       | 0      |
		+-----------+------------+----------+-------------+-----------+--------+-----+--------+----------+---------------+-----------+----------------+-----------------+--------+
		| 3         | 15619304   | Onio     | 502         | France    | Female | 42  | 8      | 159660.8 | 3             | 1         | 0              | 113931.57       | 1      |
		+-----------+------------+----------+-------------+-----------+--------+-----+--------+----------+---------------+-----------+----------------+-----------------+--------+


Problem Statement

	- Based on the data, how can we create a model to predict if the customer will exit or will stay. 
	- This model can be applied to various scenarios where there are a lot of independent variables and where the out-come is variable. 

	
Building ANN Part 1 - What libraries to use and installating those libraries.
	
	- Theano - Opensource numerical computation library. Very effecient for fast numerical comutation , based on Numpy systax, can run not only on CPU but also GPU.
	- TensorFlow - Another Opensource numerical compurations library. Build Deep Nerural network from scratch using Theano and Tensor Flow. 
	- Keras - Based-on and wraps the functions of Theano and Tenorflow. Deep Neural Network using few lines of code.

	Installing Theano, TensorFlow and Keras
	- pip install theano
	- pip install tensorflow
	- pip install keras

	Upgrade the libraries to the most updaed version. 
	- conda update --all # this will update all the libraries in Anaconda and Spyder  

ANN part 2
	
	Part1 - Data PreProcessing
		- Use the DataPreProcessing - Classification template. 
		- Chose to correct Independent variables to make the matrix of features.
		- Who might be more likely to leave the bank. 
		- Credit Score, Geography, Gender, Age, Tenure, Balance, NumOfProducts, HasCard, isActiveMember, EstimatedSalary are the variables in the Dataset which make an impact if the person will leave or stay with the bank. These variables might an impact on finding out the Dependent variable. 
		- The ANN will try to figure out the relation between the Dependent variable from the independent variable. 
		- X stores all the variales on which the dependency is there. 
		- Y stores all the dependent variables. (this case only one, Exited or not) 

		- Before Splitting the dataset, the values in the dataset must already be encoded. We can see that there are two Values in the dependent variable which needs to be encoded. 
		- Create a dummy variable 

	Part2 - Building the Deeplearning Model.

