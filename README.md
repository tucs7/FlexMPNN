# FlexMPNN 

FlexMPNN is a framework for ensemble-conditioned inverse folding inference using conformational ensembles generated via rigidity-theory–based constrained geometric simulations

# Installation steps

* Install ProteinMPNN fallowing steps described in

```
https://github.com/dauparas/ProteinMPNN
```

# Usage

To perform inference using pre-generated ensembles run

```
  ./ensemble_inference.sh

```

# Conformational ensemble generation using FRODAN

```
  python $FRODANHOME/preprocess.py -i *.pdb -o options_fixedcons.xml

  $FRODANHOME/bin/main options_fixedcons.xml

```

* Note, FRODAN is not redistributed in this repository. Academic users may obtain it directly from the original developers (see manuscript Data Availability)
