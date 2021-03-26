# GeneticAlgorithm_TSP_Demo
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/) &nbsp; 
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AbhishekSinghDhadwal/GeneticAlgorithm_TSP_Demo/blob/main/GA_TSP_Demonstration.ipynb)

A demo python implementation of genetic algorithms used in order to solve the Travelling Salesman Problem.
This notebook was created in order to provide a solution for the following problem statement as part of my CS department's Artificial Intelligence course:

*Problem statement* - Use genetic algorithms to solve the Traveling Salesperson Problem (TSP) on a large fully connected graph (about 50 nodes)

### Implementation Details :
The program is divided into the following sections -
* Input generation : Euclidean distances between points are generated by creating unique co-ordinates having values ranging from 1 to 1000 (both x and y) via the random library. This method is used in order to meet triangle inequality standards.
* Population creation : A member of the population is defined as a *random* sampling of all the city indices present, i.e a randomly generated route from city 0, traversing through all the cities, and returning to the city of origin itself.
* Fitness function : The fitness function is defined as the inverse of the total distance covered by a route.
* Crossover section : The random roulette method is used for selection of input. We perform ordered crossovers in the following manner -
    * We select a random subset from the first array.
    * We select all the elements not present in the subset and place them in the order stored in the second array.
* Main function : Runs the simulation as per input parameters.


For further details on implementation, refer the notebook.

### Instructions to run :
Open the [attached notebook](https://github.com/AbhishekSinghDhadwal/GeneticAlgorithm_TSP_Demo/blob/main/GA_TSP_Demonstration.ipynb)  in Google Colab, and press Ctrl + F9 to run all code snippets. The main function (last snippet) shall request the following details : 
Input parameter  | Description
------------- | -------------
numCities  | The number of vertices required
numPop  | The count of initial population
numGen | The number of generations the algorithm should run for
probMutation | The probability of mutation (default taken as 0.05)

#### Output information :
The program will provide input details, a randomly generated input graph along with the best fitness values (along with the respective best path and generation of occurence) and time taken to run the program.
It also plots down the best fitness values per generation as shown below:


![sampleGraph](https://user-images.githubusercontent.com/39513876/112625723-525b1f80-8e55-11eb-8d61-9d0cc8df75ee.PNG)

Note : This is a basic demonstration for a course project and not tested for production purposes. [Contact me](https://github.com/AbhishekSinghDhadwal) for corrections, feedback or suggestions!
