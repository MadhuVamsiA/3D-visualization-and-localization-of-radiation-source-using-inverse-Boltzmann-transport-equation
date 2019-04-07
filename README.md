# 3D-visualization-and-localization-of-radiation-source-using-inverse-Boltzmann-transport-equation
Occupational workers carry wearable sensors for radiation dose data logging, datasets are generated due to movement of workers. A computer code running on GPU/CPU is required which can solve reverse Boltzman Transport Equations (BTE) in offline mode using collected datasets (X,Y,Z,Dose) for given area &amp; do 3D visualization of radiation source in that area. Radiation protection program can take corrective measures for removal of unwanted sources.
We have designed a gpu/cpu code to find out the missing source using given area dose.
we have used three approaches
1. K- Nearest Neighbour (KNN) 
2. Analytical 
3. Visulization 

KNN approach:
We have wriiten code for KNN approach in matlab for given dataset.
KNN folder consits of code and results of 1D,2D and 3D visulization (in both fig and png format)
In this approach we are visulizing the given data set according to their intensity of dose that it received at a point (xi,yi,zi)
The K nearest points from the source location will receive the highest dose than other. The points which are too far from the source location will recive less intensity of dose. Such that, the source will be located nearer to the points which are having high intensity of dose.
In results of KNN it was showed that the points nearer to source are darker in color than points far away from source. In this way we can find the location and geomentry of any given source.


Analytical approach:
We have written code for Analytical approach in MATLAB for given dataset.
We are considering that source is made up of n points and trying to find these n points location.
In our dataset we have considered n target points (points that recive dose from source) and calculated n linear equations from these points to source (made up of n points) which have 'n' unknow variables. By solving these n equations we can get the values for these 'n' unknows variables which gives the co-ordinates of these 'n' points.

Visulization approach:
From the formula of linear Boltzmann transport equation it was clear that the source and target points are separeted by distance D (radius). So, if we have drawn spheres from each n target points with radius 'r' (r is the distance between source and target points) all these spheres will intersect at a common region where the source is located at. 
