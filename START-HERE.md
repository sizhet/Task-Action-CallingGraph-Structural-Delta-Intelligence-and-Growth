# START HERE — TACG-SDIG

## Task–Action CallingGraph Structural Delta Intelligence and Growth

**A 10–15 Minute Guide to the Repository**

---

# 1. What Is TACG-SDIG?

TACG-SDIG studies a simple but important question:

> **If most of a software system is already known, can AI focus on the meaningful structural difference instead of regenerating the whole solution?**

The framework begins with:

```text
Known Structure
      ↓
New Requirement or New Code
      ↓
Localization
      ↓
Graph Minus
      ↓
Structural Delta
```

Then it asks:

```text
Where has a similar delta appeared before?

How was it implemented?

Did it work?

What failed?

Can that historical change fit here?
```

The result is a structural AI coding runtime centered on **Delta Intelligence**.

---

# 2. The One-Sentence Idea

The shortest description is:

> **Localize what is already known, isolate what is different, search how similar differences were crossed before, validate the candidate change, and fold the result back into structural memory.**

---

# 3. The Canonical Loop

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

This is the central runtime of TACG-SDIG.

---

# 4. Why Delta?

Suppose the known TaskCG is:

```text
Authenticate
    ↓
Update Resource
```

The new requirement is:

```text
Authenticate
    ↓
Verify Ownership
    ↓
Update Resource
```

The main engineering problem is not the entire graph.

It is:

```text
ΔT:
Add Verify Ownership
```

Similarly, the ActionCG may change from:

```text
authenticate()
    ↓
updateResource()
```

to:

```text
authenticate()
    ↓
checkOwner()
    ↓
updateResource()
```

giving:

```text
ΔA:
Add checkOwner()
```

The pair:

```text
ΔT
 ↕
ΔA
```

is a **Task–Action Delta Pair — TADP**.

---

# 5. The Four Structural Planes

TACG-SDIG uses four primary knowledge planes.

## Task Structural Plane

```text
1A — Task CG
1B — Known Task / Job CG Collection
1C — One-Step Task / Job Primitives
```

This plane represents:

```text
what needs to be done
```

---

## Action Structural Plane

```text
1D — Action / Code CG
1E — Known Action / Code CG Collection
1F — Feasible Action / Code Primitives
```

This plane represents:

```text
what the implementation does
```

---

## Mapping Plane

```text
1G — Task ↔ Action Mapping
```

This connects:

```text
Task Node ↔ Action Node
Task Path ↔ Action Path
Task CCC ↔ Action CCC
Task DNA ↔ Action DNA
```

and supports:

```text
Task → Action
Action → Task
```

---

## Delta Structural Plane

```text
1H — Task Delta
1I — Action Delta
1J — TADP
1K — Known Delta Collection
1L — Delta CCC / DNA
1M — Delta Trajectory
1N — Evidence / Outcome / Governance
```

This plane represents:

```text
how systems change
```

---

# 6. Graph Minus

The core operation is:

```text
Target
   ⊖
Reference
   ↓
Structural Delta
```

For TaskCG:

```text
ΔT = TargetTaskCG ⊖ ReferenceTaskCG
```

For ActionCG:

```text
ΔA = TargetActionCG ⊖ ReferenceActionCG
```

But Graph Minus is not ordinary node or edge subtraction.

It may identify:

```text
missing nodes
missing edges
missing paths
changed order
changed dependency
changed conditions
changed constraints
changed reachability
changed mappings
```

The goal is:

> **Find the smallest meaningful structural transformation.**

---

# 7. Delta Core and Delta Halo

Every important delta has two useful regions.

```text
DELTA CORE
=
directly changed structure
```

and:

```text
DELTA HALO
=
the structurally affected neighborhood
```

Example:

```text
Caller
  ↓
[ New Authorization Guard ]
  ↓
Protected Operation
```

The Core is the new guard.

The Halo may include:

```text
callers
protected operations
alternate paths
policy-sensitive dependencies
```

This becomes especially important for governance.

---

# 8. Two-Way Delta Search

After isolating the delta, TACG-SDIG searches both Task and Action memories.

From Task Delta:

```text
ΔT
 ↓
Task Delta Search
 ↓
Historical Task Changes
 ↓
Task–Action Mapping
 ↓
Candidate ΔA
```

From Action Delta:

```text
ΔA
 ↓
Action Delta Search
 ↓
Historical Action Changes
 ↓
Action–Task Mapping
 ↓
Candidate ΔT
```

The two directions reinforce each other.

---

# 9. Search Before Generation

TACG-SDIG prefers this ladder:

```text
Exact Known Solution
        ↓
Closest Known Structure
        ↓
Exact Delta
        ↓
Nearest Delta
        ↓
Delta CCC / DNA
        ↓
Historical TADP
        ↓
Historical Trajectory
        ↓
Primitive Forward Walking
        ↓
Open Generation
```

The principle is:

> **Search before generation.**

---

# 10. Candidate Reconstruction

A historical solution rarely fits perfectly.

Therefore TACG-SDIG performs:

```text
Historical Delta
      +
Current Context
      ↓
Candidate Reconstruction
```

The candidate is checked for:

```text
structural similarity
boundary compatibility
task fit
action feasibility
reachability
constraints
policy
security
historical outcome
counter-evidence
```

A useful rule is:

> **Similarity finds candidates; validation determines whether they can live inside the target system.**

---

# 11. Counter-Evidence

The system does not only ask:

```text
Where did this delta succeed?
```

It also asks:

```text
Where did this delta fail?
```

Example:

```text
Candidate:
Add Retry
```

Positive experience:

```text
Worked for transient read failures.
```

Negative experience:

```text
Caused duplicate non-idempotent mutations.
```

The candidate may therefore require:

```text
Add Idempotency
+
Add Retry
```

This is **Counter-Evidence Search**.

---

# 12. Residual Delta

A historical candidate may solve only part of the target.

Then:

```text
Residual Delta
=
Required Delta
⊖
Candidate Coverage
```

The residual becomes another search object.

This allows:

```text
Large Problem
   ↓
Known Partial Solution
   ↓
Smaller Residual
   ↓
Next Search
```

---

# 13. Primitive Forward Walking

When historical knowledge is insufficient, TACG-SDIG can use:

```text
1C — Task Primitives
```

and:

```text
1F — Action Primitives
```

to move forward one feasible step at a time.

Example:

```text
Authenticate
      ↓
?
      ↓
Modify Resource
```

Task candidates:

```text
Verify Ownership
Check Permission
Request Approval
Audit
```

The runtime chooses a Task primitive, maps it to feasible Action primitives, validates it, and continues.

This is:

> **Primitive-Level Constrained Forward Walking.**

---

# 14. Delta Memory

A successful or failed delta should not disappear after use.

TACG-SDIG stores:

```text
Before Structure
Delta
After Structure
Reason
Context
Constraints
Evidence
Counter-Evidence
Outcome
```

This forms **Delta Memory**.

---

# 15. Four Memory Systems

TACG-SDIG distinguishes:

```text
Structure Memory
=
what systems are
```

```text
Mapping Memory
=
how Task and Action correspond
```

```text
Delta Memory
=
how systems change
```

```text
Trajectory Memory
=
how changes evolve over time
```

Together they form:

```text
Engineering Evolution Memory
```

---

# 16. Delta CCC and Delta DNA

Repeated transformations can be folded.

Example historical deltas:

```text
Add permission check before update

Add ownership check before delete

Add role check before export
```

may fold into:

```text
Authorization Guard Delta CCC
```

Then:

```text
Delta
 ↓
Delta DNA
 ↓
Relevant Delta CCC
 ↓
Historical Instances
```

supports fast runtime dispatch.

---

# 17. Delta Trajectory

Suppose:

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

A useful definition is:

> **A trajectory is an ordered history of observed or validated structural deltas over evolving structure.**

---

# 18. The Three Core Statements

Keep these three statements in mind while reading the repository.

> **Structures describe states.**

> **Deltas describe change.**

> **Trajectories describe evolution.**

And:

> **Code captures implementation states; structural deltas capture engineering change; delta trajectories capture engineering experience.**

---

# 19. Delta-Scoped Governance

TACG-SDIG also uses delta as a governance object.

Instead of beginning every review as a full-system rescan:

```text
Reviewed Baseline
      ↓
New Version
      ↓
Graph Minus
      ↓
Structural Change Frontier
```

Then review expands according to:

```text
Delta Core
Delta Halo
Changed Reachability
Task–Action Mapping
Policy
Security
Counter-Evidence
```

This is **Delta-Scoped Structural Governance**.

---

# 20. Governance Does Not Mean “Only Review the Delta”

Some changes have global effects.

Therefore review may expand:

```text
Delta Core
    ↓
Local Halo
    ↓
Extended Reachability
    ↓
System-Wide Review
```

The principle is:

> **Start from change, expand as structural consequences require.**

---

# 21. Task–Action Cross-Audit

The Mapping Plane supports two important questions.

From Task to Action:

> **Where was this requirement implemented?**

From Action to Task:

> **Why does this code exist?**

This creates:

```text
What We Intended
        ↕
What We Implemented
```

as a structural review mechanism.

---

# 22. The Three Main Engineering Values

TACG-SDIG has three main roles.

## I. Engineering Experience Evolution

```text
Historical Experience
      ↓
Delta Memory
      ↓
Delta CCC / DNA
      ↓
Delta Trajectory
```

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
```

---

## III. Structural Governance

```text
Baseline
      ↓
Delta
      ↓
Adaptive Review Scope
      ↓
Task–Action Cross-Audit
      ↓
Policy / Security
```

All three revolve around:

```text
Structural Delta
```

---

# 23. A Key Intelligence Principle

TACG-SDIG emphasizes:

> **Intelligence may come not only from generating better candidates, but from making fewer candidates necessary.**

The system reduces the search space through:

```text
Localization
Delta Isolation
CCC / DNA Dispatch
Task–Action Mapping
Historical Experience
Constraints
```

before open generation.

---

# 24. Human Engineering Practice

TACG-SDIG is motivated by a recurring senior-engineering workflow.

Human:

```text
Where is the relevant structure?
```

TACG-SDIG:

```text
Localization
```

Human:

```text
What is different?
```

TACG-SDIG:

```text
Graph Minus
```

Human:

```text
Have we solved this before?
```

TACG-SDIG:

```text
Delta Search
```

Human:

```text
Will that old fix work here?
```

TACG-SDIG:

```text
Reachability / Feasibility
```

Human:

```text
That solution failed last time.
```

TACG-SDIG:

```text
Counter-Evidence
```

Human:

```text
One piece is still missing.
```

TACG-SDIG:

```text
Residual Delta
```

Human:

```text
Let's add the smallest next step.
```

TACG-SDIG:

```text
Primitive Forward Walking
```

---

# 25. Minimal Running Example

Consider this requirement:

```text
Only the owner may update a resource.
```

## Current TaskCG

```text
Authenticate
→ Update Resource
```

## Required TaskCG

```text
Authenticate
→ Verify Ownership
→ Update Resource
```

Graph Minus:

```text
ΔT:
Verify Ownership
```

## Current ActionCG

```text
authenticate()
→ updateResource()
```

Historical Delta Search finds:

```text
authenticate()
→ checkOwner()
→ deleteResource()
```

Candidate reconstruction adapts:

```text
checkOwner()
```

to the update path.

Candidate:

```text
authenticate()
→ checkOwner()
→ updateResource()
```

Then validate:

```text
owner data available?
current user available?
all update paths guarded?
failure branch defined?
policy satisfied?
```

If valid:

```text
Apply Delta
→ New Structure
→ Fold Back
```

This small example contains most of the TACG-SDIG runtime.

---

# 26. Recommended Reading Order

For a first reading, follow this sequence.

## Step 1 — Understand the Big Idea

Read:

```text
TACG-SDIG-001
From CallingGraph Knowledge
to Structural Delta Intelligence
```

Focus on:

```text
Why Delta?
Why search before generation?
Why is Delta first-class?
```

---

## Step 2 — Learn the Knowledge Model

Read:

```text
TACG-SDIG-002
Four Structural Planes
and the Canonical Knowledge Model
```

Focus on:

```text
1A–1N
Task Plane
Action Plane
Mapping Plane
Delta Plane
```

---

## Step 3 — Learn Graph Minus

Read:

```text
TACG-SDIG-003
Graph Minus and
Task–Action Delta Isolation
```

Focus on:

```text
Graph Minus
Delta Core
Delta Halo
Delta Taxonomy
TADP
```

---

## Step 4 — Learn the Runtime

Read:

```text
TACG-SDIG-004
Two-Way Delta Localization,
Search, and Candidate Reconstruction
```

Focus on:

```text
Two-Way Search
Candidate Reconstruction
Counter-Evidence
Residual Delta
Primitive Walking
```

---

## Step 5 — Learn the Memory and Evolution Model

Read:

```text
TACG-SDIG-005
Delta Memory, Folding,
and Structural Evolution Trajectories
```

Focus on:

```text
Delta Memory
Delta CCC
Delta DNA
Delta Trajectory
Fold Back
```

---

## Step 6 — Learn Governance

Read:

```text
TACG-SDIG-006
Delta-Scoped Structural Governance
and Security
```

Focus on:

```text
Baseline
Delta Frontier
Changed Reachability
Task–Action Cross-Audit
Policy
Security
```

---

## Step 7 — Read the Complete Synthesis

Finish with:

```text
TACG-SDIG-007
From Human Engineering Practice
to AI Coding Growth
```

This article connects the whole framework back to practical engineering behavior.

---

# 27. Eight Figures

Use the figures in parallel with the articles.

```text
Fig-001
TACG-SDIG Grand Map
```

Use for the overall framework.

```text
Fig-002
Four Structural Planes
and 1A–1N Knowledge Model
```

Use while reading 002.

```text
Fig-003
Graph Minus
and Task–Action Delta Pair
```

Use while reading 003.

```text
Fig-004
Two-Way Delta Search
and Growth Runtime
```

Use while reading 004.

```text
Fig-005
Delta Memory
and Structural Evolution Trajectory
```

Use while reading 005.

```text
Fig-006
Delta-Scoped Governance
and Security
```

Use while reading 006.

```text
Fig-007
Human Engineering Experience
to Structural AI Coding
```

Use while reading 007.

---

# 28. If You Only Have Five Minutes

Remember this:

```text
Known Structure
      ↓
Localization
      ↓
Graph Minus
      ↓
Delta
      ↓
Search Similar Historical Delta
      ↓
Adapt Candidate
      ↓
Validate
      ↓
Grow
      ↓
Remember the Outcome
```

And these six statements:

> **Delta is a first-class structural knowledge object.**

> **Search before generation.**

> **Structures describe states; deltas describe change; trajectories describe evolution.**

> **TaskCG tells us what was intended; ActionCG tells us what was implemented.**

> **Similarity finds candidates; validation determines whether they belong.**

> **Code tells AI what the system is; Delta tells AI how the system grows.**

---

# 29. If You Are an AI Coding Researcher

Start with:

```text
001
→
003
→
004
→
007
```

The key topics are:

```text
search-space reduction
candidate reconstruction
structural growth
primitive walking
continual Fold Back
```

---

# 30. If You Are a Software Architect

Start with:

```text
002
→
003
→
005
→
007
```

Focus on:

```text
structural state
structural change
architecture trajectory
engineering evolution memory
```

---

# 31. If You Are a Security or Governance Researcher

Start with:

```text
003
→
006
→
005
```

Focus on:

```text
Delta Core / Halo
changed reachability
Task–Action cross-audit
risk trajectory
counter-evidence
```

---

# 32. If You Are Interested in Continual Learning

Start with:

```text
004
→
005
→
007
```

Focus on:

```text
validated delta
Fold Back
Delta CCC
Delta DNA
trajectory growth
local structural learning
```

---

# 33. What TACG-SDIG Is Not

TACG-SDIG is not intended as:

```text
a complete software verifier

a universal security system

a replacement for testing

a replacement for static analysis

a replacement for human engineering judgment

a claim that every software problem
can be solved through historical reuse
```

It is a structural intelligence framework for reducing, organizing, and learning from engineering change.

---

# 34. What TACG-SDIG Adds

TACG-SDIG adds several explicit engineering objects:

```text
Graph Minus

Structural Delta

Task–Action Delta Pair

Delta Core

Delta Halo

Delta Memory

Delta CCC

Delta DNA

Residual Delta

Companion Delta

Counter-Evidence

Delta Trajectory

Delta-Scoped Governance
```

These objects together form the framework's main contribution.

---

# 35. The Larger Fold–Unfold View

TACG-SDIG can be understood inside a broader structural learning loop:

```text
Historical Experience
      ↓
FOLD
      ↓
Structural Memory
      ↓
LOCALIZE
      ↓
Required Delta
      ↓
UNFOLD
      ↓
Candidate Growth
      ↓
VALIDATE
      ↓
New Experience
      ↓
FOLD BACK
```

The distinctive TACG-SDIG focus is:

> **Intelligence acting on the difference between what exists and what is needed.**

---

# 36. Final Mental Model

Think of TACG-SDIG through four questions:

### State

```text
What do we already have?
```

### Delta

```text
What is different?
```

### Search

```text
How did similar systems cross this gap?
```

### Growth

```text
Which validated change should move us forward?
```

Then repeat:

```text
State
→ Delta
→ Search
→ Growth
→ New State
```

and preserve the history.

That history becomes:

```text
Trajectory
```

and repeated experience becomes:

```text
Structural Intelligence
```

---

# 37. Start Here

Recommended first article:

**`docs/TACG-SDIG-001-From-CallingGraph-Knowledge-to-Structural-Delta-Intelligence.md`**

Then continue through `TACG-SDIG-002` to `TACG-SDIG-007`.

For visual orientation, begin with:

**`figures/Fig-001-TACG-SDIG-Grand-Map.png`**

---

## TACG-SDIG

**Task–Action CallingGraph Structural Delta Intelligence and Growth**

> **From known structure, to meaningful difference, to validated growth.**
