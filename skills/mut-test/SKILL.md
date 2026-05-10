---
name: mut-test
description: Load this skill anytime mutation is mentioned
---

# Mutation testing Instructions

When asked to run mutation testing call the MCP server, perform prepare then execute.

When calling prepare, take special care to minimize tests (test_command parameter) based on targets.

To pick the minimal test_command, search under `repos/validators/tests` for the specific validator under test (e.g., `test_finance.py`) and use that single test file.

If prepare or execute fails due to an MCP connection error, retry once; if it persists, fall back to running Cosmic Ray from the repo (report.html) for the targeted lines.

After execution, render the report and open it:

```bash
cr-html --hide-skipped cosmic-ray-sql.sqlite > report.html
start report.html
```
