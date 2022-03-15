EE 134: Graph Theory in Engineering

1 Project Description


Congratulations! your project is selected by the company X to support sensor deployment in a
jungle with the purpose of monitoring wildlife. However, apart from providing your suggested
optimal sensor placement, the company asks some additional help from you. In particular, X plans
to use drones to drop the sensors to the locations your scheme designated on the map, and wants
your help on planning the routes of the drones. You are asked to work out two scenarios:
Scenario 1. The company will use a large drone that can carry all the sensors; however, this drone
consumes fuel fast, and thus it is important to minimize the total travel distance of the drone. The
drone will start from a drone station at the center of the map (where the receiver/sink will be),
and needs to return to the same point. Moreover, because it is a large drone, as it flies above a
square x, it can simultaneously drop sensors not only on the square x but also on all neighboring
squares inside a 5 ˆ 5 square with center x.


Scenario 2. The company will use multiple drones, that are smaller and need to obey the following
restrictions:
• Each drone can carry up to 300 sensors at a time.
• Drones depart again from the central node (sink) and can fly to any location on the map
even across blocked areas, however, due to fuel constraints, each of these drones can travel a
distance of at most 1100 units (counting the return distance) and then it needs to return to
the central node to refuel.
• X has only M drones that can be used for deployment.
Goals.
For Scenario 1: Find the shortest route for the drone in terms of distance.
For Scenario 2: Design the routes of the M drones that minimize the total deployment time
assuming that all drones fly at speed 1 unit/second.
In both cases, to reduce the computational complexity, instead of finding the optimal routes, you
can design approximation algorithms.
Input. We will be given the designated locations where the sensors need to be placed. For
simplicity, we assume that the area is divided into a grid of squares with side 1 unit. If you wish,
you are allowed to slightly pertube the location of the sensor nodes, provided that the worst case
min-cut does not reduce by more than 5% and that the sensing coverage also does not reduce by
more than 5%.
You are also allowed to use the locations that you have from project 1 (or any new placement)
provided that the coverage does not drop below 85% and the worst case minimum cut does not
drop below 3.
2 Map
We will use the same 300x300 map as in Project 1. The map is a black and white image which
we represent as 2-D array. The elements of the arrays take the value 0 or 1, with 1 representing a
pixel of an unobstructed area and 0 representing a pixel of an obstructed area.
In addition to the map array, we provide a placement array which has the same size as the map and
each entry takes the value 0 or 1, with 1 representing a designated sensor location and 0 representing
no sensor. Recall that, if you wish, you can change this array as described in the previous section.
The distance between two adjacent elements in the same row or same column of the array is assumed
to be unity.
3 What to submit
Please fill in the attached notebook the following functions/cells:
• single route: A function that finds the route of the big drone in scenario 1.
• routes: A function that designs the paths for the M sensors to minimize the total deployment
time.
• simplify graph: Optional function to simplify the graph by ignoring some links to reduce
the complexity of solving the problem without highly affecting the deployment time.
• Plots: A figure plotting the number of drones vs the total deployment time for number of
drones M in t1, 3, 5, 8, 10u.
You should submit a zip file containing the following items:
2. For scenario 1, report the achieved total distance and plot the trajectory of the drone.
3. For scenario 2, report the optimal deployment ratio (min [deployment time/number of drones]).
4. A figure plotting the number of drones vs the total deployment time for number of drones
in t1, 3, 5, 8, 10u, for scenario 2. Please plot also the
trajectories of the drones. (5 points)
5. The python code. 
