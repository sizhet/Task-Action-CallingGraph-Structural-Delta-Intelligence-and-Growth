# Task–Action CallingGraph Structural Delta Intelligence and Growth

## TACG-SDIG

**Two-Way Localization, Delta Search, Trajectory Learning, and Structural Governance for AI Coding**

---

## Overview

AI coding is often framed as a generation problem:

```text
Requirement
    ↓
Generate Code
```

TACG-SDIG starts from a different observation:

> **Experienced engineers rarely solve every new problem from scratch. They localize what is already known, identify what is different, search for how similar differences were solved before, validate the candidate change, and preserve the result as new experience.**

This repository develops that process as a structural AI framework:

```text
Folded Engineering Experience
            ↓
       Localization
            ↓
        Graph Minus
            ↓
     Structural Delta
            ↓
 Two-Way Delta Search
            ↓
Candidate Reconstruction
            ↓
Reachability / Feasibility
            ↓
 Governance / Validation
            ↓
          Growth
            ↓
        Fold Back
            ↺
```

The central object is the **Structural Delta**.

> **Delta is a first-class structural knowledge object.**

Rather than reasoning only about what a software system *is*, TACG-SDIG also reasons about:

```text
what changed
why it changed
what remains missing
how similar changes were solved
whether a candidate change is feasible
whether the change is safe and compliant
what happened after the change
how changes accumulate into trajectories
```

This turns software change itself into an AI knowledge object.

---

# 1. Core Idea

Suppose a known system already implements:

```text
Authenticate
    ↓
Load Resource
    ↓
Update Resource
```

A new requirement says:

```text
Only the resource owner may update it.
```

A generation-centric approach may reopen a large implementation space.

TACG-SDIG first localizes the closest known structure and computes:

```text
Required TaskCG
      ⊖
Known TaskCG
      ↓
ΔT
```

and:

```text
Required ActionCG
      ⊖
Known ActionCG
      ↓
ΔA
```

The important missing structure may be only:

```text
Verify Ownership
```

The problem has changed from:

```text
How do we generate the program?
```

to:

```text
How have we crossed this structural gap before?
```

That is the starting point of **Structural Delta Intelligence**.

---

# 2. Structural Delta Intelligence

TACG-SDIG defines **Structural Delta Intelligence — SDI** as:

> **The capability to identify, localize, retrieve, compare, compose, validate, and learn meaningful structural changes between known, observed, and desired system states.**

Its canonical AI coding sequence is:

```text
Localization
    ↓
Graph Minus
    ↓
Delta Isolation
    ↓
Delta Search
    ↓
Candidate Reconstruction
    ↓
Validation
    ↓
Growth
```

The framework follows a strong principle:

> **Search before generation.**

Generation becomes progressively more open only when reusable structural experience is insufficient.

---

# 3. The Four Structural Planes

TACG-SDIG organizes its primary knowledge into four structural planes.

## I. Task Structural Plane

```text
1A — Task CG

1B — Collection of Known Task / Job CGs

1C — Common-Sense One-Step Task / Job CGs
```

This plane represents:

```text
what needs to be done
known task structures
primitive task moves
```

---

## II. Action Structural Plane

```text
1D — Action / Code CG

1E — Collection of Known Action / Code CGs

1F — Common-Sense Feasible Action / Code Statements / CGs
```

This plane represents:

```text
what the implementation does
known implementation structures
feasible primitive action moves
```

---

## III. Mapping Plane

```text
1G — Two-Way Mapping
     Task CG Elements
          ↕
     Action / Code CG Elements
```

The mapping is not merely a lookup table.

It may connect:

```text
node ↔ node
edge ↔ edge
subgraph ↔ subgraph
path ↔ path
CCC ↔ CCC
DNA ↔ DNA
```

and supports both directions:

```text
Task → Action
Action → Task
```

This enables a fundamental engineering question:

> **What we intended ↔ What we implemented.**

---

## IV. Delta Structural Plane

The Delta Plane makes structural change persistent and searchable.

It includes:

```text
1H — Task Delta

1I — Action Delta

1J — Task–Action Delta Pair

1K — Known Delta Collection

1L — Delta CCC / Delta DNA

1M — Delta Trajectory

1N — Evidence / Outcome / Governance
```

The Delta Plane supports:

```text
Delta Localization
Delta Search
Delta Clustering
Delta Folding
Delta Governance
Delta Trajectory Analysis
Delta Growth
```

---

# 4. Graph Minus

A core TACG-SDIG operation is:

```text
Graph Minus
```

Conceptually:

```text
ΔT = Required TaskCG ⊖ Closest Known TaskCG
```

and:

```text
ΔA = Required ActionCG ⊖ Closest Known ActionCG
```

But Graph Minus is **not ordinary set subtraction**.

It may identify:

```text
Missing Node
Missing Edge
Missing Subgraph
Missing Calling Path

Changed Ordering
Changed Dependency
Changed Condition
Changed Constraint

Changed Role
Changed State Transition
Changed Reachability
Changed Mapping
```

The result is a semantic and structural difference.

---

# 5. Delta Taxonomy

Not every important difference is simply "missing."

TACG-SDIG distinguishes several useful delta classes:

```text
Missing Delta

Extra Delta

Changed Delta

Conflicting Delta

Unsafe Delta

Unmapped Delta

Unreachable Delta

Redundant Delta
```

For example, an ActionCG may contain a significant new behavior with no corresponding Task, policy, or architectural mapping.

That produces an important governance question:

> **Why does this code exist?**

---

# 6. Task–Action Delta Pair

Task and Action changes should often be analyzed together.

TACG-SDIG introduces the **Task–Action Delta Pair — TADP**:

```text
TADP
{
    ΔT,
    ΔA,
    Mapping,
    Context,
    Constraints,
    Evidence,
    Outcome
}
```

This provides a reusable unit connecting:

```text
Required Change
        ↕
Implementation Change
```

A TADP can itself become historical engineering knowledge.

---

# 7. Two-Way Delta Search

After Graph Minus identifies the structural gap, TACG-SDIG searches both sides.

```text
              ΔT
             ↙  ↘
     Task Memory   Mapping
          ↓           ↓
     Task Delta     Action Delta
       Search         Search
          ↘           ↙
              ΔA
```

The runtime can search:

```text
Exact Delta Match

Nearest Delta Match

Delta CCC

Delta DNA

Historical TADP

Delta Trajectory

Counter-Evidence
```

This changes the search target from:

```text
Where is similar code?
```

to:

> **Where did a similar structural change happen?**

---

# 8. Candidate Reconstruction

Historical experience is rarely copied blindly.

Instead:

```text
Historical Delta
        +
Current Structural Context
        ↓
Candidate Reconstruction
```

The reconstructed candidate is evaluated against:

```text
Task Compatibility

Action Feasibility

Reachability

Dependencies

Constraints

Policy

Security

Historical Outcomes

Counter-Evidence
```

A central rule is:

> **Similarity finds candidates; structural and operational validation determines whether a candidate can live inside the target system.**

---

# 9. Residual Delta

A historical candidate may solve only part of the problem.

TACG-SDIG therefore computes:

```text
Residual Delta
=
Required Delta
⊖
Candidate Coverage
```

The residual becomes another structural search target.

This allows incremental problem solving:

```text
Large Gap
   ↓
Known Delta
   ↓
Smaller Residual
   ↓
Another Search
   ↓
Smaller Residual
```

---

# 10. Primitive-Level Constrained Forward Walking

When historical Delta Memory can no longer close the residual gap, TACG-SDIG can fall back to:

```text
1C — Task Primitives
```

and:

```text
1F — Feasible Action Primitives
```

The runtime performs:

```text
Residual Task Delta
        ↓
Candidate Task Primitive
        ↓
Task → Action Mapping
        ↓
Feasible Action Primitive
        ↓
Reachability / Feasibility
        ↓
Next Structural State
```

This is:

> **Two-Way Primitive-Level Constrained Forward Walking.**

The system opens the search space gradually rather than immediately returning to unrestricted generation.

---

# 11. A Move as a Structural Delta

A useful abstraction is:

```text
S --Δ--> S'
```

where:

```text
S  = current structural state
Δ  = candidate structural change
S' = resulting structural state
```

This connects TACG-SDIG with a general state-transition view of intelligence.

A concise principle is:

> **A move is a minimal feasible structural delta.**

Chess and Go provide an intuitive analogy:

```text
Board State
↔
Current Structural State

Move
↔
Delta

Legal Move
↔
Feasible Delta

Move History
↔
Delta Trajectory
```

Software engineering is much more open-ended, but the structural idea is useful.

---

# 12. Delta Memory

Successful and failed engineering changes should not disappear after a coding task.

TACG-SDIG folds them into:

```text
Delta Memory
```

A Delta Knowledge Unit may preserve:

```text
Before Structure

Delta

After Structure

Task Context

Action Context

Constraints

Reason

Outcome

Evidence

Counter-Evidence

Policy Status
```

Thus:

> **Fold not only what systems look like, but how systems change.**

---

# 13. Four Memory Systems

TACG-SDIG distinguishes four complementary memories.

```text
Structure Memory
=
What systems are
```

```text
Mapping Memory
=
How Task and Action structures correspond
```

```text
Delta Memory
=
How systems change
```

```text
Trajectory Memory
=
How sequences of changes evolve
```

Together:

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

---

# 14. From Delta to CCC and DNA

Repeated structural changes can be clustered.

```text
Historical Deltas
      ↓
Delta Cluster
      ↓
Delta CCC
      ↓
Delta DNA
```

Examples may include:

```text
Authorization-Guard Delta CCC

Retry-and-Recovery Delta CCC

Security-Hardening Delta CCC

Service-Extraction Delta CCC

External-API-Migration Delta CCC
```

Delta DNA can provide compact structural dispatch into the appropriate transformation neighborhood.

---

# 15. Delta Trajectory

Suppose a system evolves:

```text
S0 --Δ1--> S1
S1 --Δ2--> S2
S2 --Δ3--> S3
```

Then:

```text
T = <Δ1, Δ2, Δ3>
```

is a **Structural Evolution Trajectory**.

This gives a compact definition:

> **A trajectory is an ordered history of observed or validated structural deltas over evolving structure.**

Therefore:

> **Structures describe states. Deltas describe change. Trajectories describe evolution.**

---

# 16. Engineering Experience as Trajectory

A distributed system might evolve through:

```text
Remote Call
    ↓
Add Timeout
    ↓
Add Retry
    ↓
Add Idempotency
    ↓
Add Circuit Breaker
    ↓
Add Observability
```

This is more than a collection of patches.

It is an engineering evolution trajectory.

A future system may localize within such a trajectory and ask:

```text
Where are we?

What historically came next?

Which next delta fits our current constraints?
```

Trajectory Memory therefore connects historical engineering experience with future structural decision support.

---

# 17. Counter-Evidence

TACG-SDIG searches not only for successful precedent.

It also asks:

> **Where did a similar delta fail?**

For example:

```text
Candidate:
Add Retry
```

Positive precedent:

```text
Retry handled transient failures.
```

Counter-evidence:

```text
Retry duplicated non-idempotent mutations.
```

The reconstructed candidate may therefore become:

```text
Add Idempotency
      +
Add Retry
```

This is an important distinction between structural intelligence and simple similarity retrieval.

---

# 18. Delta-Scoped Structural Governance

AI coding can generate structural change rapidly.

Governance must therefore scale with change.

TACG-SDIG proposes:

> **Delta-Scoped Structural Governance**

The basic workflow is:

```text
Reviewed Baseline
      ↓
New TaskCG / ActionCG
      ↓
Graph Minus
      ↓
Delta Core
      ↓
Risk-Conditioned Delta Halo
      ↓
Changed Reachability
      ↓
Task ↔ Action Cross-Audit
      ↓
Policy / Security Analysis
      ↓
Counter-Evidence
      ↓
Validation
```

The principle is:

> **Use structural change to determine where governance attention should concentrate.**

---

# 19. Delta Core and Delta Halo

The **Delta Core** contains directly changed structure.

Examples:

```text
added authorization node
removed audit edge
changed API destination
expanded privilege
modified failure path
```

The **Delta Halo** contains structurally affected neighbors:

```text
callers
callees
guards
dependencies
reachable paths
data flows
policy-sensitive neighbors
```

Therefore:

> **Governance scope should follow structural effect, not merely edit location.**

---

# 20. Governance Must Be Able to Escape Locality

Delta-scoped governance does **not** mean:

```text
Only inspect changed nodes.
```

Some changes affect:

```text
shared authentication
global configuration
core routing
common data models
system-wide privileges
```

The review process can therefore expand:

```text
Delta Core
    ↓
Local Halo
    ↓
Extended Reachability
    ↓
System-Wide Review
```

when risk or uncertainty requires it.

A central governance principle is:

> **Baseline what is already known; isolate what changed; expand only as structural consequences require; escalate when locality is no longer trustworthy.**

---

# 21. Task–Action Cross-Audit

The Mapping Plane enables two important questions.

From Task to Action:

```text
Where was this requirement implemented?
```

From Action to Task:

```text
Why does this code exist?
```

This allows:

```text
What We Intended
        ↕
What We Implemented
```

to become a structural governance operation.

---

# 22. Security as Structural Delta Analysis

Suppose policy expects:

```text
Sensitive Data Access
        ↓
Authentication
        ↓
Authorization
        ↓
Audit
        ↓
Data Access
```

but the new ActionCG contains:

```text
Authentication
        ↓
Data Access
```

Graph Minus exposes:

```text
Missing Safety Delta
=
Authorization
+
Audit
```

TACG-SDIG therefore supports at least two broad security operations:

```text
Missing-Safety-Structure Detection
```

and:

```text
Known-Risky-Structure Localization
```

---

# 23. Reachability Matters

Security cannot be reduced to checking whether a guard exists somewhere.

For example:

```text
        ┌→ Authorization ─┐
Input ──┤                 ├→ Sensitive Action
        └─────────────────┘
```

contains an authorization node but also a bypass.

Therefore:

```text
Presence
≠
Effective Protection
```

Structural governance must reason about relevant calling paths and reachability.

---

# 24. Governance Boundary

TACG-SDIG does not claim to replace:

```text
testing
static analysis
dynamic analysis
formal verification
penetration testing
security specialists
human review
```

Its claim is narrower and more practical:

> **Structural deltas provide a systematic, scalable, and explainable focus for governance analysis.**

---

# 25. Human Engineering Practice

TACG-SDIG is strongly motivated by recurring senior-engineering behavior.

A human engineer may ask:

```text
Where is the relevant structure?

What is different?

Have we solved this before?

How did we solve it?

Did that solution fail anywhere?

Can it work here?

What else must change with it?

What remains missing?

What is the smallest next feasible step?

Does the final system actually work?
```

TACG-SDIG translates these into:

```text
Localization

Graph Minus

Delta Search

Candidate Reconstruction

Counter-Evidence

Feasibility

Companion Delta Search

Residual Delta

Primitive Forward Walking

Validation
```

This is a MET-style structuralization of engineering practice.

---

# 26. Three Major Engineering Values

TACG-SDIG has three major engineering roles.

## I. Engineering Experience Evolution

```text
Human / Historical Experience
      ↓
Delta Extraction
      ↓
Delta Memory
      ↓
Delta CCC / DNA
      ↓
Delta Trajectory
```

Engineering experience becomes searchable and evolvable.

---

## II. AI Coding Intelligence

```text
Requirement
      ↓
Localization
      ↓
Graph Minus
      ↓
Small Delta Space
      ↓
Historical Delta Search
      ↓
Candidate Reconstruction
```

This can reduce unnecessary candidate enumeration.

> **Intelligence may come not only from generating better candidates, but from making fewer candidates necessary.**

---

## III. Structural Governance

```text
Reviewed Baseline
      ↓
Delta
      ↓
Adaptive Structural Scope
      ↓
Task–Action Cross-Audit
      ↓
Policy / Security
      ↓
Validation
```

Delta becomes a governance dispatch unit.

---

# 27. Three Interacting Loops

The architecture can be summarized through three loops.

## Experience Loop

```text
Engineering Experience
      ↓
Structural Folding
      ↓
Delta Memory
```

## Intelligence Loop

```text
Requirement
      ↓
Localization
      ↓
Delta
      ↓
Search
      ↓
Growth
```

## Governance Loop

```text
Candidate Delta
      ↓
Task–Action Cross-Audit
      ↓
Reachability
      ↓
Policy / Security
      ↓
Validation
```

All three feed:

```text
Outcome
   ↓
Fold Back
```

---

# 28. Canonical Closed Loop

The complete TACG-SDIG runtime is:

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

Or in words:

> **Fold stores experience.**

> **Localization finds where we are.**

> **Delta identifies what is missing.**

> **Two-way search finds how others crossed that gap.**

> **Unfolding reconstructs a candidate path.**

> **Validation decides whether the path is real.**

> **Growth changes the system.**

> **Fold Back converts the result into future structural intelligence.**

---

# 29. Seven Core Articles

The repository is organized around seven primary articles.

### TACG-SDIG-001

**From CallingGraph Knowledge to Structural Delta Intelligence**

Introduces Structural Delta Intelligence, the overall framework, and the transition from CallingGraph knowledge to delta-centered AI coding.

---

### TACG-SDIG-002

**Four Structural Planes and the Canonical Knowledge Model**

Formalizes the Task, Action, Mapping, and Delta planes and the canonical `1A–1N` knowledge model.

---

### TACG-SDIG-003

**Graph Minus and Task–Action Delta Isolation**

Defines Graph Minus as semantic structural differencing and develops Task/Action delta extraction and classification.

---

### TACG-SDIG-004

**Two-Way Delta Localization, Search, and Candidate Reconstruction**

Develops Delta localization, two-way Task/Action search, candidate reconstruction, counter-evidence, feasibility, and residual-delta closure.

---

### TACG-SDIG-005

**Delta Memory, Folding, and Structural Evolution Trajectories**

Develops Delta Memory, Delta CCC/DNA, Delta Episodes, and structural evolution trajectories.

---

### TACG-SDIG-006

**Delta-Scoped Structural Governance and Security**

Develops baseline-plus-delta governance, Delta Core/Halo, changed reachability, cross-plane auditing, policy, and security analysis.

---

### TACG-SDIG-007

**From Human Engineering Practice to AI Coding Growth**

Connects senior engineering practice with the complete TACG-SDIG closed-loop runtime and structural continual growth.

---

# 30. Canonical Figures

The repository contains seven companion figures:

```text
Fig-001-TACG-SDIG-Grand-Map.png

Fig-002-Four-Structural-Planes-and-1A-1N-Knowledge-Model.png

Fig-003-Graph-Minus-and-Task-Action-Delta-Pair.png

Fig-004-Two-Way-Delta-Search-and-Growth-Runtime.png

Fig-005-Delta-Memory-and-Structural-Evolution-Trajectory.png

Fig-006-Delta-Scoped-Governance-and-Security.png

Fig-007-Human-Engineering-Experience-to-Structural-AI-Coding.png
```

Together they provide a visual path from the knowledge model to the complete AI coding growth loop.

---

# 31. Repository Structure

```text
Task-Action-CallingGraph-Structural-Delta-Intelligence-and-Growth/
│
├── README.md
├── START-HERE.md
├── CONTENTS.md
├── GLOSSARY.md
├── FIGURE-INDEX.md
├── FUTURE-DIRECTIONS.md
├── CHANGELOG.md
├── CITATION.cff
├── .zenodo.json
│
├── docs/
│   ├── TACG-SDIG-001-From-CallingGraph-Knowledge-to-Structural-Delta-Intelligence.md
│   ├── TACG-SDIG-002-Four-Structural-Planes-and-the-Canonical-Knowledge-Model.md
│   ├── TACG-SDIG-003-Graph-Minus-and-Task-Action-Delta-Isolation.md
│   ├── TACG-SDIG-004-Two-Way-Delta-Localization-Search-and-Candidate-Reconstruction.md
│   ├── TACG-SDIG-005-Delta-Memory-Folding-and-Structural-Evolution-Trajectories.md
│   ├── TACG-SDIG-006-Delta-Scoped-Structural-Governance-and-Security.md
│   └── TACG-SDIG-007-From-Human-Engineering-Practice-to-AI-Coding-Growth.md
│
└── figures/
    ├── Fig-001-TACG-SDIG-Grand-Map.png
    ├── Fig-002-Four-Structural-Planes-and-1A-1N-Knowledge-Model.png
    ├── Fig-003-Graph-Minus-and-Task-Action-Delta-Pair.png
    ├── Fig-004-Two-Way-Delta-Search-and-Growth-Runtime.png
    ├── Fig-005-Delta-Memory-and-Structural-Evolution-Trajectory.png
    ├── Fig-006-Delta-Scoped-Governance-and-Security.png
    └── Fig-007-Human-Engineering-Experience-to-Structural-AI-Coding.png
```

---

# 32. Relationship to the Structural Folding / Unfolding Framework

TACG-SDIG can be viewed as a concrete AI coding realization of a broader structural folding and unfolding framework.

```text
Historical Experience
      ↓
Structural Folding
      ↓
Folded Memory
      ↓
Localization
      ↓
Delta
      ↓
Structural Unfolding
      ↓
Candidate Growth
      ↓
Validation
      ↓
New Experience
      ↓
Fold Back
```

A useful distinction is:

> **Structural Folding and Unfolding explains how structural experience can be stored, localized, and reconstructed.**

> **TACG-SDIG focuses on intelligence acting on the difference between what exists and what is needed.**

---

# 33. Relationship to CallingGraph AI Coding

CallingGraph provides a structural representation of:

```text
tasks
actions
dependencies
paths
execution relationships
```

TACG-SDIG adds the evolutionary dimension:

```text
CallingGraph
      ↓
CallingGraph Difference
      ↓
Structural Delta
      ↓
Delta Search
      ↓
CallingGraph Growth
```

The result moves from:

```text
Structural Representation
```

toward:

```text
Structural Evolution Intelligence
```

---

# 34. Progressive MET Path

The framework does not require the full architecture to be implemented at once.

A practical progression is:

```text
Level 0
TaskCG / ActionCG Representation

Level 1
Known Structural Memory

Level 2
Task ↔ Action Mapping

Level 3
Localization

Level 4
Graph Minus

Level 5
Delta Memory

Level 6
Two-Way Delta Search

Level 7
Candidate Reconstruction

Level 8
Residual Delta

Level 9
Primitive Forward Walking

Level 10
Reachability / Feasibility

Level 11
Delta CCC / DNA

Level 12
Trajectory Memory

Level 13
Delta-Scoped Governance

Level 14
Validated Growth

Level 15
Continual Fold Back
```

This keeps the research program compatible with incremental engineering experimentation.

---

# 35. Research Scope

TACG-SDIG currently focuses on:

```text
AI Coding

Task / Action CallingGraphs

Structural Localization

Structural Difference

Delta Search

Engineering Evolution Memory

Structural Governance
```

Potential future applications may extend the same principles to other domains where systems evolve through meaningful structural changes.

Those extensions remain research directions rather than assumptions of the current implementation.

---

# 36. Core Principles

The repository is built around several recurring principles.

### 1. Delta is a first-class structural knowledge object.

### 2. Search before generation.

### 3. Intelligence may come not only from generating better candidates, but from making fewer candidates necessary.

### 4. Structures describe states; deltas describe change; trajectories describe evolution.

### 5. A trajectory is an ordered history of observed or validated structural deltas over evolving structure.

### 6. Code captures implementation states; structural deltas capture engineering change; delta trajectories capture engineering experience.

### 7. Similarity retrieves candidates; validation determines whether they belong in the current system.

---

# 37. A Candidate Learning Unit for AI Coding

A central hypothesis of TACG-SDIG is:

> **The basic learning unit of AI coding may be not only Code or CallingGraph, but a validated Structural Delta.**

A validated Delta can preserve:

```text
Before State

Task Requirement

Structural Difference

Implemented Change

Task–Action Mapping

Constraints

Evidence

Outcome
```

This makes it simultaneously:

```text
a change unit
a learning unit
a search unit
a governance unit
an evolution unit
```

---

# 38. Final Perspective

Software repositories preserve code.

CallingGraphs preserve structural relationships.

TACG-SDIG asks whether AI coding systems should additionally preserve:

```text
how systems changed
why they changed
which changes succeeded
which changes failed
which changes usually occur together
which sequences form recurring evolution paths
```

That leads to a progression:

```text
CODE
 ↓
STRUCTURE
 ↓
DELTA
 ↓
TRAJECTORY
 ↓
STRUCTURAL EVOLUTION INTELLIGENCE
```

The central idea can be stated simply:

> **Code tells AI what the system is; Delta tells AI how the system grows.**

And when deltas accumulate:

> **Delta trajectories tell AI how engineering experience evolves.**

TACG-SDIG therefore treats AI coding not merely as code generation, but as a closed-loop process of:

```text
STRUCTURAL MEMORY
      ↓
LOCALIZATION
      ↓
DELTA INTELLIGENCE
      ↓
VALIDATED GROWTH
      ↓
STRUCTURAL EVOLUTION
      ↓
NEW MEMORY
      ↺
```

---

## TACG-SDIG

**Task–Action CallingGraph Structural Delta Intelligence and Growth**

> **From known structure, to meaningful difference, to validated growth.**
