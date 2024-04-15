# Genetic algorithm for protein engineering
In silico protein engineering using Genetic Algorithms and rosetta energy calculations

genetic_algorithm.py = contains main function
apt_functions.py = contains a collection of objective functions for the genetic algorithm

GAprot.py imports genetic_algorithmpy and apt_functions.py, configures initial population and carries out the optimization

-Threads not supported yet

### GA function

genetic_algo(pose=starting_pose, opt_direction='down', gene_values=gene_values, gene_type='discrete', 
             vector_size=len(starting_pose_seq), pop_size=len(init_pop), mutation_rate=0.2, segment_fluctuation=0, 
             apt_function=apt, selection_method='tournament', threads=False,
             convergence_threshold=0, n_cycles=20, n_survivors=1, tournament_size=4,
             initial_population=init_pop, file_name="cond_1.txt", dg_method="fold")
             
  pose = starting PDB structure
  
  opt_direction = selects if the objective function goes up or down
  
  gene_values = Values that vectors can assume
  
  gene_type = Selects between discrete or continuous genes
  
  vector_size = size of the vectors
  
  selection methods = elitist or tournament selection
  
  threahds = parallel processing (not supported)
  
  n_cycles = number of optimization cycles
  
  n_survivor = number of survivors in each selection
  
  tournament_size =number of individuals selected in each tournament
  
  initial_population = An initial population can be given. Otherwise, a random population is created

  file_name= output log file, Sequences - dG - population
  
  dg_method = select between "fold" and "bind".

# Installing dependencies

## Getting started

First of all, you must download PyRosetta. To download , you need to get a license.
<br />
License and Downloads links:
<br />
[License](https://www.rosettacommons.org/software/license-and-download)
<br />
[PyRosetta4 Download](https://graylab.jhu.edu/download/PyRosetta4/archive/release/)



## Installing PyRosetta
### After downloading, unzip PyRosetta's and enter the setup directory to install it
```
tar -xvf PyRosetta[release].tar.bz2
cd PyRosetta*/setup
python3 setup.py install
```

## Installing aditional Python libs
```
pip install pandas
pip install numpy
```

Additional help for downloading and installing and PyRosetta (source:Sari Sabban youtube channel )

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/UEaFmUMEL9c/0.jpg)](https://www.youtube.com/watch?v=UEaFmUMEL9c)

