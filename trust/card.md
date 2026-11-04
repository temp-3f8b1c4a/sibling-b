# AI TrustBOM system card

> **draft (unapproved)**

## Identity

- **System:** sibling-b
- **Repository:** `sibling-b`
- **Commit:** `b71846bf119dd69183df040327c13fb7200ae40a`
- **Graph fingerprint:** `ee9cdb61f0e5`
- **Full fingerprint (SHA-256):** `ee9cdb61f0e5f7dbf5fe2a86afca02bc836fff492dd3de03db02cccd228aad57`
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
| openai | gpt-4o | us-west-2 | unknown | manual | `trust/manual.yml:3` |

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
| model-id-undeclared | medium | The bedrock package is present but no model ID was found in an allowlisted configuration file. | `src/Bedrock/Bedrock.csproj:6` (pack assist-dotnet, rule package:csproj:AWSSDK.BedrockRuntime, package AWSSDK.BedrockRuntime 3.7.400) |
| subprocessor-undeclared | medium | Provider 'bedrock' has no declared subprocessor. | `src/Bedrock/Bedrock.csproj:6` (pack assist-dotnet, rule package:csproj:AWSSDK.BedrockRuntime, package AWSSDK.BedrockRuntime 3.7.400) |

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

- dotnet (src/Bedrock/Bedrock.csproj)

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

Commit `b71846bf119dd69183df040327c13fb7200ae40a` using AI TrustBOM CLI `1.0.0`.

## Gate assessment

- **Status:** failed
- **Summary:** The gate is blocked by 3 conditions.

### Semantic changes

- Added medium finding model-id-undeclared.
- Added medium finding subprocessor-undeclared.
- Changed coverage statement ecosystems (informational): none -\> dotnet (supported).
- Changed coverage statement ecosystem manifests (informational): none -\> src/Bedrock/Bedrock.csproj.

### Required actions

#### The approved graph does not match this change

Trust approved fingerprint 862f108bee16, but this branch produces ee9cdb61f0e5.

Choose the appropriate resolution:

- Revert or correct unintended AI-system changes.
- Add a reasoned manual declaration when repository evidence is incomplete.
- If the changes are intended, have Trust review the semantic changes and complete graph before approving the current fingerprint.

Example:

```yaml
approved_graph_sha: ee9cdb61f0e5f7dbf5fe2a86afca02bc836fff492dd3de03db02cccd228aad57
```

#### Finding model-id-undeclared is not waived

The model-id-undeclared finding is medium. This workflow blocks medium or higher, and no active waiver covers it.

Evidence:

- `src/Bedrock/Bedrock.csproj:6`

Choose the appropriate resolution:

- Fix the underlying finding and rerun the scan.
- If Trust accepts the risk temporarily, add or renew a time-bounded waiver with a reason and reviewer.

Example:

```yaml
waivers:
  - finding_id: 'model-id-undeclared'
    reason: <why the risk is accepted temporarily>
    until: <yyyy-MM-dd>
    by: <Trust reviewer>
```

#### Finding subprocessor-undeclared is not waived

The subprocessor-undeclared finding is medium. This workflow blocks medium or higher, and no active waiver covers it.

Evidence:

- `src/Bedrock/Bedrock.csproj:6`

Choose the appropriate resolution:

- Fix the underlying finding and rerun the scan.
- If Trust accepts the risk temporarily, add or renew a time-bounded waiver with a reason and reviewer.

Example:

```yaml
waivers:
  - finding_id: 'subprocessor-undeclared'
    reason: <why the risk is accepted temporarily>
    until: <yyyy-MM-dd>
    by: <Trust reviewer>
```

### Next step

Resolve every blocking condition below, then rerun AI TrustBOM.

