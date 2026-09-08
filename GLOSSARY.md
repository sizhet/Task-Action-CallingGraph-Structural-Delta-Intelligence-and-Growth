# GLOSSARY — TACG-SDIG

## Task–Action CallingGraph Structural Delta Intelligence and Growth

This glossary defines the canonical terminology used throughout the TACG-SDIG repository.

---

# A

## Action

An executable or implementable operation within the Action Structural Plane.

Examples:

```text
authenticate()
checkOwner()
updateResource()
retry()
rollback()
```

An Action is usually more implementation-oriented than a Task.

---

## Action CallingGraph — ActionCG

A CallingGraph describing executable actions, implementation dependencies, calling paths, or code-level behavior.

Conceptually:

```text
Action Node
    ↓
Action Node
    ↓
Action Node
```

An ActionCG answers:

> **What does the implementation do, and how are those operations connected?**

---

## Action Delta — ΔA

A meaningful structural change on the Action side.

Conceptually:

```text
ΔA =
Target ActionCG
⊖
Reference ActionCG
```

Examples:

```text
Add checkOwner()

Add retry branch

Remove audit logging

Change synchronous call to asynchronous messaging
```

---

## Action Primitive

A small feasible implementation-side structural move.

Canonical source:

```text
1F — Common-Sense Feasible Action / Code Statements / CGs
```

Examples:

```text
authenticate()
authorize()
validate()
retry()
rollback()
emitEvent()
```

Action primitives support **Primitive-Level Constrained Forward Walking**.

---

## Action Structural Plane

One of the four primary TACG-SDIG structural planes.

It contains:

```text
1D — Action / Code CG

1E — Collection of Known Action / Code CGs

1F — Feasible Action / Code Primitives
```

It represents:

> **What the implementation does and what feasible implementation moves are known.**

---

## Adaptation

The process of modifying a historical structural delta or TADP so that it fits the current target context.

Examples include:

```text
renaming roles
changing boundaries
replacing implementation primitives
adding companion deltas
removing irrelevant branches
```

Adaptation is a core part of **Candidate Reconstruction**.

---

# B

## Baseline

A reference structural state used for comparison.

Examples:

```text
reviewed version
production version
certified version
previous release
policy-compliant reference
```

In governance:

```text
New Structure
⊖
Baseline
=
Governance-Relevant Delta
```

---

## Boundary

The structural attachment context surrounding a delta.

Typical form:

```text
Entry Boundary
      ↓
Delta
      ↓
Exit Boundary
```

Boundaries are important for both Delta Search and Candidate Reconstruction.

---

## Boundary-Aware Delta Search

Delta retrieval that uses not only the Delta Core but also its predecessor, successor, and structural attachment context.

Instead of searching only for:

```text
Add Retry
```

search:

```text
Idempotent Remote Call
        ↓
Retry
        ↓
Response Processing
```

This improves precision.

---

# C

## CallingGraph — CG

A graph describing calling, dependency, execution, or task/action relationships among structural units.

Within TACG-SDIG, two important forms are:

```text
TaskCG
ActionCG
```

CallingGraphs provide the structural substrate for localization, Graph Minus, Delta Search, and growth.

---

## Candidate Delta

A structural change retrieved, reconstructed, composed, or generated as a possible solution to a current structural gap.

A Candidate Delta is not yet accepted.

It must pass appropriate validation.

---

## Candidate Reconstruction

The process of adapting historical structural experience into a candidate delta or TADP for the current system.

Conceptually:

```text
Historical Delta
      +
Current Context
      ↓
Candidate Delta
```

---

## Candidate Growth

A proposed transition:

```text
S --Δcandidate--> S'
```

before sufficient validation has established it as accepted growth.

---

## Changed Reachability

A difference between the reachable structures of a baseline and a new structure.

Conceptually:

```text
Reachable(New)
⊖
Reachable(Baseline)
```

It may reveal:

```text
new privileged paths
new external access
new bypasses
new reachable data flows
```

---

## CCC

A folded structural pattern representing recurring structural regularity.

Within TACG-SDIG, an important specialized form is:

```text
Delta CCC
```

which represents recurring transformation structure rather than recurring state structure.

---

## Companion Delta

A structural change that commonly or necessarily accompanies another delta.

Example:

```text
Primary Delta:
Add Retry

Companion Delta:
Add Idempotency
```

Companion Deltas help avoid incomplete candidate reconstruction.

---

## Composite Delta

A coordinated transformation containing multiple related sub-deltas.

Example:

```text
Add Authorization
+
Add Failure Branch
+
Add Audit
```

A Composite Delta may represent one meaningful engineering change.

---

## Conflicting Delta

A delta that creates or reveals structural contradiction.

Example:

```text
Task Delta:
Restrict Access

Action Delta:
Broaden Allowed Roles
```

This may be classified as a **Conflicting Task–Action Delta**.

---

## Constrained Forward Walking

A local structural search process that extends a partial solution using feasible Task and Action primitives under explicit structural constraints.

See:

```text
Primitive-Level Constrained Forward Walking
```

---

## Context-Preserving Folding

A folding process that preserves the conditions under which a recurring structural transformation is applicable.

Example:

Poor abstraction:

```text
Retry failures.
```

Better folded abstraction:

```text
Retry transient failures
when the operation is idempotent
or protected by idempotency control.
```

---

## Counter-Delta

A delta or historical case that structurally opposes, invalidates, or challenges a candidate delta.

It may be treated as one form of counter-evidence.

---

## Counter-Evidence

Historical or structural evidence showing where a similar candidate failed, was rejected, caused regression, or was unsuitable.

Canonical question:

> **Where did a similar delta fail?**

Counter-Evidence is first-class knowledge in TACG-SDIG.

---

## Cross-Plane Consistency

Consistency between the Task, Action, and Mapping planes.

Typical questions:

```text
Does ΔA fully implement ΔT?

Does ΔA introduce extra behavior?

Does ΔT remain partially unimplemented?

Does Action behavior have a valid Task explanation?
```

---

# D

## Delta

A meaningful structural change between a reference and a target state.

Conceptually:

```text
Δ = Target ⊖ Reference
```

In TACG-SDIG:

> **Delta is a first-class structural knowledge object.**

---

## Delta CCC

A folded recurring structural transformation.

Example:

```text
Insert Authorization Gate
before Privileged Operation
```

A Delta CCC captures:

> **What repeatedly changes in the same structural way?**

---

## Delta Cluster

A group of structurally related historical deltas in Delta metric space.

Example:

```text
authorization additions
retry additions
service-extraction changes
```

Delta Clusters are candidates for folding into Delta CCCs.

---

## Delta Core

The directly changed structural region.

Examples:

```text
new authorization node
removed audit edge
changed permission condition
new external call
```

The Delta Core provides the primary identity of the change.

---

## Delta Decision Intelligence

The capability to choose a useful structural change or growth trajectory based on current state, target state, historical deltas, constraints, feasibility, policy, and outcomes.

Canonical question:

> **Which historical delta or trajectory best moves the current structure toward the desired structure under current constraints?**

---

## Delta DNA

A compact structural identity used for fast Delta dispatch and localization.

Typical runtime:

```text
Raw Delta
    ↓
Delta DNA
    ↓
Relevant Delta CCC / Cluster
```

Delta DNA supports the first phase of Two-Phase Delta Search.

---

## Delta Episode

A bounded engineering change event containing one or more coordinated deltas.

Examples:

```text
security patch
migration step
feature addition
bug repair
refactoring event
```

A Delta Episode may preserve:

```text
before state
deltas
after state
reason
evidence
outcome
```

---

## Delta Folding

The process of converting repeated historical deltas into higher-level reusable transformation knowledge.

Typical progression:

```text
Historical Deltas
      ↓
Delta Cluster
      ↓
Delta CCC
      ↓
Delta DNA
```

---

## Delta Halo

The structurally affected neighborhood around the Delta Core.

It may include:

```text
callers
callees
guards
dependencies
data flows
reachable paths
policy-sensitive neighbors
```

The Delta Halo supports impact analysis and governance.

---

## Delta History

An ordered historical record of structural changes.

Example:

```text
Δ1
→ Δ2
→ Δ3
```

Delta History becomes the basis of a Delta Trajectory.

---

## Delta Intelligence

The runtime capability to reason about structural differences through:

```text
isolation
localization
retrieval
comparison
composition
validation
learning
```

See also **Structural Delta Intelligence — SDI**.

---

## Delta Knowledge Unit

A persistent record of one meaningful structural transformation.

Possible fields:

```text
beforeStructure
delta
afterStructure
taskContext
actionContext
constraints
reason
evidence
counterEvidence
outcome
policyStatus
```

---

## Delta Memory

Persistent structural memory describing how systems change.

It answers:

> **Where has this kind of structural change happened before?**

---

## Delta Metric Space

A searchable structural space in which Delta Objects are compared by features such as:

```text
Delta Core
Boundary
Task Meaning
Action Meaning
Constraints
Outcome
```

---

## Delta Object

A structured representation of meaningful change.

It may contain:

```text
Delta Core
Delta Halo
boundaries
raw changes
semantic class
constraints
mapping
reachability
evidence
confidence
```

---

## Delta Plane

Short form for the **Delta Structural Plane**.

---

## Delta Risk

A governance-oriented assessment of the structural significance of a delta.

Possible dimensions:

```text
privilege impact
data sensitivity
external reachability
guard changes
policy sensitivity
historical failures
```

Delta Risk can dispatch review depth.

---

## Delta-Scoped Governance

A governance strategy that begins from a structural delta rather than treating every new version as entirely unknown.

Canonical pattern:

```text
Reviewed Baseline
      ↓
Graph Minus
      ↓
Delta
      ↓
Delta Halo
      ↓
Changed Reachability
      ↓
Focused Governance
```

The scope may expand when structural effects require it.

---

## Delta Search

Retrieval of historical structural changes similar to a current delta.

Canonical question:

> **Where did a similar structural change happen before?**

Search modes may include:

```text
Exact Delta Match
Nearest Delta Match
Delta CCC Localization
Delta DNA Dispatch
Trajectory Search
```

---

## Delta Structural Plane

The fourth primary TACG-SDIG structural plane.

Canonical contents:

```text
1H — Task Delta

1I — Action Delta

1J — Task–Action Delta Pair

1K — Known Delta Collection

1L — Delta CCC / DNA

1M — Delta Trajectory

1N — Evidence / Outcome / Governance
```

---

## Delta Trajectory

An ordered history of structural deltas.

Conceptually:

```text
T = <Δ1, Δ2, ..., Δn>
```

Canonical definition:

> **A trajectory is an ordered history of observed or validated structural deltas over evolving structure.**

---

## Delta Trajectory Intelligence

The capability to analyze and reason over ordered structural change histories.

It can support:

```text
trajectory localization
next-delta recommendation
migration analysis
risk accumulation detection
evolution planning
```

---

## Delta Type

A semantic category assigned to a structural change.

Canonical TACG-SDIG types include:

```text
Missing
Extra
Changed
Conflicting
Unsafe
Unmapped
Unreachable
Redundant
Composite
```

---

## Direct Delta

The directly modified structural region before broader impact expansion.

Closely related to:

```text
Delta Core
```

---

## DNA

A compact structural identity used for dispatch or localization.

In TACG-SDIG, specialized forms include:

```text
Task DNA
Action DNA
Delta DNA
```

---

# E

## Engineering Evolution Memory

The combined memory of structural states, mappings, deltas, and trajectories.

Conceptually:

```text
Engineering Evolution Memory
=
Structure Memory
+
Mapping Memory
+
Delta Memory
+
Trajectory Memory
```

It preserves not only what systems are, but how they change and evolve.

---

## Engineering Structural Delta

A structurally meaningful engineering transformation rather than a raw graph edit.

Example:

```text
Insert Authorization Guard
```

rather than:

```text
add node
remove edge
add two edges
```

---

## Evidence Bundle

A collection of supporting and opposing evidence associated with a candidate delta.

Possible contents:

```text
positive historical cases
negative historical cases
task similarity
action similarity
policy results
runtime outcomes
rollback history
```

---

## Experience Loop

One of the three major TACG-SDIG loops.

```text
Historical Engineering Experience
      ↓
Delta Extraction
      ↓
Delta Folding
      ↓
Delta Memory
```

---

## Extra Delta

A structural behavior present in the observed or new system but absent from the expected or reference structure.

An Extra Delta often triggers the question:

> **Why does this behavior exist?**

---

# F

## Feasibility

Whether a candidate structural change can actually be realized within the current implementation environment.

Feasibility may depend on:

```text
available data
services
state
APIs
resources
dependencies
```

Feasibility is distinct from reachability.

---

## Fold

The process of compressing repeated structural experience into reusable structural knowledge.

Examples:

```text
structure → CCC
delta → Delta CCC
trajectory → Trajectory CCC
```

---

## Fold Back

The process of storing validated or rejected runtime experience back into structural memory.

Possible updates:

```text
Structure Memory
Mapping Memory
Delta Memory
Trajectory Memory
```

---

## Forward Graph Minus

Graph Minus used in the direction:

```text
Desired Structure
⊖
Current Structure
=
Required Delta
```

This supports planning and growth.

---

## Forward Walking

Incremental structural extension through local candidate moves.

In TACG-SDIG, the preferred form is constrained by Task and Action primitives, mappings, feasibility, and policy.

---

# G

## Governance Loop

One of the three major TACG-SDIG loops.

```text
Candidate / Observed Delta
      ↓
Task–Action Cross-Audit
      ↓
Reachability
      ↓
Policy / Security
      ↓
Counter-Evidence
      ↓
Governance Decision
```

---

## Governance Plane

A cross-cutting operational layer that evaluates the primary Task, Action, Mapping, and Delta structures.

It may contain:

```text
Policy CCCs
Risky Path CCCs
Governance TADPs
Counter-Evidence
Risk Dispatch
Review Outcomes
```

It is not treated as a fifth canonical knowledge plane.

---

## Governance TADP

A Task–Action Delta Pair enriched for governance analysis.

Possible fields:

```text
requiredTaskDelta
observedActionDelta
mappingStatus
policyContext
reachability
risk
evidence
decision
```

---

## Graph Minus

The core structural difference operator of TACG-SDIG.

Conceptually:

```text
Δ = Target ⊖ Reference
```

Graph Minus aims to isolate the smallest meaningful structural transformation rather than merely compute raw node or edge differences.

---

## Growth

A structural transition from one system state to another.

TACG-SDIG distinguishes:

```text
Candidate Growth
Validated Growth
```

Growth is not synonymous with adding nodes.

---

# H

## Historical TADP

A previously observed or validated Task–Action Delta Pair stored in Delta Memory.

Historical TADPs are strong candidate sources because they preserve both:

```text
why the system changed
↕
how the system changed
```

---

# I

## Impact Neighborhood

The region affected by a structural delta through dependencies, reachability, state interaction, or policy relevance.

Closely related to:

```text
Delta Halo
```

---

## Implementation Drift Delta

The difference between an approved structural change and the actual implemented change.

Conceptually:

```text
ΔDrift
=
ΔObserved
⊖
ΔApproved
```

This supports post-change governance.

---

## Intelligence Loop

One of the three main TACG-SDIG loops.

```text
Requirement
      ↓
Localization
      ↓
Graph Minus
      ↓
Delta Search
      ↓
Candidate Reconstruction
      ↓
Growth
```

---

# K

## Known ActionCG Collection — 1E

A repository of reusable historical Action/Code CallingGraphs.

It supports structural localization and Action-side search.

---

## Known Delta Collection — 1K

Persistent memory containing historical structural deltas and TADPs.

It supports Delta Search and folding.

---

## Known TaskCG Collection — 1B

A repository of reusable historical Task or Job CallingGraphs.

It supports Task-side localization and search.

---

# L

## Localization

The process of finding the closest relevant structural neighborhood in folded knowledge.

Typical forms:

```text
TaskCG Localization
ActionCG Localization
Delta Localization
CCC Localization
DNA Dispatch
Trajectory Localization
```

Canonical principle:

> **Localization finds where we are structurally.**

---

# M

## Mapping Memory

Persistent memory of Task–Action correspondence.

It answers:

```text
How was this task historically implemented?

What task intent historically explains this action structure?
```

---

## Mapping Plane

The TACG-SDIG structural plane centered on:

```text
1G — Task ↔ Action Mapping
```

It supports many-to-many correspondence across:

```text
nodes
edges
subgraphs
paths
CCC
DNA
```

---

## Minimal Feasible Structural Delta

The smallest local structural change that can validly move a current structure toward a desired state.

A related canonical statement is:

> **A move is a minimal feasible structural delta.**

---

## Missing Delta

A required structural element, relation, path, condition, or subgraph absent from the observed or reference system.

Examples:

```text
missing authorization
missing audit path
missing dependency
missing failure handling
```

---

# N

## Negative Delta Memory

Persistent memory of structural changes that:

```text
failed
were rejected
were rolled back
caused regression
violated policy
```

Negative Delta Memory is a major source of Counter-Evidence.

---

# O

## Outcome

Observed result associated with a structural delta or Delta Episode.

Examples:

```text
successful
failed
rolled back
partially successful
rejected
unknown
```

Outcomes are important for Delta ranking and learning.

---

# P

## Path Delta

A structural change involving a calling or task path.

Examples:

```text
New Calling Path

Removed Calling Path

New Bypass Path

Changed Failure Path

New External Reachability Path
```

---

## Policy CCC

A folded recurring structural policy pattern.

Examples:

```text
Privileged-Operation Guard CCC

Sensitive-Data Access CCC

External-Transfer Governance CCC
```

---

## Policy-Conditioned Graph Minus

Graph Minus interpreted through a policy perspective.

A structural change that appears ordinary under one perspective may become governance-critical under policy constraints.

---

## Primitive-Level Constrained Forward Walking

The process of closing a Residual Delta using one-step Task primitives and feasible Action primitives under structural constraints.

Canonical loop:

```text
Residual Delta
      ↓
Task Primitive
      ↓
Task → Action Mapping
      ↓
Action Primitive
      ↓
Reachability / Feasibility
      ↓
Next State
```

---

# R

## Reachability

Whether a structural node, path, or candidate delta can actually be reached from valid entry points.

Important principle:

```text
Presence
≠
Reachability
```

A security guard that exists but can be bypassed may not provide effective protection.

---

## Residual Delta

The part of a required delta not yet covered by a candidate solution.

Conceptually:

```text
Residual Delta
=
Target Delta
⊖
Candidate Coverage
```

Residual Delta enables recursive search and incremental reconstruction.

---

## Reverse Graph Minus

Graph Minus applied from observed implementation change back toward intended meaning.

Example:

```text
New ActionCG
⊖
Previous ActionCG
=
ΔA
```

followed by:

```text
ΔA
→
Task Mapping
```

This supports explanation and auditing.

---

## Risky-Path Localization

Structural search for newly introduced or existing calling paths matching known risky patterns.

Examples:

```text
Unauthenticated Request
→ Privileged Operation

Sensitive Data
→ External Destination
```

---

# S

## Search Before Generation

A core TACG-SDIG principle.

Preferred progression:

```text
Exact Known Solution
      ↓
Closest Structure
      ↓
Historical Delta
      ↓
Delta CCC / DNA
      ↓
Historical TADP
      ↓
Trajectory
      ↓
Primitive Walking
      ↓
Open Generation
```

---

## Security Delta

A structural change with security significance.

Examples:

```text
Add Authentication

Remove Authorization

Expand Privilege

Introduce External Data Transfer

Remove Validation Guard
```

---

## Security Delta CCC

A folded recurring security transformation.

Examples:

```text
Security Hardening Delta CCC

Security Regression Delta CCC
```

---

## Security Trajectory

An ordered history of security-relevant deltas.

Example:

```text
Open
→ Authenticated
→ Authorized
→ Audited
```

or a negative trajectory:

```text
Guard Relaxation
→ Privilege Expansion
→ Audit Reduction
```

---

## Structural Change Frontier

The primary governance-relevant region produced by:

```text
Graph Minus
+
Delta Halo
+
Changed Reachability
```

It defines the initial review scope.

---

## Structural Delta

A meaningful structural change between two system states.

It may involve:

```text
nodes
edges
paths
subgraphs
conditions
dependencies
constraints
mappings
reachability
```

---

## Structural Delta Intelligence — SDI

The capability to:

> **Identify, localize, retrieve, compare, compose, validate, and learn meaningful structural changes between known, observed, and desired system states.**

TACG-SDIG is a canonical AI coding realization of SDI.

---

## Structural Evolution Intelligence

The capability to reason not only about structural states and isolated deltas, but about longer-term sequences and patterns of change.

Typical progression:

```text
State
→ Delta
→ Trajectory
→ Evolution Intelligence
```

---

## Structural Evolution Trajectory

See **Delta Trajectory**.

---

## Structural Growth

A transition from one structural state to another through one or more deltas.

A stronger form is:

```text
Validated Structural Growth
```

---

## Structural Memory

Generic term for persistent folded structural knowledge.

Within TACG-SDIG, it includes:

```text
Structure Memory
Mapping Memory
Delta Memory
Trajectory Memory
```

---

## Structural Move

A candidate or validated transition:

```text
S --Δ--> S'
```

A structural move is analogous to a move in a state-transition problem.

---

## Structure Memory

Persistent memory of known system states and structures.

It answers:

> **Where have we seen a structure like this before?**

---

# T

## TACG-SDIG

**Task–Action CallingGraph Structural Delta Intelligence and Growth**

A structural AI coding framework centered on:

```text
Localization
Graph Minus
Delta Search
Candidate Reconstruction
Validation
Growth
Fold Back
```

---

## Task

A desired goal, requirement, job, or planning-side operation represented within the Task Structural Plane.

Tasks express intent rather than implementation.

---

## Task CallingGraph — TaskCG

A CallingGraph describing task intent, workflow, planning structure, or required operations.

It answers:

> **What needs to be done, and how are the required tasks structurally related?**

---

## Task Delta — ΔT

A meaningful structural change on the Task side.

Conceptually:

```text
ΔT =
Target TaskCG
⊖
Reference TaskCG
```

Example:

```text
Add Ownership Verification
before Resource Update
```

---

## Task Primitive

A small reusable one-step task move.

Canonical source:

```text
1C — Common-Sense One-Step Task / Job CGs
```

Examples:

```text
Verify Identity
Check Permission
Verify Ownership
Request Approval
Record Audit
```

---

## Task Structural Plane

One of the four primary TACG-SDIG structural planes.

It contains:

```text
1A — Task CG

1B — Known Task / Job CG Collection

1C — Task Primitives
```

---

## Task–Action Cross-Audit

Bidirectional structural review between Task and Action planes.

Task → Action asks:

```text
Where was this requirement implemented?
```

Action → Task asks:

```text
Why does this code exist?
```

---

## Task–Action Delta Pair — TADP

A paired representation of Task-side and Action-side structural change.

Conceptually:

```text
TADP
=
ΔT
↕
ΔA
```

A richer TADP may contain:

```text
Mapping
Context
Constraints
Evidence
Outcome
```

---

## TADP Seed

A preliminary Task–Action Delta Pair created during Graph Minus and early mapping.

It may later be enriched through:

```text
historical search
counter-evidence
feasibility
policy
validation
```

---

## Trajectory

An ordered sequence of structural deltas over evolving states.

Canonical form:

```text
T = <Δ1, Δ2, ..., Δn>
```

Canonical statement:

> **Structures describe states; deltas describe change; trajectories describe evolution.**

---

## Trajectory CCC

A folded recurring evolution pattern composed of ordered Delta CCCs or Delta Episodes.

Example:

```text
Open
→ Authenticate
→ Authorize
→ Audit
```

may form a security maturation Trajectory CCC.

---

## Trajectory DNA

A compact structural identity for dispatching or localizing trajectory patterns.

This is a future extension of the TACG-SDIG folding model.

---

## Trajectory Memory

Persistent memory of ordered structural change histories.

It answers:

> **How have systems of this kind typically evolved?**

---

## Trajectory Prefix Localization

Matching the current delta history against the beginning of known historical trajectories.

It supports:

```text
candidate next delta
trajectory continuation
evolution planning
```

---

## Two-Phase Delta Search

A two-stage Delta retrieval mechanism.

```text
Phase 1:
Delta DNA / Coarse Dispatch

Phase 2:
Detailed Structural Comparison
```

Detailed comparison may use:

```text
boundaries
context
mapping
constraints
outcome
counter-evidence
```

---

## Two-Way Delta Search

Bidirectional Delta retrieval across Task and Action memories.

Canonical directions:

```text
ΔT → Task Memory

ΔT → Action Memory

ΔA → Action Memory

ΔA → Task Memory
```

The Mapping Plane links the two sides.

---

## Two-Way Primitive Walking

Alternating Task-side and Action-side primitive extension.

Conceptually:

```text
Task Primitive
      ↓
Action Primitive
      ↓
Task Consistency
      ↓
Action Feasibility
      ↓
Next Move
```

---

# U

## Unfold

The process of reconstructing a candidate structure or transformation from folded structural knowledge.

Within TACG-SDIG:

```text
Target Delta
      ↓
Localization
      ↓
Folded Delta Knowledge
      ↓
Unfold
      ↓
Candidate TADP / Growth Path
```

---

## Unmapped Delta

A significant Task or Action delta lacking a valid mapping to the other structural plane or to an accepted policy/infrastructure explanation.

Example:

```text
New Action:
sendCustomerDataExternally()
```

with no corresponding Task or policy mapping.

Canonical governance question:

> **Why does this code exist?**

---

## Unreachable Delta

A structural change that exists in the graph but cannot be reached through valid execution or task paths.

Important distinction:

```text
Present
≠
Operationally Integrated
```

---

## Unsafe Delta

A structural change classified as potentially unsafe due to its semantic or reachability effects.

Examples:

```text
Remove Guard

Expand Privilege

Create Unvalidated Input Path

Add Sensitive External Data Flow
```

---

# V

## Validated Delta

A structural delta that has passed the required level of structural, operational, policy, security, runtime, or human validation.

A Validated Delta is a strong candidate for Fold Back.

---

## Validated Growth

A structural transition accepted after appropriate validation.

Conceptually:

```text
S --Δvalidated--> S'
```

---

# 1A–1N CANONICAL KNOWLEDGE MODEL

## 1A — Task CG

The current or target Task CallingGraph.

---

## 1B — Collection of Known Task / Job CGs

Historical or reusable Task structures.

---

## 1C — Common-Sense One-Step Task / Job CGs

Primitive Task moves used for local structural extension.

---

## 1D — Action / Code CG

The current, observed, or target Action CallingGraph.

---

## 1E — Collection of Known Action / Code CGs

Historical or reusable implementation structures.

---

## 1F — Common-Sense Feasible Action / Code Statements / CGs

Primitive feasible Action moves.

---

## 1G — Two-Way Task ↔ Action Mapping

Many-to-many mapping between Task and Action structural objects.

---

## 1H — Task Delta

Structural change on the Task side.

```text
ΔT
```

---

## 1I — Action Delta

Structural change on the Action side.

```text
ΔA
```

---

## 1J — Task–Action Delta Pair

Paired Task and Action change.

```text
TADP
```

---

## 1K — Known Delta Collection

Persistent historical Delta Memory.

---

## 1L — Delta CCC / Delta DNA

Folded and dispatchable recurring transformation knowledge.

---

## 1M — Delta Trajectory

Ordered structural evolution history.

---

## 1N — Evidence / Outcome / Governance

Supporting knowledge describing:

```text
success
failure
counter-evidence
policy
risk
review
runtime outcome
```

---

# CANONICAL DELTA TAXONOMY

## Missing Delta

Required structure is absent.

---

## Extra Delta

Observed structure contains additional behavior.

---

## Changed Delta

Existing structure changed semantically or structurally.

---

## Conflicting Delta

Task and Action structures contradict each other.

---

## Unsafe Delta

Change introduces or removes structure in a way that may create risk.

---

## Unmapped Delta

Change lacks a valid cross-plane or policy explanation.

---

## Unreachable Delta

Change exists but cannot be reached or integrated correctly.

---

## Redundant Delta

Change duplicates structure unnecessarily or ambiguously.

---

## Composite Delta

Several coordinated sub-deltas form one meaningful engineering transformation.

---

# FOUR MEMORY SYSTEMS

## Structure Memory

> **What systems are.**

---

## Mapping Memory

> **How Task and Action structures correspond.**

---

## Delta Memory

> **How systems change.**

---

## Trajectory Memory

> **How those changes evolve over time.**

---

# THREE TACG-SDIG LOOPS

## Experience Loop

```text
Historical Experience
      ↓
Delta Extraction
      ↓
Delta Folding
      ↓
Delta Memory
```

---

## Intelligence Loop

```text
Requirement
      ↓
Localization
      ↓
Graph Minus
      ↓
Delta Search
      ↓
Candidate Reconstruction
      ↓
Growth
```

---

## Governance Loop

```text
Task ↔ Action
      ↓
Delta
      ↓
Reachability
      ↓
Policy / Risk
      ↓
Counter-Evidence
      ↓
Governance Decision
```

---

# CANONICAL CLOSED LOOP

```text
FOLD
 ↓
LOCALIZE
 ↓
GRAPH MINUS
 ↓
DELTA
 ↓
TWO-WAY SEARCH
 ↓
UNFOLD / RECONSTRUCT
 ↓
VALIDATE
 ↓
GROW
 ↓
FOLD BACK
 ↺
```

---

# CANONICAL STATEMENTS

> **Delta is a first-class structural knowledge object.**

> **Search before generation.**

> **Intelligence may come not only from generating better candidates, but from making fewer candidates necessary.**

> **Localization finds where we are; Graph Minus tells us what changed or what is missing.**

> **Similarity finds candidates; structural and operational validation determines whether a candidate can live inside the target system.**

> **Structures describe states; deltas describe change; trajectories describe evolution.**

> **A trajectory is an ordered history of observed or validated structural deltas over evolving structure.**

> **Code captures implementation states; structural deltas capture engineering change; delta trajectories capture engineering experience.**

> **Code tells AI what the system is; Delta tells AI how the system grows.**

> **Govern not only the new code; govern the structural change it introduces.**

---

## TACG-SDIG

**Task–Action CallingGraph Structural Delta Intelligence and Growth**

> **From known structure, to meaningful difference, to validated growth.**
