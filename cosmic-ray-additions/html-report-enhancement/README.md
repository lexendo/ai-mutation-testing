# Cosmic Ray HTML Report – Skipped Mutants Filter

This change extends the existing `html.py` report generator in Cosmic Ray with a new flag for hiding skipped mutants from the generated HTML report.

## Added option

```bash
--hide-skipped / --show-skipped
```

## Problem

The generated HTML report could contain many skipped mutations. These entries usually had little value for result analysis, but made the report cluttered and harder to read.

This also made reviewing mutation testing results more time-consuming, which is a practical problem because mutation testing is already slow and can produce large result sets.

## Solution

When `--hide-skipped` is used, work items with `worker_outcome == "skipped"` are hidden from the HTML report.

This keeps the report focused on useful results, mainly killed and surviving mutants.

## Example

```bash
cosmic-ray html --hide-skipped session.sqlite > report.html
```

## Notes

This change is implemented in the existing `html.py` report flow and is already used in the official Cosmic Ray framework.