# AI TrustBOM system card

> **draft (unapproved)**

## Identity

- **System:** sibling-b
- **Repository:** `sibling-b`
- **Commit:** `2d359e6afac9c9651c0596a164e8d0d48ca36dda`
- **Graph fingerprint:** `c6442fba043f`
- **Full fingerprint (SHA-256):** `c6442fba043f91b5e61148a445280b3a16e188aa2b2001430792ab9fc93c41b5`
- **CLI version:** `1.0.0`
- **Description:** Synthetic sibling source for MTP-30/31 import tests.
- **Customer-facing name:** Sibling B Service

## Draft classification

- **Role:** `unknown`
- **GPAI provider:** `false`
- **High risk:** `unknown`
- **Article 50:** `unknown`

## Models

| Provider | Model | Region | Endpoint | Source | Cite |
|---|---|---|---|---|---|
| openai | gpt-4o | us-east-1 | unknown | manual | `trust/manual.yml:3` |

## Declared subprocessors

| Provider | Party | Purpose | Location | DPA path | Cite |
|---|---|---|---|---|---|
| openai | OpenAI | Synthetic model inference | United States | trust/dpas/openai.txt | `trust/dpas/openai.txt`<br>`trust/subprocessors.yml:2` |

## Data handling

Trust declares, for each AI provider used by this system, how long prompts and customer data are retained, whether that data is used to train provider models, and how deletion is requested. AI TrustBOM does not read, fetch or verify provider terms. "unknown" means Trust has not declared the value; it is not a statement that data is retained, used for training, or safe.

| Provider | Prompt retention | Training use | Deletion path | Source | Cite |
|---|---|---|---|---|---|
| openai | 30 days | not used for training | trust/deletion-openai.md | manual | `trust/deletion-openai.md:1`<br>`trust/dpas/openai.txt:1`<br>`trust/manual.yml:19` |

## Tools

| Name | Effect | Source | Cite |
|---|---|---|---|
| unknown | unknown | unknown | none |

## MCP servers

| Name | Connection | Source | Cite |
|---|---|---|---|
| unknown | unknown | unknown | none |

## Declared data

| Class | Sent to model | Source | Cite |
|---|---|---|---|
| unknown | unknown | unknown | none |

## Declared controls

| Control | Value | Source | Cite |
|---|---|---|---|
| human_send_required | true | manual | `trust/manual.yml:12` |
| kill_switch | true | manual | `trust/manual.yml:15` |
| prompt_bodies_stored | false | manual | `trust/manual.yml:9` |

## Evaluation gates

| Name | Path | Source | Cite |
|---|---|---|---|
| unknown | unknown | unknown | none |

## Findings

| ID | Severity | Message | Cite |
|---|---|---|---|
| none | info | No open scan findings. | none |

## Coverage statement

This card describes only what AI TrustBOM detected in tracked repository files and what Trust declared manually. It does not establish that other AI use is absent: files, ecosystems and runtime behaviour outside the method below may contain AI use that was not detected.

**Detector packs used:**

- assist-dotnet 1.0.0
- assist-go 1.0.0
- assist-java 1.0.0
- assist-js 1.7.0
- assist-python 1.4.0
- data-processing 1.0.0
- raw-http 1.0.0

**Ecosystems found with detector support:**

- None found

**Ecosystems found without detector support (AI use unknown):**

- None found

**Not in scope (excluded by Trust):**

- None declared

**Method limits:**

- Models, regions and endpoints are matched only in allowlisted configuration files by detector-pack patterns.
- Ecosystems are recognised from manifest and lockfile names only.
- Source code is not parsed; there is no AST or call-graph analysis.
- Runtime behaviour, network traffic and deployed infrastructure are not inspected.
- Only files tracked in Git at the scanned commit are read.

Ecosystems are recognised from tracked manifest and lockfile names only; an ecosystem without a recognised manifest or lockfile is not listed.

## Generated from

Commit `2d359e6afac9c9651c0596a164e8d0d48ca36dda` using AI TrustBOM CLI `1.0.0`.

## Gate assessment

- **Status:** bootstrap required
- **Summary:** The gate is blocked because this repository has no reviewed graph approval.

### Semantic changes

No semantic graph changes are available.

### Required actions

#### The approval file is still the unsigned template

trust/approvals.yml exists but is still the unsigned template. The first graph must be reviewed by Trust before it can become the baseline.

Choose the appropriate resolution:

- Review the generated system card and repository evidence.
- Replace the template in trust/approvals.yml with the approval below and complete every human-owned value.
- Request the configured Trust or CODEOWNER review; check the full graph before approving its fingerprint.

Example:

```yaml
approved_graph_sha: c6442fba043f91b5e61148a445280b3a16e188aa2b2001430792ab9fc93c41b5
approved_by: <Trust reviewer>
approved_at: <ISO-8601 timestamp>
high_risk: unset
article_50: unset
```

### Next step

Have Trust review graph fingerprint c6442fba043f and commit trust/approvals.yml. Copy the full fingerprint from the approval template above.

