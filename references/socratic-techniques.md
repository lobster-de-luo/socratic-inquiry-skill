# Socratic Inquiry Techniques Detailed

## Origin and Core Philosophy

Socratic Questioning originates from the teaching method of ancient Greek philosopher Socrates. The core is not transmitting knowledge, but through systematic questioning, helping the other party:
1. Clarify thinking
2. Test assumptions
3. Discover contradictions
4. Build more solid arguments

## Six Stages Deep Dive

### 1. Clarification Questions

**Purpose**: Ensure both parties are on the same channel, eliminate the illusion of "everyone understands."

**Technical Points**:
- Probe abstract vocabulary for concrete meaning
- Request examples
- Distinguish subtle differences between near-synonyms

**Pitfalls**:
- Don't become "nitpicking" questioning
- Avoid making the other party feel interrogated

**Examples**:
- ❌ "What do you mean?" (Aggressive)
- ✅ "When you say 'efficiency,' do you mean development speed or runtime performance?"

### 2. Assumption Probing

**Purpose**: Expose hidden premises; many disagreements stem from different assumptions rather than different conclusions.

**Technical Points**:
- Identify implicit premises in statements
- Test universality and necessity of assumptions
- Explore "if it doesn't hold" scenarios

**Common Assumption Types**:
- Causal assumption: A causes B
- Value assumption: X is more important than Y
- Reality assumption: The situation is Z

**Examples**:
- "You assume adding people will speed up progress, but The Mythical Man-Month tells us this may backfire."

### 3. Reasoning & Evidence

**Purpose**: Examine logical validity of arguments and sufficiency of evidence.

**Technical Points**:
- Distinguish facts from opinions
- Check evidence sources and quality
- Look for counterexamples and exceptions
- Identify logical fallacies

**Common Logical Fallacies Quick Reference**:
| Fallacy | Manifestation | Response |
|---------|--------------|----------|
| Appeal to Authority | "Expert X says..." | "What is X's basis?" |
| Straw Man | Distort opponent's view then attack | "My understanding of your meaning is... is that correct?" |
| Slippery Slope | "A will lead to B will lead to C..." | "What is the probability of each step?" |
| False Dilemma | "Either A or B" | "Is there a third possibility?" |

### 4. Viewpoint Shifting

**Purpose**: Break confirmation bias, force consideration of opposing positions.

**Technical Points**:
- Perspective-taking: If I were the opponent, how would I refute?
- Time-jumping: Will this still hold in 5 years?
- Role-switching: How do different stakeholders view this?

**Powerful Questions**:
- "How would the smartest opponent attack this view?"
- "Under what circumstances would this conclusion completely fail?"
- "If resources/constraints were completely opposite, what would the solution be?"

### 5. Consequences

**Purpose**: Bring abstract reasoning back to real world, test feasibility.

**Technical Points**:
- Second/third-order effect thinking
- Extreme case testing
- Cost-benefit quantification (if possible)

**Framework**:
```
If implementing X:
- Direct results: ...
- Indirect results: ...
- Worst case: ...
- Best case: ...
- Irreversible?
```

### 6. Meta-Questioning

**Purpose**: Prevent wasting energy on wrong questions.

**When to Use**:
- Question itself may be biased
- Question may be symptom rather than root cause
- Exploring motivation and real needs

**Technical Points**:
- Distinguish between "problem we want to solve" and "real problem"
- Check question boundaries and applicability
- Explore alternative question frameworks

**Powerful Questions**:
- "Is this a technical problem or an organizational problem in disguise?"
- "If this problem didn't exist, what would happen?"

## Implementation Techniques

### Rhythm Control

**Short Cycles**: Don't pursue more than 2 rounds per stage, maintain flow.

**Checkpoints**: Briefly summarize core discoveries after every 2 stages.

**Exit Conditions**:
- User explicitly says "enough"
- Reaches 12 round limit
- Discover fundamental contradiction requiring separate handling
- Enter execution/action phase

### Tone and Relationship

**Correct Posture**:
- "Let's figure this out together"
- "I'm not sure myself"
- "This is a good question"

**Avoid**:
- "You're wrong"
- "Obviously..."
- "But..." (use "At the same time..." or "Another angle...")

### Recording and Follow-up

**Real-time Recording**:
- Key term definitions (Stage 1 output)
- Identified assumptions (Stage 2 output)
- Counter perspectives (Stage 4 output)
- Open questions (Stage 6 output)

**Follow-up Actions**:
- Convert secondary conclusion to todos
- Set up experiments to validate assumptions
- Schedule research on counter perspectives

## Common Scenario Applications

### Technical Decisions

Applicable: Architecture selection, technical debt handling, refactoring scope

Key stages: 2 (Assumptions), 3 (Evidence), 5 (Consequences)

### Product Strategy

Applicable: Feature prioritization, user assumptions, market positioning

Key stages: 1 (Concepts), 4 (Viewpoints), 6 (Question itself)

### Personal Dilemmas

Applicable: Career choices, learning paths, time management

Key stages: 1 (Clarify what you want), 2 (Hidden assumptions), 5 (Project consequences)

## Self-Check Template (AI Internal Use)

```
🔄 Socratic Self-Check · Quick Version
━━━━━━━━━━━━━━━━━━━━
Concept: What I mean by X specifically refers to...
Assumption: I rely on... (if not established...)
Reasoning: Based on... evidence (counterexample: ...)
Perspective: Opponent would say... (response: ...)
Consequences: Direct/indirect effects after implementation...
━━━━━━━━━━━━━━━━━━━━
Confidence: _/10  Main risk: ...
```

## Reference Resources

- *The Miniature Guide to Critical Thinking Concepts and Tools* by Richard Paul & Linda Elder
- *Asking the Right Questions: A Guide to Critical Thinking* by Neil Browne & Stuart Keeley
- Socratic Method: https://en.wikipedia.org/wiki/Socratic_method
