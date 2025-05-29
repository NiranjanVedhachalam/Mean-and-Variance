NAME: NIRANJAN V

REG NO: 212224110042

#  EX - 01 Mean and variance of a discrete  distribution


# Aim : 

To find mean and variance of arrival of objects from the feeder using probability distribution


# Software required :  

Python and Visual components tool

# Theory:

The expectation or the mean of a discrete random variable is a weighted average of all possible
values of the random variable. The weights are the probabilities associated with the corresponding values. 
It is calculated as,

![image](https://user-images.githubusercontent.com/103921593/192938463-e34177f4-f188-48a0-bda2-8f6d1d660ed2.png)

The variance of a random variable shows the variability or the scatterings of the random variables.
It shows the distance of a random variable from its mean. It is calcualted as

![image](https://user-images.githubusercontent.com/103921593/192938695-99fedc01-34d5-4d36-84df-5880e766ed0c.png)


# Procedure :

1. Construct frequency distribution for the data

2. Find the  probability distribution from frequency distribution.

3. Calculate mean using 
   
   ![image](https://user-images.githubusercontent.com/103921593/192940431-03b81777-c54d-4286-b4f4-82dfe7666b4c.png)

4. Find  
   
      ![image](https://user-images.githubusercontent.com/103921593/192940255-2d9dd746-6875-4a6d-877b-6da6cdb96ab1.png)

5.  Calculate variance using 
  
      ![image](https://user-images.githubusercontent.com/103921593/192942852-913550a9-fabe-4a55-b956-0487b18bbd97.png)


# Experiment :

![image](https://user-images.githubusercontent.com/103921593/229993174-5b67e57e-3e01-4ac4-9f83-410a932b22bf.png)

# Program :

```
import numpy as np
list1=[int(i) for i in input().split()]
O=len(list1); P=max(list1) 
R=list();T=list()
for i in range (P+1):
    c = 0
    for j in range(O):
        if list1[j]==i:
            c=c+1
    T.append(c)
    R.append(i)
sT=np.sum(T)
p=list()
for i in range(P+1):
    p.append(T[i]/sT) 
mean=np.inner(R,p)
EX2=np.inner(np.square(R),p)
var=EX2-mean**2 
SD=np.sqrt(var)
print("The Mean arrival arate is %.3f "%mean)
print("The Variance of arrival from feeder is %.3f "%var) 
print("The Standard deviation of arrival from feeder is %.3F "%SD)
```

# Output : 

![Screenshot 2025-05-02 134730](https://github.com/user-attachments/assets/7d859a34-0af0-4d8c-81a1-0c08e81f1114)

# Results :
The mean and variance of arrivals of objects from feeder using probability distribution are calculated.

