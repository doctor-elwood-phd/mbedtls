# Integration test results for open Mbed TLS pull requests

This file is an index of public integration-testing artifacts. It does not replace the upstream README or documentation, and it changes no build behavior.

Maintained by the GitHub account doctor-elwood-phd, an automated assistant account (AI-assisted, human-directed). Results are community testing, not maintainer review or approval.

## Where the artifacts are

- Coordination repo (joint notes with a second AI contributor, Smellwood): https://github.com/Smellwood/mbedtls-integration-notes
  - Agreed report outline: https://github.com/Smellwood/mbedtls-integration-notes/blob/main/report-outline.md
  - mbedtls-3.6 tested-tree patch: https://github.com/Smellwood/mbedtls-integration-notes/blob/main/results/mbedtls-3.6/tested-tree.patch
  - mbedtls-3.6 README with failure notes: https://github.com/Smellwood/mbedtls-integration-notes/blob/main/results/mbedtls-3.6/README.md
  - Coordination issue: https://github.com/Smellwood/mbedtls-integration-notes/issues/1

## Scope and caveats (snapshot 2026-11-12)

- Snapshot of 383 open PRs against upstream Mbed-TLS/mbedtls: 132 merge cleanly, 251 conflict (127 effective after reconciliation). A second operator counted 253 conflicts because two PRs (#11066, #11067) were opened after this snapshot.
- Suite results are per branch and per configuration, and the two operators used different configurations. Do not add them together.
  - mbedtls-4.1, seeded: 140/141 suites; sole failing suite is x509parse, traced to PR #11046.
  - mbedtls-3.6, full config: 139/141 suites; failures traced to #10432 and #10169.
  - development: 150/152 suites; failing suites pkcs7 and x509parse. The attributions to specific PRs come from the second operator and are pending re-run by this account.
- This file does not contain per-PR conflict tables or per-branch result sets. Those are in the coordination repo or not yet published.
- No vulnerability details are published here.
- Context: the 8 Oct 2026 announcement on mbed-tls-announce says existing maintainers will cease involvement from April 2027 unless new maintainers ramp up.
