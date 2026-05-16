# Readiness

Current level: GitHub-ready public skill package, with caveats for live runtime vision verification and jurisdiction-specific/legal/medical exclusions.

## Known Caveats

- This package does not modify profile-level runtime configuration; review the active Hermes profile separately before advertising runtime-specific capabilities.
- Photo diagnosis is not verified unless the active runtime has a vision-capable model/path. If vision is unavailable, route users to text intake via `workflows/troubleshoot-grow.md`.

## Required Verification Before Production or Paid Claims

- Stale path scan returns no stale layout links.
- Version/status wording is consistent across `SKILL.md` and `README.md`.
- LOW confidence policy forbids diagnosis and allows only missing-data requests or low-risk triage checks.
- State schemas and writing workflows include `source_workflow`.
- Live grow-log state contains no fake historical H2 entries below `## User Entries`.
- Profile config must be separately reviewed for explicit vision readiness before photo diagnosis is advertised as ready.
- Legal/medical/trafficking/evasion/extraction refusal boundaries remain intact in public-facing files.
