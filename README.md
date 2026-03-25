# CHSH_Report

## Objective
This is an experiment review based off of Qiskit's CHSH Inequality. We are testing the outcome of the algorithm when processing on an ideal simulator (AER) compared to a quantum machine. 

**Algorithm URL:** https://github.com/Qiskit/textbook/blob/main/notebooks/ch-demos/chsh.ipynb

## Background
The CHSH inequality, named after Clauser, Horne, Shimony, and Holt, is a generalized formulation of Bell’s Theorem. It provides a mathematical framework to test the principle of local realism. Local realism suggests that physical properties exist independently of measurement (realism) and that physical processes can only be influenced by their immediate surroundings (locality).

In classical mechanics, any system governed by local hidden variables must satisfy the inequality $|S| \leq 2$. However, quantum mechanics predicts that entangled particles can exhibit correlations that exceed this limit. By preparing a pair of qubits in a Bell state and measuring them at specific relative angles, quantum systems can reach a maximum theoretical value known as Tsirelson’s Bound.

## Experiment

In Qiskit's demonstration of the experiment, their results show that the ideal simulator reaches a near perfect violation of the CHSH violation of 2.828 at certain angles. However, when processed on one of IBMs Quantum Machines (ibm_quito), it hardly passes the CHSH expectation value of 2. Even though it passes the violation expectation of being greater than 2, it nearly fails the experiment. Excessive noise in the quantum machine's hardware is a potential way for this to be the case. The noise can be produced from factors such as readout errors and gate fidelities. This is evident with our results for the experiment.

## Results 

The difference is that in our implementation of the experiment we use a different quantum machine (ibm_miami) which yielded results extremely close to the ideal simulator. We concluded that the main factor in varying CHSH expectations using this algorithm is the amount of noise from the quantum machine.

