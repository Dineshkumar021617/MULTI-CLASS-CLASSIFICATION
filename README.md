### Ex No: 03
### Date:
# <p align="center">MULTI-CLASS-CLASSIFICATION</p>
## Aim:
To write a python program to implement the multi class classification algorithm .

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner / Google Colab

## Related Theoritical Concept:
In multi-class classification, the neural network has the same number of output nodes as the number of classes. Each output node belongs to some class and outputs a score for that class. Class is a category for example Predicting animal class from an animal image is an example of multi-class classification, where each animal can belong to only one category.

## Algorithm
1. Import the necessary modules
2. Frame the dataset using make_blobs
3. Assign the counter value using the Counter function
4. Using a for loop, plot the points using scatter function

## Program:
```
/*
Program to implement the multi class classifier.
Developed by: Dineshkumar.S
RegisterNumber:  212220230012
*/
from numpy import where
from collections import Counter
from sklearn.datasets import make_blobs
from matplotlib import pyplot
x,y=make_blobs(n_samples=1000,centers=3,random_state=1)
print(x.shape,y.shape)
counter=Counter(y)
print(counter)
for i in range(10):
    print(x[i],y[i])
for label, _ in counter.items():
    row_ix = where(y==label)[0]
    pyplot.scatter(x[row_ix,0],x[row_ix,1],label=str(label))
    pyplot.legend()
```

## Output:
![Screenshot (42)](https://user-images.githubusercontent.com/75234807/165561249-53674d19-7039-4324-848f-8dba380d0632.png)


## Result:
Thus the python program to implement the multi class classification was implemented successfully.
