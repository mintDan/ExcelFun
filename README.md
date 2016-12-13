#Analysis with Excel and VBA
This sections contains various different subjects.

1. [Path of mass through Action](https://github.com/mintDan/ExcelFun#path-of-mass-through-action)
2. [Ebola epidemic 2014-15 in Guinea](https://github.com/mintDan/ExcelFun#Ebola-epidemic-2014-2015-in-Guinea)


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

## Ebola epidemic 2014-15 in Guinea
The Ebola epidemic in Guinea is modelled with SIR, which used three time-dependent variables S(susceptibles), I(infectious), R(recovered). Data, which can be seen as R, is taken from WHO.

![Guinea.png](https://github.com/mintDan/ExcelFun/blob/master/figs/SIR.png)

The equations are solved in Excel with simple Euler integration.

![Guinea.png](https://github.com/mintDan/ExcelFun/blob/master/figs/Ebola.PNG)