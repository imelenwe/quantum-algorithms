# Plan: Generic Grover Search

## Methods

1. `phase_flip_all_ones(qc, qreg)`
2. `oracle(qc, qreg, tomark)`
3. `diffusion_operator(qc, qreg)`
4. `grover_search(query, shots=1024)`

## Explanation
1. Mark the state to search using the oracle
2. Oracle can mark all 1's
3. So if state to maerk has 0's then forst X all of the bits and then mark and then X again
4. Once marked apply diffusion operator which is H U_g H.
5. U_g marks all state except all 0 state with -ve amp
6. So apply H before and after U_g. 
7. The Oracle and Diffusion operator are applied successively to obtain the solution (find marked state)
8. G = D.O
9. If we overdo iteration then the reflections can overhsoot and miss the solution state.
