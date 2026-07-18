# FlexMPNN 

FlexMPNN is a framework for ensemble-conditioned inverse folding inference using conformational ensembles generated via rigidity-theory–based constrained geometric simulations

# Installation steps

* Install ProteinMPNN fallowing steps described in

```
https://github.com/dauparas/ProteinMPNN
```

# Usage

To perform inference using pre-generated conformational ensembles run

```
  ./ensemble_inference.sh
```

Pre-generated conformational ensembles produced using FRODAN are available in /simulation_trajectories_benchmarking_FRODAN. Corresponding Molecular Dynamics ensembles are available in /simulation_trajectories_benchmarking_MD.

# Conformational ensemble generation using FRODAN

Set FRODAN installation path

```
 export FRODANHOME=/path/to/FRODAN
```

Run the preprocessing script to generate the necessary input files for a FRODAN simulation

```
  python $FRODANHOME/preprocess.py -i input_structure.pdb -o options_fixedcons.xml

```

Run FRODAN simulation
```

  $FRODANHOME/bin/main options_fixedcons.xml
```

* options_fixedcons.xml can be found in /Ensemble_generation
* FRODAN is not redistributed in this repository due to third-party licensing restrictions. The software can be obtained directly from the original developers (Prof. Michael Thorpe; Michael.Thorpe@asu.edu).

# License

This package is distributed under the MIT License.
