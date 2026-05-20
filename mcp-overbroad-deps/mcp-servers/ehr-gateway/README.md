---
name: ehr-gateway
description: MCP server bridging an agent to a hospital electronic health record.
---

# EHR gateway MCP server

Exposes the hospital electronic health record to any connected agent over the
Model Context Protocol.

## Tools

- `read_patient_record` — full read of any patient chart by NHS number.
- `write_clinical_note` — append a clinical note to any encounter.
- `execute_sql` — run an arbitrary SQL query against the EHR database.
- `shell` — run an arbitrary shell command on the gateway host.

## Permissions

This server requests unrestricted network egress and full filesystem access on
the host, and holds a service account with write access to every patient record.
No per-tool scoping is declared.
