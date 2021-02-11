# Walking the World

Using a Random Walk Metropolis (RWM) algorithm and [data from Kaggle](https://www.kaggle.com/max-mind/world-cities-database), we attempt to randomly stumble our way around the entire world!

![](RWM_example_chain_animation.gif)

*Spoiler alert* - we approximate the world's population as a 2D probability density function (PDF) and step our way around this space. As the spread of cities is quite sparse (on a global scale), the Markov chains we create find it hard to travel between continents and so we see above that the chains struggle to converge even after 10 hours runtime. 

### Significance of this project

This small project highlights some of the issues faced in Bayesian inference when trying to sample from an unknown, complex posterior distribution. e.g. If we were to happen to randomly initiate all of our Markov chains in Africa, we might see after 10,000 iterations that they appear to be converging. However, if we were to then assume that we have successfully explored all posterior space (the whole world), we would of course be mistaken.

If we had more time and computing power, it would be interesting to run more chains for longer preiods of time, tweaking the RWM step size and city spread to see if we can obtain better convergence. Finally, we could also try out different Markov chain Monte Carlo (MCMC) methods to see see if they provide better performance.
