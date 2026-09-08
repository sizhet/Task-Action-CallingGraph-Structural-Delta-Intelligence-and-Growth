# TACG-SDIG-001 — From CallingGraph Knowledge to Structural Delta Intelligence

## Task–Action CallingGraph Structural Delta Intelligence and Growth

**TACG-SDIG**

---

## Abstract

CallingGraph representations provide a structural language for describing tasks, actions, code behavior, dependencies, and executable paths. However, representing what a system **is** is only the beginning.

Engineering intelligence must also understand:

> **What changed?**
> **What is missing?**
> **Has a similar change occurred before?**
> **How was that structural gap crossed?**
> **Is the candidate change feasible, reachable, safe, and policy-compatible?**
> **What successful change should be retained as reusable experience?**

This article introduces **Structural Delta Intelligence (SDI)** as a framework for reasoning over meaningful structural differences between known, observed, and desired system states.

Within **Task–Action CallingGraph Structural Delta Intelligence and Growth (TACG-SDIG)**, Task CallingGraphs, Action/Code CallingGraphs, their two-way mappings, and their structural deltas form four interacting structural planes.

The resulting runtime follows a central intelligence loop:

```text
Folded Structural Knowledge
        ↓
Localization
        ↓
Structural Neighborhood
        ↓
Graph Minus
        ↓
Task / Action Structural Delta
        ↓
Two-Way Delta Search
        ↓
Candidate Delta Reconstruction
        ↓
Reachability / Feasibility
        ↓
Counter-Evidence / Policy / Governance
        ↓
Primitive-Level Constrained Forward Walking
        ↓
Validated Structural Growth
        ↓
Fold Back
```

The central proposition is simple:

> **A delta should not be treated merely as the temporary output of a comparison.**
>
> **A validated structural delta can itself become a first-class unit of engineering knowledge.**

This shift turns historical software changes into searchable structural experience, supports more localized AI coding, enables delta-scoped structural governance, and creates a natural bridge from CallingGraph knowledge to structural evolution intelligence.

---

# 1. From Structural Knowledge to Structural Change

A CallingGraph can describe a system structure.

A Task CallingGraph can represent:

* goals,
* jobs,
* sub-tasks,
* dependencies,
* conditions,
* workflows,
* required transitions,
* and planning structure.

An Action/Code CallingGraph can represent:

* executable actions,
* functions,
* method calls,
* API calls,
* data transformations,
* control paths,
* dependencies,
* and implementation structure.

These representations answer an important question:

> **What structure exists?**

But engineering work is rarely limited to understanding a static structure.

Software evolves.

Requirements change.

Policies change.

Security expectations change.

APIs change.

Infrastructure changes.

Existing systems must continually move from one structural state to another.

The more operational question therefore becomes:

> **How does a known structure become the structure that is now required?**

That question introduces the central object of TACG-SDIG:

> **Structural Delta**

---

# 2. The Engineering Question Is Often a Delta Question

Consider a senior engineer receiving a new requirement for an existing system.

The engineer rarely reasons from an empty program space.

Instead, an experienced engineer often performs something closer to:

```text
What already exists?
        ↓
What does the new requirement require?
        ↓
What is different?
        ↓
Have I seen this kind of difference before?
        ↓
How was it solved?
        ↓
Will that solution work here?
        ↓
What else must change?
        ↓
Implement
        ↓
Validate
        ↓
Retain the experience
```

This is fundamentally different from:

```text
Requirement
    ↓
Generate arbitrary code candidates
    ↓
Test candidates
```

The experienced engineer uses prior structure to reduce the problem.

The system does not need to rediscover the whole program.

It needs to identify the **meaningful change frontier**.

This motivates a central TACG-SDIG principle:

> **Search before generation.**

And a broader intelligence principle:

> **Intelligence may come not only from generating better candidates, but from making fewer candidates necessary.**

---

# 3. Structural Delta Intelligence

We define:

> **Structural Delta Intelligence is the capability to identify, localize, retrieve, compare, compose, validate, and learn meaningful structural changes between known, observed, and desired system states.**

This definition contains several distinct capabilities.

## 3.1 Identify

Determine that two structures differ and identify where meaningful differences occur.

## 3.2 Localize

Find the structural neighborhood in which the new requirement, code fragment, task structure, or delta belongs.

## 3.3 Retrieve

Search historical structural knowledge for exact or nearby examples of the same or similar change.

## 3.4 Compare

Determine whether historical changes are structurally compatible with the current context.

## 3.5 Compose

Combine reusable structural deltas when no single historical delta completely satisfies the target.

## 3.6 Validate

Evaluate candidate deltas using:

* structural compatibility,
* reachability,
* feasibility,
* constraints,
* policy,
* counter-evidence,
* security expectations,
* and runtime evidence.

## 3.7 Learn

Fold successful changes back into reusable structural memory.

Thus, Structural Delta Intelligence is not merely a difference detector.

It is an intelligence system operating over **structural transformation knowledge**.

---

# 4. Four Structural Planes

TACG-SDIG begins with three established structural knowledge areas:

1. Task structure,
2. Action/code structure,
3. Task–Action mapping.

It then introduces Delta as a fourth first-class structural plane.

The canonical model is therefore:

```text
┌───────────────────────────────┐
│      TASK STRUCTURAL PLANE    │
│                               │
│ Task CG                       │
│ Known Task / Job CGs          │
│ One-Step Task Primitives      │
└───────────────┬───────────────┘
                │
                ↕
┌───────────────────────────────┐
│       MAPPING PLANE           │
│                               │
│ Task Elements                 │
│        ↕                      │
│ Action / Code Elements        │
└───────────────┬───────────────┘
                │
                ↕
┌───────────────────────────────┐
│     ACTION STRUCTURAL PLANE   │
│                               │
│ Action / Code CG              │
│ Known Action / Code CGs       │
│ Feasible Action Primitives    │
└───────────────┬───────────────┘
                │
                ↕
┌───────────────────────────────┐
│      DELTA STRUCTURAL PLANE   │
│                               │
│ Task Delta                    │
│ Action Delta                  │
│ Task–Action Delta Pair        │
│ Delta Memory                  │
│ Delta CCC / DNA               │
│ Delta Trajectory              │
│ Evidence / Outcome / Policy   │
└───────────────────────────────┘
```

The important change is conceptual:

> **Delta is promoted from an operation result to a persistent structural knowledge object.**

---

# 5. The Canonical TACG-SDIG Knowledge Structure

The initial Task–Action CallingGraph model contains seven foundational structures.

TACG-SDIG extends them with seven Delta Intelligence structures.

## 5.1 Task Structural Plane

### 1A — Task CG

The Task CallingGraph describing a target task, requirement, workflow, or planning structure.

### 1B — Collection of Known Task / Job CGs

Previously folded task structures representing historical task and engineering experience.

### 1C — Common-Sense One-Step Task / Job CGs

Small task transitions or task primitives separated from larger TaskCGs to improve delta isolation and local structural extension.

---

## 5.2 Action Structural Plane

### 1D — Action / Code CG

The CallingGraph representation of executable actions, software behavior, or code structure.

### 1E — Collection of Known Action / Code CGs

Previously observed, validated, or folded implementation structures.

### 1F — Common-Sense Feasible Action / Code Statements / CGs

Small feasible action primitives that can support local structural reconstruction and constrained forward walking.

Examples include:

```text
validate input
authenticate identity
authorize operation
load resource
transform data
call service
retry operation
rollback transaction
persist state
emit audit event
return result
```

---

## 5.3 Task–Action Mapping Plane

### 1G — Two-Way Task–Action Mapping Graph

A many-to-many structural mapping between TaskCG and ActionCG elements.

The mapping may exist at multiple granularities:

```text
Task Node       ↔ Action Node
Task Edge       ↔ Action Edge
Task Subgraph   ↔ Action Subgraph
Task Path       ↔ Action Path
Task CCC        ↔ Action CCC
Task DNA        ↔ Action DNA
```

This mapping supports both generation and explanation.

It can answer:

> What implementation realizes this task?

and:

> What task or requirement explains this implementation?

---

# 6. The Delta Structural Plane

The fourth plane adds explicit structural transformation knowledge.

## 6.1 1H — Task Structural Delta

A meaningful structural difference on the TaskCG side.

Denote it:

```text
ΔT
```

---

## 6.2 1I — Action Structural Delta

A meaningful structural difference on the Action/Code CG side.

Denote it:

```text
ΔA
```

---

## 6.3 1J — Task–Action Delta Pair

A task-side structural change and its corresponding action-side structural change can form a reusable pair.

We call this a:

> **Task–Action Delta Pair (TADP)**

Conceptually:

```text
TADP =
<
    ΔTask,
    ΔAction,
    Mapping,
    Context,
    Constraints,
    Evidence,
    Outcome
>
```

A TADP represents not merely what changed, but how a task-side requirement change was realized through an action-side implementation change.

---

## 6.4 1K — Collection of Known Structural Deltas

Historical deltas should be retained as searchable structural memory.

Examples may include:

```text
Add Authentication
Add Authorization
Add Retry
Add Transaction Boundary
Add Cache
Add Audit Logging
Add Validation
Add Recovery Path
Split Service
Replace Synchronous Call with Asynchronous Flow
Migrate API Version
Introduce External Data Transfer
```

This creates a new retrieval space:

> **Delta Memory**

---

## 6.5 1L — Delta CCC / Delta DNA

Repeated structural changes can themselves be folded.

Historical delta instances may form:

```text
Delta Instances
      ↓
Delta Clusters
      ↓
Delta CCC
      ↓
Delta DNA
```

This allows recurring engineering transformations to become compressed, searchable structural knowledge.

---

## 6.6 1M — Delta Trajectory

A sequence of structural changes forms an evolution trajectory:

```text
S0
 --Δ1-->
S1
 --Δ2-->
S2
 --Δ3-->
S3
```

The corresponding trajectory can be represented as:

```text
T = <Δ1, Δ2, Δ3, ..., Δn>
```

This produces an important general relationship:

> **Structures describe states.**
> **Deltas describe change.**
> **Trajectories describe evolution.**

---

## 6.7 1N — Delta Evidence, Outcome, and Governance

A useful Delta Knowledge Unit should preserve more than the structural change itself.

It may include:

```text
Delta Knowledge Unit
{
    beforeStructure,
    delta,
    afterStructure,

    taskContext,
    actionContext,

    mapping,
    constraints,

    supportingEvidence,
    counterEvidence,

    feasibility,
    reachability,

    policyStatus,
    risk,

    validationEvidence,
    runtimeOutcome
}
```

This allows Delta Memory to evolve from a history of changes into a history of **evaluated engineering transformations**.

---

# 7. Localization Before Delta Analysis

Suppose a new TaskCG is presented.

A naive system might immediately attempt to synthesize a complete implementation.

TACG-SDIG first asks:

> **Where is this structure located relative to what we already know?**

The runtime therefore begins with localization:

```text
New TaskCG
    ↓
Structural Representation
    ↓
Exact Structural Match
    ↓
Closest Structural Match
    ↓
CCC Localization
    ↓
DNA / Structural Search
    ↓
Closest Known Task Neighborhood
```

Through the Task–Action Mapping Plane, the system can also retrieve corresponding known ActionCG structures.

Similarly, given a piece of code or an ActionCG:

```text
ActionCG
    ↓
Action Structural Localization
    ↓
Known Action Neighborhood
    ↓
Task–Action Mapping
    ↓
Task-Side Explanation
```

This provides a structural route from:

> **Code → Prior Structural Experience → Task Explanation**

Localization establishes the neighborhood in which Delta Intelligence should operate.

---

# 8. Graph Minus

Once the closest relevant structure has been localized, TACG-SDIG isolates the structural difference.

Let:

```text
R = Required / Target Structure
K = Closest Known Structure
```

Then conceptually:

```text
Δ = R ⊖ K
```

where `⊖` denotes **Graph Minus**.

Graph Minus is not ordinary node-set subtraction.

A meaningful structural difference may include:

```text
Missing Node
Missing Edge
Missing Subgraph
Missing Path

Extra Node
Extra Edge
Extra Subgraph

Changed Ordering
Changed Dependency
Changed Condition
Changed Constraint
Changed Role
Changed State Transition

Conflicting Structure
Unsafe Structure
Unmapped Structure
Unreachable Structure
Redundant Structure
```

Therefore Graph Minus attempts to answer:

> **What meaningful structural transformation separates the known structure from the desired or observed structure?**

For TaskCG:

```text
Target TaskCG
      ⊖
Known TaskCG
      ↓
     ΔT
```

For ActionCG:

```text
Target ActionCG
      ⊖
Known ActionCG
      ↓
     ΔA
```

These may then be connected through a Task–Action Delta Pair.

---

# 9. Delta Search

Once a delta has been isolated, the next step should not automatically be free generation.

Instead:

```text
Δ
↓
Has this structural change occurred before?
```

The system searches Delta Memory:

```text
Structural Delta
      ↓
Exact Delta Match
      ↓
Nearest Delta Match
      ↓
Delta Cluster
      ↓
Delta CCC
      ↓
Delta DNA
      ↓
Historical Delta Episodes
```

This is **Structural Delta Retrieval**.

The key distinction is:

Traditional structural search asks:

> Where have we seen a structure like this?

Delta search asks:

> Where have we seen a change like this?

That difference is central to TACG-SDIG.

---

# 10. Two-Way Delta Search

Task-side and Action-side deltas should not be isolated intelligence spaces.

Given:

```text
ΔT
```

the system can search:

```text
ΔT
├── Task Delta Memory
├── Task CCC / DNA
├── Task → Action Mapping
└── Related Action Deltas
```

Given:

```text
ΔA
```

the system can search:

```text
ΔA
├── Action Delta Memory
├── Action CCC / DNA
├── Action → Task Mapping
└── Related Task Deltas
```

Together:

```text
             ΔT
          ↙      ↘
   Task Search   Action Search
          ↘      ↙
             ΔA
```

This creates a two-way structural intelligence process.

A task requirement can retrieve implementation experience.

An implementation change can retrieve task-side intent and precedent.

The two sides can also cross-check each other.

---

# 11. Candidate Delta Reconstruction

Historical Delta Memory may produce several candidate transformations:

```text
C1 = <ΔT1, ΔA1>
C2 = <ΔT2, ΔA2>
C3 = <ΔT3, ΔA3>
...
```

Similarity alone should not decide which candidate is used.

Candidate evaluation may include:

```text
Structural Similarity
Task Compatibility
Action Compatibility
Reachability
Feasibility
Dependency Satisfaction
Constraint Satisfaction
Policy Compatibility
Security Risk
Historical Outcome
Counter-Evidence
Runtime Cost
```

This establishes an important distinction:

> **Similarity finds candidates.**
>
> **Structural and operational validation determines whether a candidate can live inside the target system.**

---

# 12. Counter-Evidence

Historical precedent is useful, but precedent should not be treated as automatic approval.

For every candidate delta, TACG-SDIG can ask two questions:

```text
Where has this delta worked?
```

and:

```text
Where has this delta failed, conflicted, or been rejected?
```

Thus:

```text
Candidate Delta
      ↓
Supporting Structural Evidence
      +
Counter-Delta Evidence
      ↓
Contextual Evaluation
```

For example:

```text
Candidate:
Add cache at this structural location.
```

Positive evidence may show similar successful designs.

Counter-evidence may show:

```text
staleness failures
consistency violations
security leakage
invalid lifecycle assumptions
transaction conflicts
```

This makes historical structural memory useful not only for imitation, but also for restraint.

---

# 13. Primitive-Level Constrained Forward Walking

Historical search may still fail to produce a complete solution.

At this point, TACG-SDIG can use:

```text
1C — One-Step Task Primitives
1F — Feasible Action Primitives
```

to perform constrained structural extension.

Instead of unconstrained generation:

```text
Current Structure
       ↓
Feasible One-Step Delta
       ↓
Extended Structure
       ↓
Feasible One-Step Delta
       ↓
Extended Structure
       ↓
Target Neighborhood
```

This is:

> **Primitive-Level Constrained Forward Walking**

The distinction is important.

The system is not asked to invent an arbitrary program.

It is asked to traverse a locally feasible structural transformation space.

This creates a continuum:

```text
Exact Known Solution
        ↓
Closest Known Solution
        ↓
Known Delta
        ↓
Composite Historical Delta
        ↓
Primitive Repair
        ↓
Constrained Forward Walking
        ↓
Candidate New Structure
```

Generation becomes progressively more open only when reusable structural experience is insufficient.

---

# 14. Growth

A candidate delta that passes structural validation can be applied to the current structure.

Conceptually:

```text
Known Structure
      +
Validated Delta
      ↓
Grown Structure
```

Growth may include:

* adding structure,
* removing structure,
* replacing structure,
* reconnecting paths,
* changing conditions,
* modifying dependencies,
* adding policy guards,
* introducing recovery paths,
* or reorganizing a larger CallingGraph.

Growth is therefore not synonymous with adding nodes.

It means:

> **A validated structural transition from one system state to another.**

---

# 15. Fold Back

The intelligence loop is incomplete if successful changes disappear after execution.

A validated transformation should become new experience:

```text
Before Structure
       +
Validated Delta
       ↓
After Structure
       ↓
Observed Outcome
       ↓
Fold Back
```

The system can update:

```text
Structure Memory
Mapping Memory
Delta Memory
Trajectory Memory
```

This creates a continual structural learning loop:

```text
Fold
 ↓
Localize
 ↓
Delta
 ↓
Search
 ↓
Unfold
 ↓
Validate
 ↓
Grow
 ↓
Observe
 ↓
Fold
 ↺
```

The purpose is not merely to accumulate more code.

The purpose is to accumulate increasingly reusable **structural engineering experience**.

---

# 16. Engineering Value I — Human Coding Experience as Evolvable Structural Knowledge

Experienced engineers possess knowledge that is difficult to represent as isolated code snippets.

Much of that knowledge concerns transformations:

```text
When this requirement appears,
this part of the system usually changes.

When this dependency changes,
these other paths must also change.

When this security boundary appears,
these guards become necessary.

When this API changes,
these callers and mappings must migrate.
```

This suggests that an important unit of engineering experience is:

```text
Before Structure
       ↓
Engineering Delta
       ↓
After Structure
```

rather than merely:

```text
Code Example
```

A history of validated deltas can therefore become an **Engineering Evolution Memory**.

This supports a stronger statement:

> **Code tells us what a system is.**
>
> **Delta tells us how a system changes.**
>
> **Delta trajectory tells us how engineering experience evolves.**

---

# 17. Engineering Value II — Smarter AI Coding Through Search-Space Reduction

A large AI coding problem can expose an enormous candidate space.

A generation-first approach resembles:

```text
Requirement
     ↓
Large Program Space
     ↓
Generate Candidates
     ↓
Rank
     ↓
Test
```

TACG-SDIG attempts to reduce that space before generation:

```text
Requirement
     ↓
Structural Localization
     ↓
Known Neighborhood
     ↓
Graph Minus
     ↓
Local Delta Space
     ↓
Delta Search
     ↓
Small Candidate Set
     ↓
Validation
```

The conceptual transition is:

```text
Whole Program Space
        ↓
Local Structural Delta Space
```

This is one of the central motivations for Structural Delta Intelligence.

The goal is not to eliminate generation.

The goal is to use structural knowledge so that generation is invoked only where structural memory and constrained search are insufficient.

---

# 18. Engineering Value III — Delta-Scoped Structural Governance

Structural Delta Intelligence also creates a useful governance plane.

Suppose a software baseline has already been reviewed.

A new release changes only part of the system.

Instead of treating every release as a completely new system:

```text
Reviewed Baseline
       +
New Structural Delta
       ↓
Delta-Scoped Review
```

The governance system can focus on the structural change frontier.

Potential checks include:

```text
Changed Task Paths
Changed Action Paths
Changed Task–Action Mappings

New Reachability
Removed Guards
New Privilege Transitions
New External Calls
New Data Flows

Unmapped Actions
Unimplemented Tasks
Policy Violations
Known Risk Structures
```

This can make structural governance more scalable and more focused.

It does not replace:

* testing,
* formal verification,
* security analysis,
* runtime monitoring,
* human review,
* or domain-specific compliance systems.

Rather, it provides an additional systematic inspection layer.

---

# 19. Cross-Plane Consistency

The Task–Action Mapping Plane enables a particularly useful governance question:

> **Does what we implemented still correspond to what we intended?**

For example:

```text
Task Requirement:

User may read only resources
owned by that user.
```

Suppose the ActionCG contains:

```text
authenticate
     ↓
loadResource(id)
     ↓
returnResource
```

The TaskCG implies an ownership constraint.

The ActionCG lacks the corresponding ownership verification.

The system can identify a cross-plane delta:

```text
Task requires:
ownership verification

Action implementation:
missing

        ↓

Task–Action Consistency Delta
```

The reverse case is also important.

Suppose an ActionCG contains a significant new branch that maps to no task, requirement, policy, or infrastructure reason.

The system can ask:

> **Why does this code exist?**

Such an **Unmapped Action Delta** can become a focused review target.

---

# 20. Security as Structural Delta Analysis

Security analysis is a natural extension of this framework.

A known safe structural pattern might require:

```text
External Input
      ↓
Validation
      ↓
Authentication
      ↓
Authorization
      ↓
Privileged Operation
      ↓
Audit
```

An observed system may contain:

```text
External Input
      ↓
Authentication
      ↓
Privileged Operation
```

Then:

```text
Expected Safe CG
       ⊖
Observed CG
       ↓
Security Delta
```

The missing structure may include:

```text
Validation
Authorization
Audit
```

A complementary search direction is:

```text
Known Risk CG
      ↓
Structural Localization
      ↓
Target TaskCG / ActionCG
```

Thus security analysis can include at least:

1. **Missing-Safety-Structure Detection**
2. **Known-Risky-Structure Localization**

Both are structural localization and delta problems.

---

# 21. Delta as a Governance Dispatch Unit

Not every change deserves the same review effort.

A delta can therefore become a natural unit for governance dispatch.

For example:

```text
Variable Rename
      ↓
Low Structural Impact

Add Logging
      ↓
Small Operational Delta

Change Authorization Path
      ↓
High-Risk Structural Delta

Introduce External Data Transfer
      ↓
Critical Governance Delta
```

This suggests:

```text
Structural Delta
      ↓
Delta Classification
      ↓
Risk / Policy Dispatch
      ↓
Appropriate Validation Depth
```

Rather than applying identical analysis to every change, governance resources can be concentrated where structural deltas indicate higher impact.

---

# 22. Delta History Is a Trajectory

Delta Memory naturally introduces time.

Suppose:

```text
S0 --Δ1→ S1 --Δ2→ S2 --Δ3→ S3 --Δ4→ S4
```

Then the system possesses not merely five structures.

It possesses a history of structural evolution.

The ordered delta sequence:

```text
<Δ1, Δ2, Δ3, Δ4>
```

is a trajectory.

This enables questions such as:

```text
Which delta usually follows this delta?

Which transformation paths repeatedly succeed?

Which trajectories lead to rollback?

Which structural changes tend to introduce risk?

Which sequence of deltas moves systems
from weak governance to strong governance?

Which engineering trajectories produce
stable long-term architectures?
```

Thus:

> **A trajectory is an ordered history of observed or validated structural deltas over an evolving structure.**

This connects structural change analysis with trajectory intelligence.

---

# 23. Delta Folding

If deltas are first-class objects, they can themselves be folded.

For example, many historical systems may contain variations of:

```text
Unauthenticated Endpoint
        ↓
Add Authentication
        ↓
Authenticated Endpoint
```

Repeated instances can form a Delta Cluster.

The cluster can become a reusable Delta CCC.

A compact identity can support Delta DNA dispatch.

Likewise:

```text
Authenticated Endpoint
        ↓
Add Authorization
        ↓
Authorized Endpoint
```

and:

```text
Authorized Endpoint
        ↓
Add Audit
        ↓
Audited Endpoint
```

may eventually reveal a recurring structural evolution trajectory:

```text
Open
 ↓
Authenticated
 ↓
Authorized
 ↓
Audited
```

The system has learned something more general than individual code changes.

It has learned:

> **How systems tend to become structurally stronger.**

---

# 24. Structural Transformation Knowledge

This leads to a broader view of structural memory.

A mature TACG-SDIG system may maintain four interacting memory classes:

```text
Structure Memory
    What systems are.

Mapping Memory
    How Task and Action structures correspond.

Delta Memory
    How systems change.

Trajectory Memory
    How sequences of changes evolve.
```

Together they form:

> **Structural Transformation Knowledge**

This knowledge can support:

* retrieval,
* explanation,
* planning,
* coding,
* repair,
* migration,
* governance,
* security analysis,
* structural learning,
* and engineering decision support.

---

# 25. Human Practice as the MET Starting Point

TACG-SDIG does not require the assumption that AI must discover an entirely new form of engineering reasoning.

A practical starting point is to observe how experienced humans work.

Human engineering practice often resembles:

```text
Inspect existing structure
        ↓
Understand new requirement
        ↓
Find relevant prior experience
        ↓
Identify the difference
        ↓
Estimate consequences
        ↓
Search known solutions
        ↓
Adapt solution to local constraints
        ↓
Implement
        ↓
Test
        ↓
Learn from outcome
```

TACG-SDIG translates this practice into structural operations:

```text
Inspect
    ↓
Localization

Difference
    ↓
Graph Minus

Prior Experience
    ↓
Delta Search

Adaptation
    ↓
Candidate Delta Reconstruction

Engineering Judgment
    ↓
Reachability / Feasibility /
Counter-Evidence / Policy

Incremental Repair
    ↓
Primitive Forward Walking

Implementation
    ↓
Structural Growth

Experience
    ↓
Fold Back
```

This provides a Model Engineering and Training-oriented path from human engineering behavior to AI structural intelligence.

---

# 26. Similar Structural Practices

The same general pattern appears outside software engineering.

## 26.1 Chess and Go

A game state can be treated as a structured state.

A move changes that state.

From this perspective:

> **A move is a minimal feasible structural delta.**

A sequence of moves forms a trajectory.

Candidate moves can be searched, evaluated, and selected under constraints.

---

## 26.2 Blueprints and Buildings

An existing blueprint can be compared with a new requirement.

The important question is often not:

> How do we design a building from nothing?

but:

> What structural modifications transform the known design into the required design?

---

## 26.3 Tailoring

A known clothing pattern can be localized against a new customer's requirements.

Then:

```text
Known Pattern
      +
Customer Requirement
      ↓
Difference
      ↓
Alteration Delta
      ↓
Feasibility Check
      ↓
New Pattern
```

---

## 26.4 War Games and Planning Systems

A current operational structure can be changed through candidate actions.

Each candidate action produces a structural delta.

Sequences of deltas form possible future trajectories.

The general pattern is again:

```text
Known State
      ↓
Candidate Delta
      ↓
Resulting State
      ↓
Evaluation
      ↓
Next Delta
```

These analogies suggest that Structural Delta Intelligence may eventually extend beyond AI coding.

TACG-SDIG, however, deliberately begins with Task–Action CallingGraphs because they provide a concrete engineering environment in which the framework can be tested.

---

# 27. The TACG-SDIG Intelligence Loop

The entire framework can now be summarized as:

```text
             FOLDED EXPERIENCE
                    │
                    ↓
              LOCALIZATION
                    │
                    ↓
        STRUCTURAL NEIGHBORHOOD
                    │
                    ↓
               GRAPH MINUS
                    │
                    ↓
              ΔTask ↔ ΔAction
                    │
                    ↓
          TWO-WAY DELTA SEARCH
                    │
                    ↓
          CANDIDATE DELTA PAIRS
                    │
                    ↓
        SUPPORT + COUNTER-EVIDENCE
                    │
                    ↓
     REACHABILITY / FEASIBILITY / POLICY
                    │
                    ↓
     PRIMITIVE CONSTRAINED FORWARD WALK
                    │
                    ↓
            VALIDATED STRUCTURE
                    │
                    ↓
                  GROWTH
                    │
                    ↓
             RUNTIME OUTCOME
                    │
                    ↓
                FOLD BACK
                    │
                    └───────────────┐
                                    │
                             NEW EXPERIENCE
```

This loop expresses the central TACG-SDIG thesis.

---

# 28. Seven Core Principles

TACG-SDIG can be summarized through seven principles.

## Principle 1 — Delta Is First-Class Knowledge

> **A delta is not merely the result of comparison; it is a reusable unit of structural knowledge.**

## Principle 2 — Search Before Generation

Use folded structural experience before expanding into open generation.

## Principle 3 — Localize Before Searching Broadly

Find the structural neighborhood before exploring the solution space.

## Principle 4 — Reduce the Search Space

> **Intelligence may come not only from generating better candidates, but from making fewer candidates necessary.**

## Principle 5 — Validate Across Both Task and Action

A candidate implementation should be checked against both executable feasibility and task-side intent.

## Principle 6 — Learn Change, Not Only State

> **Structures describe states. Deltas describe change. Trajectories describe evolution.**

## Principle 7 — Successful Growth Becomes New Experience

A validated structural transition should be folded back into reusable memory.

---

# 29. Three Engineering Values

The framework is motivated by three major engineering values.

## 29.1 Engineering Experience Evolution

Transform historical coding experience from isolated artifacts into reusable structural transformation knowledge.

```text
Code History
     ↓
Structural History
     ↓
Delta History
     ↓
Trajectory History
     ↓
Engineering Evolution Memory
```

## 29.2 Smarter AI Coding

Reduce dependence on broad enumeration and unconstrained generation through:

```text
Localization
→ Graph Minus
→ Delta Search
→ Candidate Reconstruction
→ Validation
```

## 29.3 Structural Governance

Provide a systematic structural inspection plane focused on:

```text
Task–Action Consistency
Delta Risk
Reachability
Feasibility
Policy
Security
Counter-Evidence
Structural Change Frontier
```

This is not a complete software assurance solution.

It is a scalable structural intelligence layer that can complement existing engineering validation mechanisms.

---

# 30. Canonical Statements

Several statements capture the core of TACG-SDIG.

> **Fold stores experience.**

> **Localization finds where we are.**

> **Delta identifies what is missing or changed.**

> **Two-way search finds how others crossed that structural gap.**

> **Unfolding reconstructs a candidate path.**

> **Validation decides whether the path is viable in the target system.**

> **Growth applies the validated transformation.**

> **Fold-back turns successful change into new structural experience.**

And at the level of structural evolution:

> **Structures describe states.**

> **Deltas describe change.**

> **Trajectories describe evolution.**

For engineering intelligence:

> **Code captures implementation states; structural deltas capture engineering change; delta trajectories capture engineering experience.**

---

# 31. From CallingGraph Knowledge to Structural Delta Intelligence

CallingGraph knowledge provides the structural substrate.

Structural Folding provides reusable experience.

Localization provides context.

Graph Minus isolates meaningful change.

Delta Memory provides transformation precedent.

Task–Action mapping connects intent with implementation.

Counter-evidence provides restraint.

Reachability and feasibility provide engineering grounding.

Primitive forward walking provides controlled extension.

Validation provides evidence.

Growth changes the system.

Fold-back preserves the result.

Together:

```text
CallingGraph Knowledge
        ↓
Folded Structural Experience
        ↓
Localization
        ↓
Graph Minus
        ↓
Structural Delta
        ↓
Delta Intelligence
        ↓
Validated Growth
        ↓
Structural Evolution
```

This is the transition from static structural knowledge to active structural intelligence.

---

# 32. Conclusion

TACG-SDIG begins from a practical observation:

> Mature engineering rarely starts from nothing.

Existing systems, prior designs, historical implementations, known failures, successful repairs, policies, and accumulated human experience already contain structural knowledge.

The challenge is to make that experience operational.

Structural Delta Intelligence proposes one route.

Instead of asking AI only:

> **What code should be generated?**

TACG-SDIG first asks:

> **Where are we structurally?**

Then:

> **What is different between what exists and what is required?**

Then:

> **Has this structural difference been crossed before?**

Then:

> **Which historical delta is valid under the present TaskCG, ActionCG, constraints, policy, and runtime environment?**

And finally:

> **What successful new structural transformation should become part of future engineering memory?**

The resulting loop is:

```text
Fold
→ Localize
→ Isolate Delta
→ Search Delta
→ Reconstruct
→ Validate
→ Grow
→ Observe
→ Fold Again
```

This transforms CallingGraph knowledge from a description of software structure into a foundation for **Structural Delta Intelligence and Growth**.

The long-term objective is not merely an AI that can produce more code.

It is an AI that can increasingly understand:

> **what exists,**
>
> **what changed,**
>
> **what is missing,**
>
> **how similar systems evolved,**
>
> **which changes are structurally appropriate,**
>
> **and what successful engineering change should be remembered.**

That is the central research direction of **Task–Action CallingGraph Structural Delta Intelligence and Growth (TACG-SDIG)**.

---

## Next Article

**TACG-SDIG-002 — Four Structural Planes and the Canonical TACG-SDIG Knowledge Model**

The next article formalizes the Task, Action, Mapping, and Delta Structural Planes and develops the canonical **1A–1N knowledge structure** used by the TACG-SDIG framework.
