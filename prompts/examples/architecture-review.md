# Architecture Review Prompt

## Name
Architecture Review

## Intent / When to use

**For Product Owners reviewing agent proposals.**

Use this prompt when an agent has proposed a system architecture or major architectural change. This prompt helps you systematically evaluate the proposal against your requirements before approving or requesting changes.

**Workflow:**
1. Product Owner defines requirements and vision
2. Agent proposes architecture based on those requirements
3. Product Owner uses this prompt to review the agent's proposal
4. Product Owner approves, iterates, or rejects based on the review

## Inputs (required)

- {{REQUIREMENTS}} — Product owner's requirements and constraints
- {{AGENT_PROPOSAL}} — The agent's proposed architecture (design, decisions, trade-offs)
- {{PROJECT_CONTEXT}} — Any existing decisions or architectural constraints from DECISIONS.md

## Prompt

You are an expert technical reviewer evaluating an architectural proposal. Given the product owner's requirements and the agent's proposed architecture, provide:

1) **Alignment Check** — Does the proposal satisfy all stated requirements?
2) **Trade-offs Analysis** — What trade-offs did the agent make? Are they justified?
3) **Risk Assessment** — What architectural risks or technical debt might this create?
4) **Alternative Approaches** — What alternatives were considered? Why was this chosen?
5) **Decision Clarity** — What assumptions does this proposal make about technology, scale, or constraints?
6) **Implementation Feasibility** — Is this architecture implementable with the stated constraints?
7) **Recommendation** — Approve as-is, request changes, or reject with rationale.

## Recommended settings

- System message: You are a technical architect evaluating proposals for clarity, completeness, and alignment with requirements.
- Model: Any capable LLM; use lower temperature (0.2–0.3) for consistent analysis.
- Context: Include relevant DECISIONS.md entries for architectural history.

## Example input

**REQUIREMENTS:**
"Build a web API that supports 10,000 concurrent users. Must use Node.js. Data must be queryable in real-time. Team has 2 engineers, 3-month timeline."

**AGENT_PROPOSAL:**
"Architecture: Express.js + PostgreSQL with Redis caching. Horizontal scaling via Docker + Kubernetes. Estimated 6 weeks to MVP."

**PROJECT_CONTEXT:**
"Previous decision: Use Node.js for all services (DECISIONS.md ADR-003)"

## Expected response format

- Alignment Check (yes/no + rationale)
- Trade-offs Analysis (numbered list)
- Risk Assessment (identified risks + severity)
- Alternatives (list of options considered)
- Decision Clarity (assumptions listed)
- Feasibility (yes/no + effort estimate)
- Recommendation (approve/request changes/reject)

## Notes / Safety checks

- This prompt is for **Product Owner review**, not for agents to use on themselves
- The product owner makes the final decision; use this prompt to systematically evaluate proposals
- Document the review outcome in DECISIONS.md if approved
- If changes are requested, the agent should revise the proposal and resubmit for re-review
