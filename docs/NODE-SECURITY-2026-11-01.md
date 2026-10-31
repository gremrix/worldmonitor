# Node security maintenance draft — 1 November 2026

This repository is a fork. Its upstream homepage is not evidence of a deployment owned by gremrix. No production deployment or actual runtime version was verified.

Replace active Node 20 selectors with Node 22.23.4, including the tracked Docker build recipes. The Docker tag has not been pulled or built in this environment; validate image availability, dependency compatibility and CA stores before merging. No application tests, container build or upstream reconciliation were run locally. Fixture-only historical Node 18 examples are unchanged. Floating Node 22 CI selectors already resolve current patches for fresh runs; that does not attest to historical builds.

Sources: https://nodejs.org/en/blog/vulnerability/october-2026-security-releases and https://render.com/docs/advisory-emudhra . Supported patched floors are 22.23.4 / 24.22.1 / 26.12.1. No Render hosting assumption, no dependency-audit clearance and no production deployment is claimed. Rebuild images rather than restarting old containers, inspect node -p process.versions.node in the build/runtime stages that use Node, and verify the actual deployed image digest after a reviewed release.
