# DSGD-MF

This is a python file to realize the distribtued stochastic gradient descent on Spark to solve matrix factorization problem in recommendation system.
Use following command to run the dsgd_mf.py file.
```
$spark-submit dsgd_mf.py <num_factors> <num_workers> <num_iterations> <beta_value>
<lambda_value> <inputV_filepath> <outputW_filepath> <outputH_filepath>
```
num_factors is number of factors, that is, how many factors you want the two decomposed matrix W and H have.

num_workers is how many workers you can provide to parallel the algorithm.

num_iterations is how many epoches you hope the SGD perform on the whole dataset.

beta_value is the step size in SGD.

lambda_value is the coefficient of penalty in SGD.

As an example, if you have a dataset V with m users and n movies, and hope to decompose V into W*H, W has m rows and 100 columns, H has 100 rows and n columns, the num_factor is 100. You have 10 slaves to parallel work, and hope to iterate the algorithm on the whole dataset for 50 times, the step size in SGD is 0.8, weight of penalty term is 1.0, input dataset name is test.csv, output name of W is w.csv, output name of V is v.csv, then your code will be:
```
spark-submit dsgd_mf.py 100 10 50 0.8 1.0 test.csv w.csv h.csv
```

Created by Susu Xu; xssthu at gmail dot com; Apr 16th 2015.
