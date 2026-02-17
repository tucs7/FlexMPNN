# FlexMPNN 

FlexMPNN is a framework for ensemble-conditioned inverse folding inference using conformational ensembles generated via rigidity-theory–based constrained geometric simulations

# Installation steps

* Install ProteinMPNN fallowing steps described in

```
https://github.com/dauparas/ProteinMPNN
```

# Usage

To perform inference using ensembles run

```
  ./ensemble_inference.sh

```



# Data

* Includes three biomolecule landscapes:
  + RNA ligase ribozyme: R. Rotrattanadumrong and Y. Yokobayashi, “Experimental exploration of a ribozyme neutral
network using evolutionary algorithm and deep learning,” Nat. Commun., vol. 13, p. 4847, 2022
  + Fluorescent protein: F. J. Poelwijk, M. Socolich, and R. Ranganathan, “Learning the pattern of epistasis linking
genotype and phenotype in a protein,” Nat. Commun., vol. 10, p. 4213, 2019
  + Anti-influenza antibody: A. M. Phillips, K. R. Lawrence, A. Moulana, T. Dupic, J. Chang, M. S. Johnson, I. Cvijovic,
T. Mora, A. M. Walczak, and M. M. Desai, “Binding affinity landscapes constrain the evolution
of broadly neutralizing anti-influenza antibodies,” eLife, vol. 10:e71393, 2021
* All above are stored in the /data

# Usage

* Example run:
```
python FMIRA.py -f "Influenza_fluB" -ni 200 -np 10 -ns 10 -nu 20
```

* Options:
  + -f: Fitness landscape ("Ribozyme", "Fluorescence", "Influenza_fluB")
  + -ni: Size of the initial dataset
  + -np: Number of particles
  + -ns: Number of samples created by revere quantum annealing around single particle
  + -nu: Number of updates 


* Note, that to use FMIRA you need a D-Wave passcode that can be obtained at

```
https://cloud.dwavesys.com/leap/signup/
```

Add it in the part 'YOUR PASSCODE'

```
sampler = DWaveSampler(endpoint='https://cloud.dwavesys.com/sapi', token='YOUR PASSCODE', solver='Advantage_system4.1')
