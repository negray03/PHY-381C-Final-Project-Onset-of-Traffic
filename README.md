# Modeling Traffic Using the Nagel–Schreckenberg Model
#### Natalie Gray, Meredith Pritchard, Judah Byars, Inhyeok Cho, and Emma Horner

## Introduction
  ### Description: 
We plan to model the onset of traffic using the Nagel–Schreckenberg model, which is essentially a cellular automa model.

- figure
- equation???
  
## Installation
Requirements: 
```
pip install numpy
pip install matplotlib
```

## Implementation
### Single lane implementation:
First we implement a model for single lane traffic as our baselilne/starting point.  The road is represented by a 1D array where each position represents a “cell” or location in which a car could occupy.

We then randomly place several cars into the cells and each cell is assigned a numerical value: 

    - $v = -1$     → cell is empty, no car occupies that cell
    - $v = 0-5$     → cell has a car with velocity $0-5$

With these as the inititail conditions, we iterate over various time steps and the simulation evovles according to the following rules for car motion, including acceleration, slowing down, and randomization. 

1. Car motion: Finally, all cars are moved forward the number of cells equal to their velocity. For example, if the velocity is $v = 3$, the car is moved forward $3$ cells.
2. Acceleration: All cars not at the maximum velocity have their velocity increased by one unit. For example, if the velocity is $v = 4$ it is increased to $5$.
3. Slowing down: All cars are checked to see if the distance between it and the car in front (in units of cells) is smaller than its current velocity (which has units of cells per time step). If the distance is smaller than the velocity, the velocity is reduced to the number of empty cells in front of the car – to avoid a collision. For example, if the velocity of a car is now 5, but there are only 3 free cells in front of it, with the fourth cell occupied by another car, the car velocity is reduced to 3.
4. Randomization: The speed of all cars that have a velocity of at least 1, is now reduced by one unit with a probability of p. For example, if $p = 0.5$, then if the velocity is 4, it is reduced to 3 50% of the time.


### Multiple lane implementation: 
Next we add multiple lanes to our model. RUles...

## Results Visualization
- To visualize the results, .... 

## Conclusion
- In conclusion, ....

## Applications
- some applicatoins of this model could be....

## Authors and Acknowledgments
This project was completed by Natalie Gray, Meredith Pritchard, Judah Byars, Inhyeok Cho, and Emma Horner. We want to acknowledge and thank Professor William Gilpin and Carson McVay for their support and wisdom LOL

## Resources:
https://www.mdpi.com/1424-8220/24/23/7672 -- might have some good images for the intro


