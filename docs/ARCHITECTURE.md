# Architecture overview

This document describes boundaries and responsibilities, not private implementation details.

## 1. Scientific engine

The scientific engine performs numerical inference and manages the research loop. Within the model families currently available to it, the loop can collect observations, fit candidate explanations, compare models using evidence and complexity penalties, derive consequences, test predictions, inspect residual structure, and update claims when evidence conflicts.

The set of model families and available actions is finite. Success inside that language is not the same as open-ended scientific discovery.

## 2. Experimental world

Controlled simulated worlds provide the phenomena and noisy instruments. In the Frontier branch, the world generator/integrator runs in a separate process from the scientist. The intended boundary is that the scientist sees only explicitly permitted public information and experiment observations; hidden rules are consulted only by the evaluator after the run has been sealed.

Development worlds help build the system but cannot alone establish generalization. Held-out worlds should be generated independently of the scientist's source and kept from the developer tuning the tested agent until the protocol permits unsealing.

## 3. Scientific memory

The design distinguishes raw observations from revisable beliefs. Scientific records should preserve provenance and a history of claim-status changes so an incorrect later conclusion does not silently rewrite the evidence that led to it. This repository does not include the canonical memory database or its private contents.

## 4. Optional language interface

A language model is not the scientific source of truth. If used, it should interpret a request into a constrained representation or explain structured records emitted by the engine. Any rephrasing should be checked for added numbers, altered uncertainty, or changed epistemic status. Interface fidelity is a separate evaluation task.

## 5. Primary prototype versus Frontier

The primary prototype and the experimental Frontier branch are distinct development lines. Frontier experiments with richer, physics-neutral representations and a more separated hidden-world boundary; it is incomplete and should not be described as fully integrated into the primary prototype or its 3D interface.
