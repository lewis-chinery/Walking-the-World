# Sampling the World

Using a Random Walk Metropolis sampler and [data from Kaggle](https://www.kaggle.com/max-mind/world-cities-database), we attempt to randomly stumble our way across the entire world!

![](RWM_example_chain_animation.gif)

*Spoiler alert* - we approximate the world's population as a PDF and step our way about this space. As the spread of cities is quite sparse (on a global scale), the RWM chains we create find it hard to travel between continents and so we see above that the chains struggle to converge even after 10 hours runtime. 

### Significance of this work

This small project highlights some of the issues faced in Bayesian inference when trying to sample from an unknown, irregular posterior distribution. e.g. If we were to randomly initiate all of our chains in Africa, we might see after 10,000 iterations that they appear to be converging. However, if we were to then assume that we have successfully explored all posterior space (the whole world), we would of course be mistaken.

If we had more time and computing power, it would be interesting to run more RWM chains for longer preiods of time, tweaking the step size and city spread to see if we can obtain better and more efficient convergence.  Finally, we could also try out different Markov Chain Monte Carlo (MCMC) methods to see see if they provide better performance.
