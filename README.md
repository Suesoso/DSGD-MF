# DSGD-MF

This is a python file to realize the distribtued stochastic gradient descent on Spark to solve matrix factorization problem in recommendation system.
Use following command to run the dsgd_mf.py file.
```
$spark-submit dsgd_mf.py <num_factors> <num_workers> <num_iterations> <beta_value>
<lambda_value> <inputV_filepath> <outputW_filepath> <outputH_filepath>
```
Suppose you have a dataset V with m users and n movies, and hope to decompose V into W*H, W has m rows and num_factor columns, H has num_factor rows and n columns.

num_factors is number of factors, like, how many factors you want the two decomposed matrix W and H have.

num_workers is how many workers you can provide to parallel the algorithm.

num_iterations is how many epoches you hope the SGD perform on the whole dataset.

beta_value is the step size in SGD.

lambda_value is the coefficient of penalty in SGD.

