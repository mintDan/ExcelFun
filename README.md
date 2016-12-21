#Analysis with Excel and VBA
This sections contains various different subjects.

1. [Path of mass through Action](https://github.com/mintDan/ExcelFun#path-of-mass-through-action)
2. [Ebola epidemic 2014-15 in Sierra Leone](https://github.com/mintDan/ExcelFun#ebola-epidemic-2014-15-in-sierra-leone)
3. [Water tank animation](https://github.com/mintDan/ExcelFun#water-tank-animation)
4. [Tournament](https://github.com/mintDan/ExcelFun#tournament)

## Path of mass through Action
The Excel sheet calculates the path of a thrown mass, in the single vertical dimension. Pressing "Vary Height" will change the object height, and calculate the action S. The true path of an object minimizes the Action integral S.

![Sint.png](https://github.com/mintDan/ExcelFun/blob/master/figs/Sint.png)

The Lagrangian L is given by L=T-V. Discretization of the Lagrangian gives

![Lapprox.png](https://github.com/mintDan/ExcelFun/blob/master/figs/Lapprox.png)

Which gives the discrete Action

![Sapprox.png](https://github.com/mintDan/ExcelFun/blob/master/figs/Sapprox.png)

Varying the path leads to different Actions, and varying w.r.t each node on the grid, gives an explicit linear system of equations.

![Svary.png](https://github.com/mintDan/ExcelFun/blob/master/figs/Svary.png)

Screenshot of the spreadsheet is seen here with the button that starts the process.

![Sheet.png](https://github.com/mintDan/ExcelFun/blob/master/figs/Sheet.PNG)

## Ebola epidemic 2014-15 in Sierra Leone
The Ebola epidemic in Sierra Leone is modelled with SIR, which used three time-dependent variables S(susceptibles), I(infectious), R(recovered). Data, which can be seen as R, is taken from WHO.

![Guinea.png](https://github.com/mintDan/ExcelFun/blob/master/figs/SIR.png)

The equations are solved in Excel with simple Euler integration.

![Guinea.png](https://github.com/mintDan/ExcelFun/blob/master/figs/Ebola.PNG)


## Water tank animation
This is an animation of water pouring out of a water tank. The system is described by Torricelli's law and mass conservation. Mass conservation is given by

![Wt.png](https://github.com/mintDan/ExcelFun/blob/master/figs/WTmass.PNG)
The water flowing covers a certain area pr time unit, which is assumed constant. By Torricelli's law we have

![Wt.png](https://github.com/mintDan/ExcelFun/blob/master/figs/WTvout.PNG)
Which can then be used to calculate the change in the height of water tank. The change in height of the water tank will then change the velocity out of the tank due to the lowered pressure. Hence we can solve the system iteratively.

![Wt.png](https://github.com/mintDan/ExcelFun/blob/master/figs/WTh.PNG)

The Excel sheet animates the system. It can be seen that the water flow out weakens with time, as the pressure falls. It can also be seen that the change in water height w.r.t time also becomes slower, due to velocity out getting weaker.
![Wt.png](https://github.com/mintDan/ExcelFun/blob/master/figs/Watertank.PNG)

## Tournament
In a round-robin tournament every player meets every other player, and in this case a player either wins or loses. This can be represented as a directed graph.

![Sheet.png](https://github.com/mintDan/ExcelFun/blob/master/figs/Tourney.png =100x20)

In this case, player a beats b,c and e, and player c only beats player d and e. Counting the number of wins, a has 3 wins, b has 1, c has 2, d has 3 wins and e has 1 win. 
So the problem is who wins, a or d? and who is third and fourth? This can be solved by looking at the adjacency matrix for the graph, and calculating the power series.
The adjacency matrix is

![Sheet.png](https://github.com/mintDan/ExcelFun/blob/master/figs/AdjMatrix.png)

Column order is (c,e,d,b,a) and likewise with rows. Row one means that c beat e and d, hence there's 1 in those entries, and 0 in the rest.
The way to figure out the winners is then by calculating the matrix B and summing up with rows.

![Sheet.png](https://github.com/mintDan/ExcelFun/blob/master/figs/BMatrix.png)

The calculation is done here and we can see the winner is d.

![Sheet.png](https://github.com/mintDan/ExcelFun/blob/master/figs/TSheet.PNG)