# Adam-optimizer

I have implemented adam optimizer from scratch in python. I have assumed the stochastic function to be x^2 -4*x + 4.
I have referred the algorithm from "Adam: A Method for Stochastic Optimization" written by Diederik P. Kingma and Jimmy Ba.

First I have initialised all parameters like alpha, beta_1, beta_2, epsilon, theta_0, 1st moment vector, 2nd moment vector and timestep. Then I looped till the parameter vector(theta_0) is converged.

In the while loop, I have updated the timestep, got the gradient from the stochastic function, updated exponential moving averages of the gradient(m_t) and the average gradient(v_t) and calculated the bias-corrected estimates m_cap and v_cap. Finally, I updated the parameters(theta_0) and also kept a condition to check when the previous value of the inital parameter(theta_0) becomes equal to the new theta_0 and stopped the while loop at that point which means that it is converged. 

Adam uses an adaptive learning rate and is an efficent method for stochastic optimization which only requires first-order gradients with little memory requirement. It combines the advantages of Adagrad optimizer to deal with sparse gradients and the ability of RMSProp optimizer to deal with non-stationary objectives.  
