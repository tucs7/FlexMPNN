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

* Note, that to use FMIRA you need a D-Wave passcode that can be obtained at

```
https://cloud.dwavesys.com/leap/signup/
```

Add it in the part 'YOUR PASSCODE'

```
sampler = DWaveSampler(endpoint='https://cloud.dwavesys.com/sapi', token='YOUR PASSCODE', solver='Advantage_system4.1')
