# Collection of Stochastic SAT Instances

## Purpose

This collection of stochastic SAT (SSAT) instances is intended to be a benchmarking suite for evaluating the efficiency of decision procedures for SSAT solving.

## Format

The SSAT instances in this collection are encoded with the `sdimacs` format, which adapts the `qdimacs` format for quantified Boolean formulas.

A randomly quantified variable `x` (with probability `p`) is written as `r p x 0`.
For example, the SSAT query:

```
exist x1, exist x2, random p=0.5 x3, random p=0.5 x4. (x1 or x3) and (x2 != x4).
```

is encoded as follows:

```
p cnf 4 3
e 1 0
e 2 0
r 0.5 3 0
r 0.5 4 0
1 3 0
2 4 0
-2 -4 0
```

## Collected SSAT Families

The collection consists of the following families of SSAT instances:

- `re-random-k-CNF/`: RE-SSAT instances converted from random k-CNF formulas
- `re-strategic-company/`: RE-SSAT instances converted from strategic-company QBFs
- `re-PEC/`: RE-SSAT instances encoding the PEC problem
- `er-random-k-CNF/`: ER-SSAT instances converted from random k-CNF formulas
- `ere-sand-castle/`: ERE-SSAT instances encoding the sand-castle problem
- `ere-ToiletA/`: ERE-SSAT instances converted from ToiletA QBFs
- `ere-conformant/`: ERE-SSAT instances converted from conformant-planning QBFs
- `ere-MaxCount/`: ERE-SSAT instances converted from maximum-model-counting formulas

## Contribution

This repository is open for submission of new SSAT instances.
Please fork the repository, commit your changes, and send a pull request.

## License

The SSAT instances are under open-source license Apache 2.0.

## Contact

You are welcome to create an issue for discussion.
