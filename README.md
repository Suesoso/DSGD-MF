# DSGD-MF

This is a python file to realize the distribtued stochastic gradient descent on Spark to solve matrix factorization problem in recommendation system.
Use following command to run the dsgd_mf.py file.

$spark-submit dsgd_mf.py <num_factors> <num_workers> <num_iterations> <beta_value> <lambda_value> <inputV_filepath> <outputW_filepath> <outputH_filepath>


