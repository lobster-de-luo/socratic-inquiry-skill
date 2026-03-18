---
name: socratic-inquiry
description: Socratic questioning for bidirectional reasoning calibration. Explicit trigger: user inputs /socratic command or explicitly requests. Six-stage process (Clarification → Assumption → Reasoning → Viewpoints → Consequences → Meta-questioning), ≤5 rounds per stage, 30 rounds total hard limit, strict prohibition on stage merging. Output as dialogic inquiry + secondary conclusion; process stored in session only.
---

# Socratic Inquiry

## When to Use

**Explicit Triggers (Priority)**:
- User inputs `/socratic [topic]` — enter Mode A immediately
- User says "use Socratic method", "Socratic inquiry", etc. — enter after confirming topic

**Cautious Triggers (Require User Confirmation)**:
- User expresses uncertainty ("I think maybe...", "I'm not sure...") — may propose "Shall we dig deeper with Socratic inquiry?"
- Complex reasoning tasks — may propose entering Mode B self-check

**Prohibited**: Do not initiate Socratic mode without user consent or explicit request.

## Six-Stage Inquiry Framework

**Mandatory Constraints (Hard Rules, No Exceptions)**:
- Maximum 5 rounds per stage
- Hard ceiling of 30 total rounds
- **No stage merging** — do not proceed to next stage before completing current stage
- **Must explicitly label stage and round** — prefix each round with "[Stage X: Name] Round N"

### Execution Discipline (Based on Failure Lessons)

**Common Errors (Exposed During Testing)**:
1. ❌ Stage merging: introducing Stage 4 questions while completing Stage 3
2. ❌ Boundary violation: trying to "accelerate" to conclusion at Stage N
3. ❌ Forgotten round tracking: losing track of remaining budget

**Correction Strategies**:
- Before each round, mentally state the current stage objective
- After user response, determine if current stage is complete before advancing
- Strictly adhere to "one question, one answer" rhythm; no question stacking
- Round tracking format: `Total: X rounds, Stage Y (Round Z), Remaining: W rounds`

### 1. Clarification
Objective: Ensure mutual understanding of key terms, reduce cognitive bias.

Common questions:
- "What do you specifically mean by 'X'?"
- "Can you give a concrete example?"
- "How is this different from 'Y'?"

**Limit**: ≤ 5 rounds in this stage

### 2. Assumption Probing
Objective: Expose unstated premises and test their validity.

Common questions:
- "You seem to assume X. Why do you believe this?"
- "If this assumption doesn't hold, what happens to the conclusion?"
- "Are there other possible explanations?"

**Limit**: ≤ 5 rounds in this stage

### 3. Reasoning & Evidence
Objective: Examine argument structure and evidence quality.

Common questions:
- "How do you know this is true?"
- "Are there gaps in this reasoning step?"
- "Are there counterexamples or exceptions?"

**Limit**: ≤ 5 rounds in this stage

### 4. Viewpoint Shifting
Objective: Step outside current framework, explore alternatives.

Common questions:
- "What if we think about it the opposite way?"
- "What would someone with the opposite view say?"
- "Another way to look at this is... does that make sense?"

**Limit**: ≤ 5 rounds in this stage

### 5. Consequences
Objective: Project actual impacts of decisions or conclusions.

Common questions:
- "If we do this, what results?"
- "What are the worst and best case scenarios?"
- "Does this conclusion hold in extreme cases?"

**Limit**: ≤ 5 rounds in this stage

### 6. Meta-Questioning
Objective: Examine the value and boundaries of the question itself.

Common questions:
- "Why ask this question?"
- "What do you hope to gain from this inquiry?"
- "Is this the right question to ask?"

**Limit**: ≤ 5 rounds in this stage, and **only enabled in deep mode**

## Two Usage Modes

### Mode A: Collaborative Inquiry (Thinking with User)

**Initiation**: User inputs `/socratic [topic]` or explicitly requests

**Execution Flow (Strict Adherence)**:
1. **Initialize**: Confirm topic + reset round counter → "Let's explore 'X' using Socratic inquiry. Ready?"
2. **Stage Cycle**: Progress sequentially 1→2→3→4→5→6, **no jumping or merging**
3. **Round Format**:
   ```
   [Stage N: Name] Round M
   [Question content]
   
   (Total: X rounds, Stage Y (Round Z), Remaining: W rounds)
   ```
4. **Stage-Level Decisions**:
   - User response touches core → Complete stage, mark "Stage N complete", proceed to next
   - User response vague/needs deeper probe → Continue to next round in current stage (if already at Round 5, force stage completion)
5. **Termination Conditions** (stop when any is met):
   - Reaches 30 round limit
   - User explicitly says "enough", "that's fine", "end", etc.
   - Completes Stage 6 Round 5
6. **Output**: Mandatory secondary conclusion

**Prohibited Behaviors**:
- Including content from two stages in one response
- Asking "what about Stage N+1" while at Stage N
- Introducing new stage questions when summarizing for user
- Bypassing stage boundaries with words like "meanwhile", "additionally"

### Mode B: Internal Self-Check (AI Self-Calibration)

**Trigger**: Before complex reasoning, or proactively declare after reasoning

**Self-Check List** (Quick version, ≤ 30 seconds):
- [ ] Are key terms clearly defined?
- [ ] What unstated assumptions are relied upon?
- [ ] Is evidence sufficient? Any counterexamples?
- [ ] Are there gaps in the reasoning chain?
- [ ] Are there other explanations?

**Output Format**:
```
🔄 Socratic Self-Check
- Concept: X refers to...
- Assumption: Relies on...
- Reasoning: Evidence..., potential counterexample...
- Conclusion: ...
```

## Output Specifications

### Secondary Conclusion Format

After inquiry concludes, must output structured secondary conclusion:

```
━━━━━━━━━━━━━━━━━━━━
📌 Socratic Inquiry · Secondary Conclusion
━━━━━━━━━━━━━━━━━━━━

【Core Concepts】(Clarified definitions)
...

【Key Assumptions】(Tested/pending assumptions)
- Assumption 1: ... (Confidence: High/Medium/Low)
- Assumption 2: ...

【Reasoning Chain】(Key steps)
1. ...
2. ...

【Counter Perspectives】(Discovered through viewpoint shifting)
...

【Follow-up】(Open questions)
...
━━━━━━━━━━━━━━━━━━━━
```

### Memory Strategy

- **Process**: Stored in current session only, not retained long-term
- **Secondary Conclusion**: If user approves, write to `memory/YYYY-MM-DD.md` or `MEMORY.md`
- **Tag**: Use `#socratic` for future retrieval

## Reference Resources

| File | Content |
|------|---------|
| [references/examples.md](references/examples.md) | Dialogue examples (technical decisions, abstract topics) |
| [references/case-abstract-topics.md](references/case-abstract-topics.md) | Guide for abstract topic inquiry |
| [references/socratic-techniques.md](references/socratic-techniques.md) | Detailed inquiry techniques |
|