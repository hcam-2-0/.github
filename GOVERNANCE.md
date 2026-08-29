# H-CAM Governance

## Sources Of Truth

| Concern | Canonical GitHub location |
|---|---|
| Delivery status, priority, gates, and target profile | H-CAM Platform Delivery Project |
| Work scope, acceptance criteria, decisions, risks, and ownership | GitHub issues |
| Implementation, review discussion, and validation evidence | Pull requests and commits |
| Platform architecture and engineering operating model | `hcam-docs` |
| Cross-service API, event, and schema contracts | `hcam-protos` |
| Runtime source and repository-specific operations | The owning implementation repository |
| Security reporting | `SECURITY.md` and an approved private channel |

Slack or meetings may start a discussion, but decisions and actionable work must
be captured in GitHub. External planning tools may mirror status, but they do
not replace repository history, issues, contracts, or Project fields.

## Ownership

Each repository has one primary responsibility. Cross-repository changes must
identify the owning repository, affected contracts, compatibility strategy,
and rollout order. Shared behavior belongs in a versioned contract or package,
not copied source.

The accountable owner accepts phase gates and security-sensitive authority.
Review requirements may be changed explicitly for a bounded period, but no
message such as "continue", silence, or unrelated approval is acceptance of a
decision or expansion of data, camera, model, deployment, or network authority.

## Change Classes

- **Routine:** compatible implementation, tests, or documentation inside one
  owned boundary.
- **Cross-repository:** changes an API, event, schema, package, deployment
  interface, or ownership boundary and requires a linked architecture decision.
- **Controlled:** affects credentials, identity, private networks, cameras,
  media, datasets, models, evidence, retention, or deployment and requires the
  explicit gate recorded on the Project item.
- **Emergency:** restores availability or security with the smallest bounded
  change; follow-up evidence and reconciliation remain mandatory.

## Phase Gates

A phase or work package is complete only when its acceptance criteria,
validation evidence, limitations, unresolved risks, artifact/commit identity,
and accountable-owner decision are recorded. A merged pull request alone does
not imply phase acceptance or deployment authorization.

## Data And Safety Baseline

H-CAM repositories must not contain Government/private data, police records,
credentials, personal data, sensitive camera media, unlicensed datasets, or
unapproved model artifacts. Synthetic and public fixtures must be labelled.
External systems are read-only unless an explicit, bounded authorization says
otherwise.
