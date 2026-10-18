# Reproducibility status

## Current status: overview only, not a runnable source release

This repository describes the research program but does not include the private engine source, canonical memory database, world truth, or a runnable reproduction package. Consequently, a reader cannot reproduce the project results from this repository alone.

## Requirements for a future reproduction release

A versioned release should include:

- The exact source revision used to generate each claimed result.
- Dependency versions and supported Python version.
- One documented command to create/select a development world and execute the scientist.
- Run seed, world-generator version, declared compute budget, and environment details.
- Complete immutable observation/decision/claim ledger for each reported run.
- Prediction records distinguishing fitting data from held-out data.
- A post-run comparison against hidden simulator truth, clearly separated from the scientist's knowledge during the run.
- Automated tests for key inference and integrity guarantees.
- A clear statement of known failures and unsupported environments.

## Do not infer reproducibility from a video

A video can show a workflow, but it cannot establish the exact code revision, data provenance, or whether a result can be regenerated. Until a reproduction package is released and checked by another party, describe current results as developer-recorded controlled-simulation outcomes.
