# PLC Project:  Traffic Light


## Objective
Design a traffic light system to control car flow on a crossroad. 

## Design Importance

![1](https://user-images.githubusercontent.com/86275885/122995045-74ded500-d37f-11eb-9cea-d3721a0a1a35.jpg)


In areas where there is a conjunction on crowded highways, there is a major problem in traffic organization. Numerous life-taking car accidents happen because of this issue. As shown in the conceptual picture, when an efficient traffic organization is missing, cars crashes are most likely to occur.


![2](https://user-images.githubusercontent.com/86275885/122995120-90e27680-d37f-11eb-85cf-ccf1be5fcae9.jpg)


The solution for this major problem is to design an efficient traffic light controller capable of controlling traffic so that everyone can pass safely. The turn problem should be solved as well. A great solution is to insert a traffic light controller specifically intended for turns, this way the system will be fully effective.

![4](https://user-images.githubusercontent.com/86275885/122995240-bc656100-d37f-11eb-8817-d01702e7b2e8.jpg)


## Design Components


![1](https://user-images.githubusercontent.com/86275885/122995348-e4ed5b00-d37f-11eb-8de1-9122167d56a2.png)
![2](https://user-images.githubusercontent.com/86275885/122995351-e585f180-d37f-11eb-9ddb-0b81fb2e6b3e.png)
![3](https://user-images.githubusercontent.com/86275885/122995352-e585f180-d37f-11eb-8b12-cb024fcab353.png)
![4](https://user-images.githubusercontent.com/86275885/122995353-e585f180-d37f-11eb-890b-99682aa5f0a2.png)


## Design Logic
![5](https://user-images.githubusercontent.com/86275885/122995446-00f0fc80-d380-11eb-861f-f308e031bd7d.png)

-	State 1: For 15 seconds, we have green A and green Arrow A as well as red on CD and red on B
-	State 2: For 10 seconds, we have green A and yellow Arrow A as well as red on CD and red on B
-	State 3: For 15 seconds, we have green A and B, red on CD
-	State 4: For 10 seconds, we then have yellow A and B, red on CD
-	State 5: For 15 seconds, we have red on A and B, green on CD
-	State 6: For 10 seconds, we have red on A and B, yellow on CD and then the cycle restarts again with state 1 if no car was detected previously on green lights CD.
-	State 7: For 15 seconds, when a car has been detected on green lights CD, the green arrow CD will turn ON.
-	State 8: For 10 seconds, yellow arrow CD turns ON and green arrow CD is OFF. At the end of these 10 seconds, the state machine returns to state 1. 


## Conclusion
This project implemented a state machine which taught us how to create several states and design a mechanism to link all of them. It allowed us to dynamically draw a pattern between the different situations and how to control them efficiently. 



