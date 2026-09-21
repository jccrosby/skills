---
name: crosby-dependency-upgrade
description: Research and plan a library, framework, runtime, or toolchain upgrade using manifests, compatibility constraints, and authoritative release information. Use when an upgrade may include breaking changes or migration work; do not apply it unless requested.
---

# Plan a dependency upgrade

Build an evidence-backed upgrade path for the repository as it exists. Prefer official release notes, migration guides, compatibility tables, security advisories, and package metadata over summaries or memory.

## Establish the current state

1. Inspect manifests, lockfiles, runtime constraints, build configuration, and direct usage of the dependency.
2. Identify the resolved version, requested range, target version, package manager, and relevant peer or platform dependencies.
3. Determine whether intermediate versions or codemods are required.

## Research the change

Review every relevant release between the current and target versions. Record:

- breaking and deprecated behavior,
- runtime, peer, and platform requirements,
- configuration or API migrations,
- data or generated-artifact changes,
- known incompatibilities and security implications,
- recommended upgrade order.

Cite authoritative sources near the claims they support. Distinguish repository evidence from external guidance and label unresolved compatibility questions.

## Produce the plan

Return:

1. current and target state,
2. compatibility findings,
3. required code and configuration changes,
4. ordered upgrade steps,
5. focused verification and regression coverage,
6. rollback or recovery limits,
7. risks and unresolved questions.

Do not edit manifests, regenerate lockfiles, run codemods, or publish packages unless the user asks. When implementation is requested, preserve unrelated dependency versions and inspect lockfile changes for unexpected transitive updates.
