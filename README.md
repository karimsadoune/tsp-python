# tsp-python
## A Python Application That Use Genetic Algorithms To Solve Travelling Sale Probleme

We will use a **GA** to find a solution to the traveling salesman problem. this problem is described as follows: "Given the list of cities and the distances between each
pair of cities, what is the shortest possible route to visit each city and back to the city of origin? »

At this point there are two important rules:

1. Each city must be visited exactly once.
2. We have to return to the starting city, so our total distance should be calculated accordingly.
---
and as a general algorithm approach:
- *Gene*: a city (represented by the coordinates (x, y))
- Individual (or “chromosome”): a single pathway meeting the above conditions
- *Population*: a set of possible pathways (i.e. a set of individuals)
- *Parents*: two routes combined to create a new route
- *Mating pool*: a set of parents that are used to create our next population (thus creating the next generation of roads)
- *Fitness*: a function that tells us how well each route is
good (in our case, how short the distance)
- *Mutation*: a way to introduce variations in our population
by randomly swapping two cities in a route
- *Elitism*: a way to carry the best individuals into the next generation
---
The **GA class** to bring together all the methods related to the genetic algorithm.
- crossover(): Returns a child route of **Route()** after reproducing the routes of both parents. Routes must be the same length.
- mutate(): Exchange two random indexes in **route_to_mut.route**
- tournament_select(): Randomly select tournament size
tournament_size an amount of **Routes()** from the input population. Takes the strongest of the smallest number of **Routes()**.
---
The **app1 class** create a *UI* using **Tkinter**
