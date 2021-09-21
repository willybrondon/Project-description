#Permeability Interpolation!

##Objectives:
The aim of this project was to predict the permeability value of an aquifer zone based on the available knowing permeability value. The result will be a permeability map. 
![image](https://user-images.githubusercontent.com/54869269/134154277-c196d133-2ed0-47d5-b7a8-cfac1fccd956.png)

##Technology:
The tools that has been is the language python with the libraries:
-Pandas, numpy, matplotlib, skgstat (variogram, krigring), scipy.

##Description
The method to accomplish this task is Kriging.
The knowing permeability value is on excel file. The excel file contain the coordinate value (longitude and latitude), permeability value, name the aquifer, permeability value converted.
In order to have the permeability map, data will be imported, then range of permeability value is selected to build a variogram. The variogram takes into account a model (Exponential, Spherical, Gaussian, Materm, and Cubic), an estimator (cressie), fit method (lm, trf, dogbox); it is a kind of optimization method, cell number.  The best variogram is based on the estimation of the parameters of the variogram so that the selected permeability value will highly correlate to the model (fit the shape of the model).
After the creation of the variogram, a grid is set up according to the maximum and minimum values of the permeability value. The interpolation of the permeability value is done on 2D grid with the variogram created and kriging method. As the result, a permeability map is obtained. The permeability value of the aquifer is known everywhere. This map can be used for simulation, to know where the heater water on the aquifer is.


