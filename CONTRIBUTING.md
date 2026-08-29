# Contributing to H-CAM

H-CAM is managed as a multi-repository enterprise platform. Keep each change
focused on one owned responsibility and preserve compatibility at repository
boundaries.

## Delivery flow

1. Create or link a GitHub issue for the outcome, decision, risk, or defect.
2. Add the issue to the H-CAM Platform Delivery project and set its phase,
   workstream, priority, target profile, and gate.
3. Work on a focused branch such as `feature/*`, `fix/*`, `docs/*`,
   `research/*`, or `codex/*`.
4. Update contracts and architecture documentation before changing a
   cross-service interface.
5. Open a pull request with validation evidence, compatibility impact, rollback
   notes, and explicit data-handling boundaries.
6. Merge only after the gates currently enabled for that work item are met.

Repository review requirements may be temporarily changed by an accountable
owner, but the issue, commit, validation, and decision trail must remain in
GitHub.

## Required hygiene

- Run the repository's documented checks before publishing a change.
- Keep generated artifacts, model binaries, datasets, camera media, and local
  test output out of Git unless a repository policy explicitly permits them.
- Never commit secrets, credentials, Government/private data, police records,
  personal data, or sensitive footage.
- Use synthetic, public, or explicitly authorized data and label it accurately.
- Record limitations; do not claim deployment, conformance, or production
  readiness without the required evidence and acceptance.

See [GOVERNANCE.md](GOVERNANCE.md) for sources of truth and ownership rules.
