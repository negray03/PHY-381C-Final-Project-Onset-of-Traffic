# PHY-381C-Final-Project-Onset-of-Traffic

## Description: 
We plan to model the onset of traffic using the Nagel–Schreckenberg_model which is essentially a cellular automa model.

## Directory structure

Maybe a demo section that shows some the oscilatory nature 
A directory for the main code with a sub-directory for the code of additional lanes of traffic
Another folder for the results

I am very open to changes here this was a potential rough outline

## Plan of implementation:

1. Create a length of cells that are in a loop and the first cell and last cell are also connected and place several cars in the cells. Only one car to a cell. 
2. These cars will need to model acceleration and velocity so intial they can all be assigned a velocity between 1 and 5 after every iteration if there is enought room ahead of them (aka nuber of cells to move) they can move the number of cells their velocity has been set at and increase their velocity by 1 (acceleration) until they reach the max velocity.
3. If there isn't an option to move forward the number of cells then their velocity will decrease to the number of empty cells between them and the car in front of them.
4. The cars will also have randomization in their speed so will set all cars with >1 velocity will decrease 1 velocity with probability p. 
5. Then we will update all cars at the same time.

The additional layer we plan to add to this to add some complexity is another lane or two. Where if the car does not have enough spaces to move forward its velocity we check to see if it can do so in the lane beside it. If so, it will move over. If not, it will stay in its lane and follow the regular protocol. 

## Team Contributions

These are things that I forsee needing to be done, but feel free to add some to the list. I was thinking we could kind of just do this like a signup sheet. Multiple people could sign up for the same thing too and work together on it. 

1. Creating the project READme (not this one the real one)

2. Implementing the basic level of code (1 lane of traffic)
Natalie
3. Implementing the multiple lanes

4. Creating some way to show the results

5. Making the Presentation 

6. I am assuming we will all presesnt unless one of us can't be there
Natalie



