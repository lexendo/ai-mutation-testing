# Targeted Mutation Testing – Use Case Baseline

This folder contains an experimental baseline for targeted mutation testing workflows with Cosmic Ray and a RooCode agent.

The goal is to avoid running mutation testing on the whole codebase. Instead, the workflow focuses only on relevant changed code, selected line ranges, suitable mutation operators, and related tests.

## Contents

The documents describe the main use case and its substeps:

- detect changed files and line ranges
- apply line-based mutation filtering
- apply basic quality gates
- exclude irrelevant mutation jobs through the Cosmic Ray database
- select relevant mutation operators
- select relevant tests
- execute the targeted mutation run

## Why it is useful

Mutation testing is often slow and noisy. This baseline shows how an agent-driven workflow can reduce the mutation scope while still keeping meaningful results.

In the experiment, only a small subset of mutations was executed, which made the run much faster and easier to analyze.

## Status

This is an experimental baseline, not a final production workflow.  
It was created to define and demonstrate how targeted mutation testing could work with Cosmic Ray, line filtering and RooCode-style automation.