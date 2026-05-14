# Cosmic Ray Line Filter

This change adds a new `line-filter` to Cosmic Ray.

The filter allows users to run mutation testing only on selected line ranges instead of mutating the whole file or module.

## Problem

Mutation testing can be slow and computationally expensive, especially on larger codebases. In many workflows, users do not need to mutate everything.

A common case is refactoring, where the developer only changed or wants to verify a specific part of a file. Running mutation testing on the whole module can create many unnecessary mutants and make the process slower than needed.

## Solution

The new `line-filter` skips all mutations outside configured line ranges.

This allows users to focus mutation testing only on the relevant code area, reducing noise and helping with faster, more targeted analysis.

## Example config

```toml
[cosmic-ray.filters.line-filter.lines]
"math.py" = "1-4"
"util.py" = ["3", "10-12"]
```

## Example usage

```bash
cosmic-ray init cosmic-ray.toml cosmic-ray.sqlite
cr-filter-lines cosmic-ray.sqlite --config cosmic-ray.toml
cosmic-ray exec cosmic-ray.toml cosmic-ray.sqlite
```

## Why this is useful

This is mainly useful for targeted mutation testing workflows, for example:

- checking only lines touched during refactoring
- focusing on recently changed code
- reducing unnecessary mutation jobs
- making mutation testing more practical on larger projects

## Notes

This functionality did not previously exist in Cosmic Ray, so it was added as a new filter.

The change was communicated with a Cosmic Ray maintainer and is currently waiting for approval as a pull request before being merged into the production Cosmic Ray framework.