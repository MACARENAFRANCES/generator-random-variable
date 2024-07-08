# generator-random-variable
Generate and plot samples of Uniform, Normal, Binomial, and Exponential random variables using methods like LGM, Box-Muller, and Polar-Marsaglia. This is used to simulate, analyze data, and evaluate models under conditions of uncertainty.

## Uniform  
Generate 10,000 Uniformly distributed random number on [0,1] using LGM, compare with built-in python function. 

LGM empirical mean = 0.4996  
LGM empirical standard deviation = 0.2872  
Built-in empirical mean = 0.4987  
Built-in empirical standard deviation = : 0.2874  

My uniform random number generator using LGM method work as expected to generate 10,000 uniformly distributed number in [0,1]. However, the python built- in function is faster significantly. The mean and standard deviation from the two generators are approximately the same.  


## Part 2 - Binomial(n=44, p = 0.64)  
Binomial(n,p) is a sum of n Bernoulli(p). We first genrate Unform variable, then Bernoulli, then Binomial.   

Histogram  
<img width=“964” src="https://github.com/MACARENAFRANCES/generator-random-variable/blob/main/binom.png">


## Part 3 - Exponential(lambda = 1.5)  
Generating Exponentially distribution using the inverse transofrmation method, where we can generate a variate Y by inversing the distribution function. 

Histogram  
<img src="https://github.com/MACARENAFRANCES/generator-random-variable/blob/main/exp.png">

## Part 4 - Normal(0,1) with Box-Muller Method.  
Box-Muller Method can generate standard and independent Normal, given identically and independently distributed uniform random numbers. The method takes a continous two dimensional uniform distribution. **Box-Muller is significantly faster than Polar-Marsaglia methods in computation time.**  

Histogram  
<img width=“964” src="https://github.com/MACARENAFRANCES/generator-random-variable/blob/main/theorem.png">
<img width=“964” src="https://github.com/MACARENAFRANCES/generator-random-variable/blob/main/n1b.png">

## Part 5 - Normal(0,1) with Polar-Marsaglia Method. 
While Polar-Marsaglia method also generate independent stand Normal variables with uniforml random numbers, only approx 3/4 of times that generate the uniform variables: U1 and U2 will get the Normal variables: Z1 and Z2, hence the longer computation time. However, Polar-Marsaglia does not need to estiamte the sine and cosine functions in the Box-Muller method. 

Histogram  
<img width=“964” src="https://github.com/MACARENAFRANCES/generator-random-variable/blob/main/n2pl.png">
