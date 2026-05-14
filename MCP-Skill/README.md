# RooCode Skill – Targeted Mutation Testing

This skill tells a RooCode agent how to handle targeted mutation testing with Cosmic Ray.

It helps the agent detect mutation testing requests, use the MCP server, prepare line-based mutation configs, run the workflow, and generate HTML reports when needed.

## Purpose

The skill connects RooCode with the Cosmic Ray MCP workflow, mainly through:

```text
prepare_line_mutation_config
execute_line_mutation_testing
```

It is useful because mutation testing is slow, so the agent should focus only on relevant files/lines and avoid rerunning tests when results already exist.

## Notes

Designed for RooCode workflows that use my MCP server.