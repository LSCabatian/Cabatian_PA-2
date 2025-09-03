Normalization Problem
``` python
#Import numerical python Library
import numpy as np

#Create random 5x5 array
X = np. random. rand(5, 5)

#Function for Normalized Values
Z = (X - X.mean()) /X.std()

#save Normalized values as X_nomatized. ny
np. save("X_normalized.npy", Z)

#Print X and Z
print ("Original Value: \n", X, "\n Normalized Value: \n", Z)
#end

Original Value: 
 [[0.46086187 0.84715866 0.25929357 0.93914511 0.96556181]
 [0.41596598 0.83260649 0.18402485 0.51945112 0.51266944]
 [0.55735762 0.87197792 0.58047002 0.72199439 0.10709104]
 [0.29896503 0.83882289 0.46014752 0.32504504 0.65463942]
 [0.35445968 0.092665   0.48369713 0.77633538 0.30893073]] 
 Normalized Value: 
 [[-0.2885077   1.21936853 -1.0753122   1.5784297   1.68154503]
 [-0.46375493  1.16256538 -1.36911718 -0.05980963 -0.08628134]
 [ 0.08815514  1.31624838  0.17837239  0.73080058 -1.66942168]
 [-0.92045809  1.18683059 -0.29129614 -0.81865701  0.46788625]
 [-0.70383948 -1.7257325  -0.19937223  0.94291595 -0.88155782]]
```
Divisible by 3 Problem
``` python
import numpy as np

#Create an array of the first 100 positive integers
n = np.arange(1,101)

#Square every element
A_squared = np.square(n)

#Resize into a 10x10 ndarray
A = A_squared.reshape(10,10)

#Determine the elements divisible by 3
Div_by_3 = A[A % 3 == 0]

#Save the result as div_by_3.npy
np.save('div_by_3.npy', Div_by_3)

#Print the output of "A" and "div_by_3"
print("A =\n", A, "\nElements divisible by 3:\n", Div_by_3)

A =
 [[    1     4     9    16    25    36    49    64    81   100]
 [  121   144   169   196   225   256   289   324   361   400]
 [  441   484   529   576   625   676   729   784   841   900]
 [  961  1024  1089  1156  1225  1296  1369  1444  1521  1600]
 [ 1681  1764  1849  1936  2025  2116  2209  2304  2401  2500]
 [ 2601  2704  2809  2916  3025  3136  3249  3364  3481  3600]
 [ 3721  3844  3969  4096  4225  4356  4489  4624  4761  4900]
 [ 5041  5184  5329  5476  5625  5776  5929  6084  6241  6400]
 [ 6561  6724  6889  7056  7225  7396  7569  7744  7921  8100]
 [ 8281  8464  8649  8836  9025  9216  9409  9604  9801 10000]] 
Elements divisible by 3:
 [   9   36   81  144  225  324  441  576  729  900 1089 1296 1521 1764
 2025 2304 2601 2916 3249 3600 3969 4356 4761 5184 5625 6084 6561 7056
 7569 8100 8649 9216 9801]
