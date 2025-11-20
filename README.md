# Modeling Traffic Using the Nagel–Schreckenberg Model
#### Natalie Gray, Meredith Pritchard, Judah Byars, Inhyeok Cho, and Emma Horner

## Introduction
  ### Description: 
We plan to model the onset of traffic using the Nagel–Schreckenberg model, which is essentially a cellular automa model.

- figure
- equation??? <img width="887" height="678" alt="Screenshot 2025-11-20 at 1 42 40 PM" src="https://github.com/user-attachments/assets/e307524f-5c4b-4019-8a21-c0d8ff0091d3" />
Figure adapted from Liang et al., 2024.

## Installation
Requirements: 
```
pip install numpy
pip install matplotlib
```

## Implementation
### Single lane implementation:
  First we implement a model for single lane traffic. The rules are.......

1. Create a length of l cells that are connected in a loop so that the first cell and last cell are connected and then we can randomly place several cars in the cells. Only one car to a cell. 
2. These cars will need to model acceleration and velocity so intially they can all be assigned a velocity between 1 and 5. After every iteration if there is enought room ahead of them (aka number of cells to move between them and the car ahead) they can move the number of cells their velocity has been set at and increase their velocity by 1 (acceleration) each iteration until they reach the max velocity.
3. If there isn't an option to move forward the correct number of cells then their velocity will decrease to the number of empty cells between them and the car in front of them.
4. The cars will also have randomization in their speed so will set all cars with >1 velocity will decrease 1 velocity with probability p. 
5. Then we will update all cars at the same time.

The additional layer we plan to add to this to add some complexity is another lane or two. Where if the car does not have enough spaces to move forward its velocity we check to see if it can do so in the lane beside it. If so, it will move over. If not, it will stay in its lane and follow the regular protocol. 

We also plan to add car crashes where if two cars are close to each other they have a small probability of crashing and holding up traffic in that lane for some finite amount of iterations. 

1. Acceleration: All cars not at the maximum velocity have their velocity increased by one unit. For example, if the velocity is 4 it is increased to 5.

2. Slowing down: All cars are checked to see if the distance between it and the car in front (in units of cells) is smaller than its current velocity (which has units of cells per time step). If the distance is smaller than the velocity, the velocity is reduced to the number of empty cells in front of the car – to avoid a collision. For example, if the velocity of a car is now 5, but there are only 3 free cells in front of it, with the fourth cell occupied by another car, the car velocity is reduced to 3.

3. Randomization: The speed of all cars that have a velocity of at least 1, is now reduced by one unit with a probability of p. For example, if p = 0.5, then if the velocity is 4, it is reduced to 3 50% of the time.

4. Car motion: Finally, all cars are moved forward the number of cells equal to their velocity. For example, if the velocity is 3, the car is moved forward 3 cells.

### Multiple lane implementation: 
Next we add multiple lanes to our model. RUles...

## Results Visualization
- To visualize the results, .... 

## Conclusion
- In conclusion, ....

## Applications
- some applicatoins of this model could be....

## Team Contributions
1. Creating the project proposal: 
Natalie
2. Creating the project READme (not this one the real one):
Emma, Meredith
3. Implementing the basic level of code (1 lane of traffic):
Natalie
4. Implementing the multiple lanes:
Judah
5. Car Crashes and their minimization
Inhyeok
6. Creating some way to show the results:
Judah
7. Making the Presentation:
Meredith, Emma
8. We will all presesnt:
Natalie, Emma, Meredith, Inhyeok, Judah

## Resources:
https://www.mdpi.com/1424-8220/24/23/7672 -- might have some good images for the intro


