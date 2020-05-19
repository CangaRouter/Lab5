# Unit Testing Documentation template

Authors: Marco pappalardo

Date: 19/05/2020

Version: 1.0



# Contents

- [Black Box Unit Tests](#black-box-unit-tests-Ex-1)
- [Black Box Unit Tests](#black-box-unit-tests-Ex-2)
- [Black Box Unit Tests](#black-box-unit-tests-Ex-3)
- [Black Box Unit Tests](#black-box-unit-tests-Ex-4)

  

# Black Box Unit Tests Ex 1



### Method orderIntegers 



**Criteria for method  orderIntegers:**
	

- Lenght of the input array

- Type of data inside the array
  

**Predicates for method  orderIntegers:**

| Criteria                  | Predicate    |
| ------------------------- | ------------ |
|Lenght of the input array  |=3            |
|                           | >3           |
|                           | <3           |
|Data inside array          | Integer      |
|                           | not Integer  |




**Boundaries for method orderIntegers**:

| Criteria            | Boundary values             |
| ------------------- | --------------------------- |
| Lenght of the input | 3                           |
| Value of integers   | minInt, maxInt              |





 **Combination of predicates for method orderIntegers**

| Length of the array | Vality/Invality | Description of test case |  
| ------------- | -------------- | ------------- |
| < 3 | V | [5,6] , error |
|  | I | [515,H] , error |
|  |  | []  ,  error |
| > 3 | V | [1,2,3,4] , error |
|  | I | [2,2,6,T] , error |
| = 3 | V | [8,7,1] return 8, array [8,7,1] |
|  |  | [minint,0,maxint] return maxint, array [maxint,0,minint] |
|  | I | [0,0,I] , error|


# Black Box Unit Tests Ex 2



### Method acceptableToEat



**Criteria for method  acceptableToEat:**
	

- values of argument

- Type of data in arguments
  

**Predicates for method  acceptableToEat:**

| Criteria                  | Predicate      |
| ------------------------- | -------------- |
|values of argument         |>maxInt         |
|                           |<maxInt,>0 |
|                           | <0        |
|Type of data               | Integer        |
|                           | not Integer    |




**Boundaries for method acceptableToEat**:

| Criteria            | Boundary values             |
| ------------------- | --------------------------- |
| Value of arguments  | 0, maxInt                   |





 **Combination of predicates for method acceptableToEat**

| Length of the array | Vality/Invality | Result | Description of test case |  
| ------------- | -------------- |-----------| ------------- |
| > maxInt | I | error | (maxInt+1,10,25)|
|  | I |error| (515,maxInt+1,H)|
|<maxInt,>=0| V | true | (50,20,30)|
|  | V | false | (100,100,100)|
|  | I | error| (100,200,H)   |
| <0 | I |error| (8,7,-1)  |
|  | I |error| (8,H,-1)  |


# Black Box Unit Tests Ex 3



### Method parallelogram



**Criteria for method  parallelogram:**
	

- absolute values of argument
- relative values of argument (one with another)
- Type of data in arguments
  

**Predicates for method  parallelogram:**

| Criteria                  | Predicate      |
| ------------------------- | -------------- |
|values of argument         |>maxInt         |
|                           |<maxInt,>0 |
|                           | <0        |
|Type of data               | Integer        |
|                           | not Integer    |
| x1                        | >x2            |
|                           | <x2            |
| y1                        | >y3            |
|                           | <y3            |
| x3                        | >x4            |
|                           | <x4            |
| y2                        | >y4            |
|                           | <y4            |




**Boundaries for method parallelogram**:

| Criteria            | Boundary values             |
| ------------------- | --------------------------- |
| Value of arguments  | 0, maxInt                   |





 **Combination of predicates for method parallelogram**

| Range |Vality/Invality |P1| P2| P3| P4| Result | Description of test case |  
| ------------- | -------------- |-----|-----|-----|-----|-----------| ------------- |
|>maxInt |I |0,maxInt+1| 0,maxiInt+2 | 1,maxInt+1|1,maxInt+2| -1 | (0,maxInt+1, 0,maxiInt+2,1,maxInt+1,1,maxInt+2) |
| |I |H,maxInt+1| H,maxiInt+2 | 1,maxInt+1|1,maxInt+2| -1 | (0,maxInt+1, 1,0,0,1,1,1) |
|<maxInt,>=0| V |0,0| 1,0 | 0,1|1,1| 1 | (0,1, 1,0,0,1,1,1) |
|  | I |H,1| H,0 | 0,1|1,1| -1 | (H,1,H,0,0,1,1,1) |
|  | I |1,1| 0,0 | 1,2|2,2| -1 | (1,1,0,0,1,2,2,2) x1>x2 |
|  | I |0,1| 0,1 | 0,0|2,2| -1 | (0,1,0,1,0,0,2,2) y1>y3 |
|  | I |0,1| 0,1 | 1,2|0,2| -1 | (0,1,0,1,1,2,0,2) x3>x4 |
|  | I |0,1| 0,1 | 0,2|0,0| -1 | (0,1,0,1,0,2,0,0) y2>y4 |
| <0 | I |0,-1| 0,-1 | 0,2|1,2| -1 | (0,-1, 0,-1,1,2,1,2)   |
| | I |H,-1|H,-1 | 0,2|1,2| -1 | (H,-1, H,-1,0,2,1,2)   |

# Black Box Unit Tests Ex4


### Class Inventory 

**Criteria:**
- Unique identity code
- Availability item

**Predicates:**

| Criteria                  | Predicate    |
| ------------------------- | ------------ |
| Identity code | Unique |
| | Not unique or null |
| Availability item | > 0 |
|| = 0 |
|| < 0 |

**Boundaries**:

| Criteria            | Boundary values             |
| ------------------- | --------------------------- |
| Availability Item |  maxInt |
|| 0 |


 **Combination of predicates**

|  Identity code | Availability | Validity |Result| Description of test case |  
| ------------- | -------------- |-----| ------------- | ------------------ | 
| Not unique | <0 | I | NotExists| addItem(i) |
|  | >0 | I |NotExists | addiItem(i) |
| Unique | >0 | V |  | addiItem(i)  |
| | <0| I |NotAvailable |addiItem(i) |