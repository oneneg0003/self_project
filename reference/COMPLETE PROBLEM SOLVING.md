# COMPLETE PROBLEM SOLVING PHASE ARCHITECTURE
(State-Flow Graph Version)

==================================================

## 0️⃣ TRIGGER
Dominant Function: Awareness

Purpose:
Recognize that a problem or opportunity exists.

- Detect gap, anomaly, inefficiency, confusion, or goal
- Identify why it matters
- Decide whether it deserves structured solving

Inputs:
- Reflection results
- Deployment outcomes
- Reinforcement updates
- New task initiation

Input From:
- DEPLOYMENT
- REFLECTION
- REINFORCEMENT
- (Start State)

Outputs:
→ Problem signal

Output To:
- FRAMING
- (Terminate / Ignore)

==================================================

## 1️⃣ FRAMING(Problem Definition Layer)
Dominant Function: Clarification

Purpose:
Define exactly what is being solved.

- Precise restatement
- Define success criteria
- Identify inputs, outputs, objectives
- Define scope and boundaries
- Identify stakeholders
- Classify problem type

Inputs:
- Problem signal

Input From:
- TRIGGER
- VALIDATION (if structural failure detected)
- DECISION (if revision required)

Outputs:
→ Well-defined problem statement
→ Success criteria
→ Scope boundaries

Output To:
- INFORMATION & MODELING
- SEARCH SPACE DEFINITION

==================================================

## 2️⃣ INFORMATION & MODELING
Dominant Function: Structural Understanding

Purpose:
Build structured representation of the problem

A. Information Gathering
    - Collect givens
    - Separate knowns / unknowns / unknowables
    - Ask clarifying questions
    - Acquire missing data

B. Representation Engineering
    - Choose model form 
        -algebraic
        -geometric
        -graph
        -probabilistic
        -algorithmic
        -simulation
C. Structural Mapping
    - Variables (what can change)
    - Constraints (limits)
    - Relationships (interactions)
    - Goals (what must be achieved)
    - Invariants / symmetries
    - Degrees of freedom
D. Causal Analysis
    - Identify root causes
    - Distinguish symptom vs cause
    - Map cause–effect chains
    - Identify feedback loops
    - Analyze how root causes interact

Inputs:
- Problem definition
- Scope boundaries

Input From:
- FRAMING
- GENERATION (if new data required)
- VALIDATION (if inconsistency found)

Outputs:
→ Structured model
→ Variable map
→ Known/unknown list
→ Causal map

Output To:
- SEARCH SPACE DEFINITION
- GENERATION
- EVALUATION (if model already sufficient)

==================================================

## 3️⃣ SEARCH SPACE DEFINITION
Dominant Function: Boundary Control

Purpose:
Define solution space.

- Explicit constraints
    - Logical
    - Physical
    - Computational
    - Resource
    - Ethical
    - Adversarial
- Assumptions
    - Explicit vs implicit
    - Domain vs temporary
    - Reversible vs irreversible
- Define allowed vs forbidden regions
- Identify edge and extreme cases
- Detect underdetermined vs overdetermined regimes


Inputs:
- Structured model
- Success criteria

Input From:
- INFORMATION & MODELING
- FRAMING

Outputs:
→ Bounded solution space
→ Validity rules

Output To:
- GENERATION
- EVALUATION

==================================================

## 4️⃣ GENERATION
Dominant Function: Divergent Exploration

Purpose:
Create candidate solutions.

- Generate multiple approaches
- Use analogy and transfer
- Extremal and limiting reasoning
- Controlled randomness
- Combine and cluster ideas
- Form competing hypotheses / candidates

Inputs:
- Structured model
- Constraints
- Boundaries

Input From:
- INFORMATION & MODELING
- SEARCH SPACE DEFINITION
- CONSTRUCTION (if build failure)
- EVALUATION (if all candidates rejected)

Outputs:
→ Candidate solution set

Output To:
- EVALUATION
- INFORMATION & MODELING (if gap detected)

==================================================

## 5️⃣ EVALUATION
Dominant Function: Convergent Selection

Purpose:
Select the strongest candidate.

- Compare candidates using criteria:
    - Constraint satisfaction
    - Explanatory power
    - Simplicity
    - Generality
    - Risk vs benefit
    - Test cost vs information gain
- Eliminate weak candidates
- Select primary candidate (optionally backup)


Inputs:
- Candidate set
- Constraints
- Success criteria

Input From:
- GENERATION
- SEARCH SPACE DEFINITION
- INFORMATION & MODELING

Outputs:
→ Ranked options
→ Selected candidate

Output To:
- CONSTRUCTION
- GENERATION (if none viable)
- INFORMATION & MODELING (if missing data)

==================================================

## 6️⃣ CONSTRUCTION
Dominant Function: Implementation

Purpose:
Build the selected solution.

- Formal derivation / proof
- Algorithm implementation
- Prototype building
- Simulation execution
- Step-by-step development


Inputs:
- Selected candidate

Input From:
- EVALUATION

Outputs:
→ Concrete artifact
→ Executable solution

Output To:
- VALIDATION
- GENERATION (if structural failure)

==================================================

## 7️⃣ VALIDATION
Dominant Function: Critical Testing

Purpose:
Ensure correctness and robustness.

- Internal logical consistency
- Edge and boundary case testing
- Stress and adversarial tests
- Sensitivity analysis
- Compare predicted vs actual behavior
- Redundancy checks


Inputs:
- Constructed artifact
- Success criteria

Input From:
- CONSTRUCTION
- EVALUATION (theoretical validation case)

Outputs:
→ Verified solution
OR
→ Failure report

Output To:
- DECISION
- GENERATION (if candidate invalid)
- INFORMATION & MODELING (if structural flaw)
- FRAMING (if problem misdefined)

==================================================

## 8️⃣ DECISION
Dominant Function: Commitment

Purpose:
Commit or revise.

- Accept / Reject / Revise
- Choose trade-offs explicitly
- Assess confidence level
- Document limitations
Inputs:
- Validation result

Input From:
- VALIDATION

Outputs:
→ Committed solution
OR
→ Revision directive

Output To:
- DEPLOYMENT (if accepted)
- GENERATION
- INFORMATION & MODELING
- FRAMING

==================================================

## 9️⃣ DEPLOYMENT
Dominant Function: Application

Purpose:
Apply in real context.

- Implement in environment
- Communicate assumptions and limits
- Monitor early performance


Inputs:
- Committed solution

Input From:
- DECISION

Outputs:
→ Real-world performance results
→ Operational feedback

Output To:
- REFLECTION
- TRIGGER (if new problem emerges)

==================================================

## 🔟 REFLECTION
Dominant Function: Meta-Cognition

Purpose:
Extract learning from outcome.

- What worked?
- What failed?
- Where were assumptions wrong?
- Where was time wasted?
- Which signals were ignored?


Inputs:
- Deployment outcomes
- Validation results

Input From:
- DEPLOYMENT
- VALIDATION

Outputs:
→ Lessons learned
→ Model updates

Output To:
- GENERALIZATION
- TRIGGER (if systemic issue found)

==================================================

## 1️⃣1️⃣ GENERALIZATION
Dominant Function: Abstraction

Purpose:
Extract reusable structure.

- Identify structural pattern
- Extract reusable template
- Identify triggering cues
- Compress into schema or checklist

Inputs:
- Lessons learned

Input From:
- REFLECTION

Outputs:
→ Schema / reusable structure

Output To:
- REINFORCEMENT
- TRIGGER (future use)

==================================================

## 1️⃣2️⃣ REINFORCEMENT
Dominant Function: Capability Upgrade
step_10(introspection+retrospection)
[Reinforcement](https://github.com/negzero/skills/blob/main/cp_road_map2.md)
Purpose:
Improve internal toolkit.

- Improve tools
- Improve evaluation criteria
- Improve search heuristics
- Expand model library
- Reduce future cognitive load
based on feeback from step_10
Inputs:
- Schema
- Reflection results

Input From:
- GENERALIZATION
- REFLECTION

Outputs:
→ Upgraded internal system

Output To:
- TRIGGER (next problem cycle)

==================================================================

MACRO FLOW:

Trigger
→ Framing
→ Information & Modeling
→ Search Space Definition
→ Generation
→ Evaluation
→ Construction
→ Validation
→ Decision
→ Deployment
→ Reflection
→ Generalization
→ Reinforcement
→ (Next Problem)

==================================================================

For EACH Phase in PS_Phases:

# CANONICAL ACTION ARCHITECTURE (PS-Integrated Version)

User (Actor)
  ↓
Identity / Role (who am I in this action?)
  ↓
Context (environment / situation / domain)
  ↓
Stakeholders / Audience (who is affected? who evaluates success?)
  ↓
Purpose (why act? meaning / value)
  ↓
Job / Goal (what outcome must be achieved?)
  ↓
Success Definition (acceptance criteria / "done" condition)
  ↓
Priority (importance relative to other goals)
  ↓
Time Horizon (short-term / long-term orientation)
  ↓
Constraints (rules, limits, time, policies)
  ↓
Resources (time, attention, knowledge, energy, data available)
  ↓
Dependencies (information required, approvals, prior results, prerequisite knowledge)
  ↓
Preconditions (what must be true before starting)
  ↓
Assumptions (what is believed to be true)
  ↓
Evidence Base (what supports assumptions?)
  ↓
Uncertainty Map (knowns / unknowns / unknown unknowns)
  ↓
Risk Awareness (what can go wrong conceptually or procedurally?)
  ↓
Paradigm (general problem-solving lens)
  ↓
Strategy (high-level plan)
  ↓
Alternatives Considered (other possible approaches)
  ↓
Selection Rationale (why this strategy?)
  ↓
Tactics (concrete moves inside strategy)
  ↓
Toolset (mechanisms used: models, frameworks, heuristics, representations)
  ↓
Techniques / Methods (rules for using the tools)
  ↓
Skill Needed (capability required to execute techniques correctly)
  ↓
Algorithm (abstract step logic, if applicable)
  ↓
Procedure (concrete step-by-step execution)
  ↓
Checkpoints / Guardrails (self-check rules)
  ↓
Error Handling (what to do if reasoning fails or result contradicts goal)
  ↓
Metric(s) (how success is measured)
  ↓
Instrumentation (how measurement is obtained)
  ↓
Validation / Verification (correctness + robustness checks)
  ↓
Feedback (results from execution)
  ↓
Reflection (why it worked or failed)
  ↓
Decision Gate (Continue? Revise? Pivot?)
  ↓
Communication / Output Structuring (how result is expressed)
  ↓
Documentation (what to record for reuse)
  ↓
Skill Update (capability adjustment)
  ↓
Practice Plan (deliberate repetition)
  ↓
Knowledge Extraction (structural lesson learned)
  ↓
Abstraction / Schema Update (generalization into reusable template)
  ↓
Transfer Plan (where else this applies)



===========================================================================

# PHASE CONTROL STRATEGIES (Meta-Layer)

Execution Modes:

1️⃣ Sequential Mode
Trigger → Framing → Modeling → ...

2️⃣ Parallel Mode
Run:
- Information + Modeling simultaneously
- Generation + Evaluation (rapid prototyping loop)
- Validation during Construction

3️⃣ Recursive Mode
Inside any phase:
    If subproblem detected →
        Call PS_Phases on subproblem
        Return result to parent phase

4️⃣ Skipping Mode
Skip a phase IF:
- Exit criteria already satisfied
- Problem type does not require it
- Information is trivial

5️⃣ Fast Loop Mode (Compressed Solving)
Framing → Modeling → Generate → Quick Validate
(Used for low-risk problems)

6️⃣ Deep Mode (High Stakes)
Full execution with strict validation and reflection

7️⃣ Early Validation Mode
Validation happens inside:
- Modeling (check structural coherence)
- Generation (test small pieces early)
- Construction (test per module)

8️⃣ Dynamic Phase Re-entry
From any phase:
    If contradiction detected →
        Return to the earliest phase where assumption broke
        
        
===========================================================================

Key Structural Upgrade

Instead of:

PS = Timeline

Make it:

PS = Phase Graph

Each phase is a node.

Edges define allowed transitions.

Example:

Evaluation → Generation

Validation → Modeling

Construction → Generation

Deployment → Framing (if stakeholder rejects)

This gives flexibility without chaos.
