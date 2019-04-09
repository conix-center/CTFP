# CTFP

Towards Verified, Constant-time Floating Point Operations 

This is for the sake of collecting source code created in CONIX to a single location. Code repository at https://github.com/marcandrysco/CTFP

# Publication

```
Marc Andrysco, Andres Noetzli, Fraser Brown, Ranjit Jhala, and Deian Stefan
A DSL for Timing-Sensitive Computation
Proceedings of the ACM Conference on Computer and Communications Security (October 15 2018)
```

This work is documented by SRC publication [P095923]

## Abstract

> The runtimes of certain floating-point instructions can vary up to two orders of magnitude with instruction operands, allowing attackers to break security and privacy guarantees of real systems (e.g., browsers). To prevent attacks due to such floating-point timing channels, we introduce CTFP, an efficient, machine-checked, and extensible system that transforms unsafe floating-point operations into safe, constant-time computations. CTFP relies on two observations. First, that it is possible to execute floating-point computations in constant-time by emulating them in software; and second, that most security critical applications do not require full IEEE-754 floating-point precision. We use these observations to: eliminate certain classes of dangerous values from ever reaching floating-point hardware; emulate floating-point operations on dangerous values when eliminating them would severely alter application semantics; and leverage fast floating-point hardware when it is safe to do so. We implement the constant-time transformations with our own domain-specific language that produces LLVM bitcode. Since the transformations themselves equate to bit surgery on already complicated floating-point arithmetic, we use a satisfiability modulo theories (SMT) solver to ensure that their behavior fits our specifications. Finally, we find that CTFP neither breaks real world applications nor incurs overwhelming overhead.
