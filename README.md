# _[COMPLETED]_
# Neuroevolution-GeneticAlgorithm_Snake-Problem

In this Notebook I propose a neuroevolutionary approach to the classical Snake game,
which combines a neural network with a genetic algorithm to find the best individuals, 
where an individual is a list of weights that are passed to the network.

The genetic algorithm uses:
<br>
-two-point crossover with probability 0.2,<br>
-mutation adding or subtracting float values drawn from a Gaussian distribution<br>
with mean=0, std=0.4 and individual weight change probability=0.01<br>
-roulette wheel selection<br>
-custom fitness function: 30log(steps+1)) + (steps/2) + (food*500) - (((0.1*penalty)**1.3)*(food**1.2))<br>
where <br>
steps=number of steps in the correct direction, <br>
food=amount of food eaten,<br>
penalty=sum of steps in the wrong direction with penalty if snake dies<br>
-population size of 150<br>
-2000 generations (but can be adjusted to increase score)<br>
  <br>
I use a feed-forward network with 18 nodes in both the first and second layer.
