# Modeling Traffic Using the Nagel–Schreckenberg Model
#### Natalie Gray, Meredith Pritchard, Judah Byars, Inhyeok Cho, and Emma Horner

## Introduction
  ### Description: 
We plan to model the onset of traffic using the Nagel–Schreckenberg model, which is essentially a cellular automa model.

## Installation
Requirements: 

## Directory structure
`demo.ipynb`        contains a quick demonstration of the simulation and visualization  
`Lanes.ipynb` implements the one lane version of Nagel–Schreckenberg model and adds the multi-lane version with lane changing rules
`car_crash.py`   adds car crash capability to simulate lane closures  ????? are we gonna have this ??????
`results/`           directory for generated plots and CSV data  

## Numerical Approach
  ### Plan of implementation: (add update rules)

1. Create a length of l cells that are connected in a loop so that the first cell and last cell are connected and then we can randomly place several cars in the cells. Only one car to a cell. 
2. These cars will need to model acceleration and velocity so intially they can all be assigned a velocity between 1 and 5. After every iteration if there is enought room ahead of them (aka number of cells to move between them and the car ahead) they can move the number of cells their velocity has been set at and increase their velocity by 1 (acceleration) each iteration until they reach the max velocity.
3. If there isn't an option to move forward the correct number of cells then their velocity will decrease to the number of empty cells between them and the car in front of them.
4. The cars will also have randomization in their speed so will set all cars with >1 velocity will decrease 1 velocity with probability p. 
5. Then we will update all cars at the same time.

The additional layer we plan to add to this to add some complexity is another lane or two. Where if the car does not have enough spaces to move forward its velocity we check to see if it can do so in the lane beside it. If so, it will move over. If not, it will stay in its lane and follow the regular protocol. 

We also plan to add car crashes where if two cars are close to each other they have a small probability of crashing and holding up traffic in that lane for some finite amount of iterations. 

## Basic Usage
## Results Visualization
## Conclusion
## Applications
## Resources
## Credits

## Team Contributions

These are things that I forsee needing to be done, but feel free to add some to the list. I was thinking we could kind of just do this like a signup sheet. Multiple people could sign up for the same thing too and work together on it. 

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

## References:
https://www.mdpi.com/1424-8220/24/23/7672 -- might have some good images for the intro


