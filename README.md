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

* FRODAN is not redistributed in this repository due to third-party licensing restrictions. The software can be obtained directly from the original developers (Prof. Michael Thorpe; Michael.Thorpe@asu.edu).
