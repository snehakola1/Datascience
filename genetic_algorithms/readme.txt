tsp_genetic_algo.ipynb contains implementation of genetic algorithm for TSP problem. Tried implementation of different crossover functions(already existing and my own variations of already existing crossover operators). Compared those crossover functions by tuning the parameters. The parameters I have considered are populationsize, mutation rate, number of generations, elite rate. Considered two crossover operators order1Crossover, orderBasedCrossover as base operators and tried out slightly modified versions of them.
bestpick_order1Crossover : Instead of picking random subsequence of path from parent(that is done in order1Crossover), I tried to pick the smallest path from the parent.
bestpick_orderBasedCrossover : Instead of picking random indices to preserve from the parent, I choose the smallest k(a parameter that can be tuned) paths to preserve.
combinationCrossover : This is ensemble of crossovers which randomly chooses one of the above 4 crossovers to generate a child.
Implemented parallel 'for' loop for tuning of parameters as these runs are independent of each other.

From multiple runs, I have observed that GA with order1crossover  performs better than ant colony optimization solution.

However, it needs more analysis and tuning of parameter to compare the crossover functions and come up with the best crossover operator for the problem



Reference code taken from  
Implementaion of ga : https://towardsdatascience.com/evolution-of-a-salesman-a-complete-genetic-algorithm-tutorial-for-python-6fe5d2b3ca35
Ant colony optimization : https://github.com/ppoffice/ant-colony-tsp

