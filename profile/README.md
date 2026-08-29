# H-CAM

**H-CAM is a modular, resource-adaptive video intelligence platform for
real-time camera operations, AI analytics, investigation, and enterprise
governance.**

The platform is designed to run from a CPU-only developer laptop through an
owned GPU lab, standalone servers, and Kubernetes clusters. Capability
inventory, explicit policy, compatibility data, and safe fallbacks determine
which services and AI layers run; unavailable acceleration must degrade
predictably without changing platform contracts.

## Platform Map

| Layer | Primary repositories |
|---|---|
| Product and operator experience | `hcam-frontend`, `hcam-dashboard`, `hcam-ui`, `hcam-admin` |
| API, identity, and contracts | `hcam-api`, `hcam-auth`, `hcam-protos`, `hcam-sdk` |
| Camera and video data plane | `hcam-video-engine`, `hcam-storage` |
| AI and intelligence | `hcam-intelligence-core`, `hcam-ai-models`, `hcam-tracking`, `hcam-anpr` |
| Data and events | `hcam-data`, `hcam-event-bus` |
| Security and operations | `hcam-security`, `hcam-infrastructure`, `hcam-deployment`, `hcam-observability` |
| Architecture and delivery | `hcam-docs`, `h-cam-2.0`, [Platform Delivery Project](https://github.com/orgs/hcam-2-0/projects/1) |

## Engineering Model

```text
Issue / Decision -> Project gate -> Focused branch -> Pull request
       -> Validation evidence -> Merge -> Release or phase acceptance
```

- Runtime boundaries use versioned APIs, events, schemas, and packages.
- The control plane configures and authorizes; the data plane processes streams
  and emits bounded metadata/events.
- The synthetic lab is isolated from the production architecture and never
  represents Government or police data.
- Current priorities and authorization gates live in the
  [H-CAM Platform Delivery project](https://github.com/orgs/hcam-2-0/projects/1).

Start with [H-CAM documentation](https://github.com/hcam-2-0/hcam-docs), the
[governance model](https://github.com/hcam-2-0/.github/blob/main/GOVERNANCE.md),
and the [security policy](https://github.com/hcam-2-0/.github/security/policy).
