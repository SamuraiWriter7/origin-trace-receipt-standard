# Origin Trace Receipt Standard

**Origin Trace Receipt Standard** is a lightweight specification for preserving the origin, trace, transformation, evidence binding, transformation diff, royalty handoff, human review gate, and downstream protocol handoff information of AI-assisted outputs.

It is designed as a bridge between:

- AI Search Trace Receipt Standard
- Synchronization Audit Protocol
- Origin Structure Market
- Origin License Policy Registry
- Royalty OS / Compute Access Royalty OS
- OKF Royalty OS Bridge
- Memory Breathing / Trace Relay systems
- Multi-Wing orchestration systems

## Purpose

AI-assisted creation increasingly involves multiple layers:

1. A human origin or structural idea
2. AI-mediated search, dialogue, or transformation
3. Evidence that supports origin, trace, or transformation claims
4. Structural differences between input and output
5. Similarity, synchronization, or derivation risk
6. Downstream reuse, licensing, market registration, or royalty allocation
7. Human review before sensitive downstream actions
8. Protocol handoff to specialized systems

Without a common receipt format, these layers become disconnected.

This standard defines a minimal `Origin Trace Receipt` record that can connect those layers without replacing specialized downstream protocols.

## Core Concept

An Origin Trace Receipt answers nine questions:

1. **Origin** — What idea, structure, document, code, prompt, or protocol did this output originate from?
2. **Trace** — What sources, interactions, repositories, files, or conversations contributed to it?
3. **Transformation** — How was the input transformed into the output?
4. **Evidence** — What evidence supports the origin, trace, transformation, or audit claims?
5. **Diff** — What was preserved, added, removed, modified, abstracted, or formalized?
6. **Audit** — Is there synchronization, derivation, or originality risk?
7. **Royalty Handoff** — Which royalty, license, market, or registry system should receive the record?
8. **Human Review Gate** — Which actions require human review before proceeding?
9. **Protocol Handoff** — Which downstream protocol should inspect or process this receipt next?

## Design Principles

- Minimal but extensible
- Human-readable first
- Machine-validatable by JSON Schema
- Compatible with YAML and JSON
- Designed for AI agents, GitHub repositories, documentation systems, and royalty-aware workflows
- Does not attempt to decide ownership automatically
- Does not execute payment or settlement
- Does not replace legal, governance, or human review
- Preserves evidence for later human or protocol review
- Prevents sensitive downstream actions from bypassing human review

## Record Layers

### 1. Origin Layer

Describes the initial origin of the structure.

Examples:

- idea
- prompt
- document
- code
- dataset
- workflow
- protocol
- conversation

The Origin Layer may include:

- origin ID
- title
- origin type
- origin summary
- creator reference
- repository reference
- license policy ID

### 2. Trace Layer

Records source interactions used in the creation or transformation process.

Examples:

- user dialogue
- source repository
- uploaded file
- web page
- model output
- manual note

The Trace Layer does not prove ownership by itself.  
It preserves source interaction context for later audit.

### 3. Transformation Layer

Describes how the input became the output.

Examples:

- summary
- rewrite
- specification
- derivation
- composition
- analysis
- translation
- implementation

This layer gives a high-level explanation of the transformation.

### 4. Evidence Binding Layer

The Evidence Binding Layer connects receipt claims to reviewable evidence.

It does not decide ownership, authorship, or originality automatically.  
Instead, it records which evidence supports each layer of the receipt.

Evidence may include:

- conversation excerpts
- file references
- repository URLs
- repository commits
- document hashes
- external receipts
- timestamps
- signatures
- manual attestations
- model outputs

Each evidence binding can target a specific receipt layer:

- origin
- trace
- transformation
- evidence
- transformation_diff
- audit
- royalty_hook
- royalty_handoff
- human_review_gate
- boundary
- handoff
- validation
- whole_receipt

This makes the receipt auditable without forcing all downstream systems to use the same evidence format.

### 5. Transformation Diff Layer

The Transformation Diff Layer records how an output differs from its inputs.

It can describe whether elements were:

- preserved
- added
- removed
- modified
- merged
- split
- reordered
- abstracted
- formalized

This layer does not automatically determine ownership or infringement.

Instead, it preserves the structural difference record needed for later audit, attribution, licensing, royalty allocation, or market registration.

Each diff item may include:

- source element
- output element
- diff type
- impact level
- semantic distance
- evidence binding IDs
- review flags
- rationale

This allows downstream systems to inspect whether an AI-assisted output is mostly preserved, lightly modified, deeply transformed, or structurally novel.

### 6. Audit Layer

The Audit Layer records the current review state of the receipt.

It may describe:

- synchronization risk
- originality assessment
- evidence level
- whether evidence binding exists
- whether transformation diff exists
- whether royalty handoff is ready
- whether human review is required
- Human Review Gate status

The Audit Layer does not make a final legal or ownership decision.  
It records the current state so downstream systems can decide what to do next.

### 7. Royalty Hook Layer

The Royalty Hook Layer provides a lightweight declaration of value-return intent.

It may include:

- whether royalty intent is enabled
- policy ID
- allocation recipients
- recipient roles
- share percentages

This layer does not execute payment.  
It only records declared allocation intent.

In the v0.5 schema, `royalty_hook` is optional at the top level.  
The required value-return routing layer is `royalty_handoff`.

### 8. Royalty Handoff Layer

The Royalty Handoff Layer routes an evidence-bound and diff-aware receipt toward downstream value-return systems.

It does not execute payment.  
It does not decide ownership.  
It does not automatically determine licensing outcome.

Instead, it records whether the receipt is ready to be reviewed by systems such as:

- Royalty OS
- Compute Access Royalty OS
- Origin Structure Market
- Origin License Policy Registry
- OKF Royalty OS Bridge
- external marketplaces
- external registries

The layer may describe:

- handoff status
- handoff targets
- target protocol
- target purpose
- required inputs
- missing inputs
- allocation basis
- license handoff status
- review requirements
- settlement intent

This makes the receipt usable as a bridge between trace preservation and value return.

### 9. Human Review Gate

The Human Review Gate prevents evidence-bound, diff-aware, and royalty-handoff-ready receipts from triggering sensitive downstream actions without human review.

This layer may block:

- market registration
- license publication
- commercial use
- AI training use
- royalty execution
- external settlement
- public origin claims
- agent auto-handoff

The gate can define:

- review triggers
- reviewer roles
- blocking conditions
- allowed actions after review
- rejected actions
- decision status
- decision authority
- decision notes

The Human Review Gate does not replace legal judgment or governance.  
It provides a machine-readable checkpoint that downstream systems can respect.

### 10. Boundary Layer

The Boundary Layer defines usage constraints.

Examples:

- attribution required
- commercial restricted
- no training
- custom policy
- prohibited uses
- consent notes

This layer helps prevent downstream systems from stripping away origin, trace, evidence, diff, royalty handoff, or human review information.

### 11. Protocol Handoff Layer

The Protocol Handoff Layer points the receipt toward specialized downstream protocols.

Examples:

- ai-search-trace-receipt-standard
- synchronization-audit-protocol
- origin-structure-market
- origin-license-policy-registry
- compute-access-royalty-os
- kazene-memory-breathing-protocol
- trace-relay-protocol
- multi-wing-orchestration-generator

This layer is used when another protocol should perform deeper inspection, registration, review, or routing.

## First Arc

The first arc of this standard is:

```text
v0.1 = Record Layer
v0.2 = Evidence Binding Layer
v0.3 = Transformation Diff Layer
v0.4 = Royalty Handoff Layer
v0.5 = Human Review Gate
```

Together, these layers create a minimal bridge record for:

```text
origin → trace → evidence → diff → audit → royalty handoff → human review → protocol handoff
```

## Minimal Example

```yaml
schema_version: "0.5.0"
record_type: origin_trace_receipt
receipt_id: otr_2026-07-03-human-review-gate-v0.5
created_at: "2026-07-03T01:00:00Z"

origin:
  origin_id: origin_trace_receipt_core
  title: Trace Receipt / Audit / Origin / Royalty / Human Review Bridge
  origin_type: protocol
  origin_summary: >-
    A bridge record that preserves origin, trace, evidence, transformation diff,
    royalty handoff, human review gate status, and downstream protocol routing.

trace:
  trace_id: trace_initial_design
  source_interactions:
    - source_id: source_user_dialogue
      source_type: conversation
      role: primary
      contribution_weight: 0.7
      interaction_summary: >-
        A design dialogue that defined the origin, trace, evidence, diff,
        royalty handoff, and human review layers.

transformation:
  transformation_type: specification
  input_summary: A set of related protocol ideas.
  output_summary: A machine-readable receipt standard.
  preserved_elements:
    - origin preservation
    - source interaction trace
  changed_elements:
    - formalized schema
    - added human review gate

evidence:
  evidence_set_id: evidence_origin_trace_receipt_v0.5
  binding_strategy: mixed
  evidence_bindings:
    - binding_id: binding_schema_file
      target_layer: whole_receipt
      evidence_type: file_reference
      reference_type: file_path
      reference: "schemas/origin-trace-receipt.schema.json"
      verification_status: trace_supported
      confidence: 0.9
      evidence_summary: Binds the receipt structure to the JSON Schema file.
  evidence_summary: Evidence links support later review.

transformation_diff:
  diff_id: diff_royalty_handoff_to_human_review_gate_v0.5
  diff_scope: schema
  input_references:
    - origin-trace-receipt.schema.json v0.4
  output_references:
    - origin-trace-receipt.schema.json v0.5
  diff_items:
    - element_id: element_top_level_human_review_gate
      diff_type: added
      source_element: null
      output_element: human_review_gate
      impact_level: critical
      rationale: Adds a human review checkpoint before sensitive downstream actions.
  preservation_score: 0.86
  novelty_score: 0.58
  diff_summary: v0.5 adds a Human Review Gate.

audit:
  synchronization_risk: low
  originality_assessment: mixed
  evidence_level: evidence_bound
  evidence_bound: true
  transformation_diff_bound: true
  royalty_handoff_ready: true
  human_review_required: true
  human_review_gate_status: required

royalty_handoff:
  handoff_id: royalty_handoff_origin_trace_receipt_v0.5
  handoff_status: ready_for_review
  handoff_targets:
    - target_id: target_origin_structure_market
      target_protocol: origin-structure-market
      target_purpose: market_registration
      required_inputs:
        - origin
        - trace
        - evidence
        - transformation_diff
        - human_review
      missing_inputs: []
      handoff_readiness: ready
  allocation_basis:
    basis_type: mixed
    source_layers:
      - origin
      - trace
      - evidence
      - transformation_diff
    calculation_method: manual_review
    allocation_notes: Review required before allocation.
  license_handoff:
    license_policy_id: attribution_required_v0.5
    usage_scope: limited
    attribution_required: true
    commercial_status: restricted
    training_status: restricted
    license_notes: Commercial use and AI training require review.
  review_requirements:
    human_review_required: true
    review_triggers:
      - custom_policy
  settlement_intent:
    enabled: true
    execution_mode: review_required
    settlement_type: royalty_split
    settlement_notes: Settlement must be handled downstream after review.
  handoff_summary: Routes receipt toward royalty and market review.

human_review_gate:
  gate_id: human_gate_origin_trace_receipt_v0.5
  gate_status: pending_review
  review_required: true
  review_triggers:
    - market_registration_requested
    - external_settlement_requested
  reviewer_roles:
    - originator
    - auditor
  blocking_conditions:
    - condition_id: condition_market_registration_review
      condition_type: market_registration
      severity: medium
      blocks_actions:
        - market_registration
        - public_claim
      condition_summary: Market registration requires human review.
  allowed_after_review:
    - attribution_publication
    - market_registration
    - royalty_handoff
  rejected_actions:
    - royalty_execution
    - external_settlement
    - agent_auto_handoff
  decision_record:
    decision_status: pending
    decision_authority: multi_party_review
    decision_notes: Human review has not yet approved downstream execution.
  gate_summary: Human review is required before sensitive actions.

boundary:
  usage_policy: attribution_required
  prohibited_uses:
    - false attribution of origin
    - removal of trace or audit metadata
    - bypassing the Human Review Gate for sensitive downstream actions
  consent_notes: Reuse requires attribution, trace preservation, and review compliance.

handoff:
  next_protocols:
    - synchronization-audit-protocol
    - origin-structure-market
    - origin-license-policy-registry
  related_records:
    - origin_trace_receipt_v0.5
  handoff_notes: Use downstream systems for deeper audit, licensing, and settlement review.

validation:
  validation_status: draft
```

## Repository Structure

```text
origin-trace-receipt-standard/
├─ README.md
├─ CHANGELOG.md
├─ schemas/
│  └─ origin-trace-receipt.schema.json
├─ examples/
│  └─ origin-trace-receipt.example.yaml
├─ scripts/
│  └─ validate_examples.py
├─ requirements.txt
└─ .github/
   └─ workflows/
      └─ validate.yml
```

## Validation

Install dependencies:

```bash
pip install -r requirements.txt
```

Validate examples:

```bash
python scripts/validate_examples.py
```

Expected output:

```text
[validate] Origin Trace Receipt
  schema : schemas/origin-trace-receipt.schema.json
  example: examples/origin-trace-receipt.example.yaml
[ok] origin-trace-receipt.example.yaml is valid
```

## Version

Current candidate:

```text
v0.5.0-candidate
```

## Status

This repository currently defines the first complete arc of the Origin Trace Receipt Standard.

The goal of v0.5 is not to solve ownership, licensing, royalty allocation, market registration, or legal review automatically.

The goal is to define the smallest reliable receipt that can connect:

- origin
- trace
- evidence
- transformation diff
- audit
- royalty handoff
- human review
- downstream protocol routing

## Non-Goals

This standard does not:

- prove legal ownership
- determine infringement
- execute payment
- finalize licensing outcomes
- replace legal review
- replace governance review
- replace downstream royalty systems
- replace origin markets or registries
- authorize agent execution without review

## License

Add a license according to the intended usage policy of the repository.

Recommended options:

- MIT for open technical reuse
- Apache-2.0 for patent-aware technical reuse
- CC-BY-4.0 for documentation-focused reuse
- Custom attribution-required policy for origin-sensitive protocol work
