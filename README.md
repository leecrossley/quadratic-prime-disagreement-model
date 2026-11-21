# A prime model with two independently chosen zero patterns

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24416497.svg)](https://doi.org/10.5281/zenodo.24416497)

This result is now maintained in [quadratic-mertens-first-crossings](https://github.com/leecrossley/quadratic-mertens-first-crossings/tree/main/results/quadratic-prime-disagreement-model). This repository is archived and keeps its releases and DOI.

Can the primes that split differently from $`\mathbb Q(\sqrt5)`$ force a quadratic Mertens average below zero? For every sufficiently large packet spacing $`P`$, an assignment of signs to ordinary primes supplies a test of what that comparison alone can establish. The proof does not quantify how large $`P`$ must be.

Both directions of disagreement occur with the usual smoothed counting estimate. The weighted lead rises by order $`\log D`$ across a factor of three, where $`D`$ is a scale parameter. With the double central zero the average stays positive at every real start $`y\ge2`$. For each fixed $`a>0`$ one can choose a sufficiently close pair so that positivity holds throughout $`2\le y\le D^a`$. The product twisted by $`\chi_5`$ can simultaneously have a different zero pattern and a nonzero central value. [Proof](PROOF.md)

The construction starts from the genuine character of discriminant 13, then changes signs in sparse packets of primes. The eligibility of the packets and the base average use the critical-line property for $`\zeta`$ and the three fixed quadratic functions of conductors 5, 13 and 65. The model has no claimed number field of conductor $`D`$. Twisting by $`\chi_{13}`$ detects its base, leaving a concrete distinction from actual large-conductor characters. Alpöge's announced Dirichlet GRH theorem supplies this input. [Prior construction and literature](PRIOR-WORK.md) · [Announcement](https://alpo.ge/remark.pdf) · [Independent formal checks](https://math.mit.edu/~drew/grh/)

## Reproduce the checks

```sh
python3 -m venv .venv
.venv/bin/python -m pip install -r requirements.txt
PYTHON=.venv/bin/python sh verify-release.sh
```

Two implementations evaluate the first packet of two examples. A standard-library calculation also proves that $`L(1/2,\chi_{65})>6/5`$. Lean checks the allocation, rounding, factorisation and signed-tail inequalities. The continuation of the two infinite products and the all-start positivity estimate have written proofs. [Verification details](CHECKS.md)
