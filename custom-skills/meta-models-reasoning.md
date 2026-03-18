---
name: meta-models-reasoning
description: Apply six meta-cognitive frameworks to enhance decision-making and problem-solving quality. Use this skill when analyzing complex problems, making strategic decisions, evaluating options, troubleshooting issues, or when the user explicitly asks for deeper analysis. Forces systematic examination of cognitive biases and blind spots before arriving at conclusions.
license: MIT
version: 1.0
author: Dr Hernani Costa
---

# Meta Models Reasoning Skill

This skill implements six meta-cognitive frameworks that should be applied BEFORE using any domain-specific mental model or framework. These are "models about how to use models" - they catch cognitive shortcuts that lead to poor decisions.

## When to Apply This Skill

**ALWAYS apply when:**
- User asks for analysis of a complex situation
- User needs to make a strategic decision
- User is troubleshooting a problem with multiple variables
- User asks "what should I do about..." or "how should I approach..."
- User presents a problem they've been stuck on
- User asks for recommendations with significant consequences

**SKIP when:**
- Simple factual questions
- Creative writing without analytical component
- Code execution with clear specifications
- User explicitly wants a quick answer without deep analysis

---

## THE SIX META MODELS

### 1. NONLINEARITY CHECK ⚡

**Default assumption:** Relationships are NOT one-to-one and linear.

**Red flags to catch:**
- "If I do X, I'll get Y"
- "A leads to B leads to C"
- Simple cause-effect chains
- Sequential step-by-step logic without feedback loops

**Action required:**
Before proceeding, map the actual relationship web:
1. List all variables/factors involved
2. Draw connections between factors (how do they influence each other?)
3. Identify feedback loops (does output affect input?)
4. Note which factors have conditional relationships ("A affects B only when C is present")

**Output format:**
```
NONLINEARITY ANALYSIS:
Key variables: [list]
Critical interdependencies: [list relationships that aren't obvious]
Feedback loops identified: [list]
Linear assumptions to challenge: [list user's implicit linear assumptions]
```

---

### 2. GRAY THINKING CHECK 🌫️

**Default assumption:** Most solutions exist in the gray zone, not at extremes.

**Red flags to catch:**
- "Should I do A or B?"
- "It's either X or Y"
- Binary framing of complex situations
- False dichotomies
- "The choice is between..."

**Action required:**
1. Identify the apparent binary choice
2. Ask: "Why can't this be A AND B in some proportion?"
3. Map the spectrum between extremes
4. Find gray-zone solutions that combine elements

**Output format:**
```
GRAY THINKING ANALYSIS:
False dichotomy detected: [A] vs [B]
Why these aren't mutually exclusive: [explanation]
Gray-zone alternatives:
  - Option combining 70% A + 30% B: [describe]
  - Option combining 30% A + 70% B: [describe]
  - Novel synthesis: [describe hybrid approach]
Recommended gray-zone position: [specific recommendation]
```

---

### 3. OCCAM'S BIAS CHECK 🔍

**Default assumption:** Reality doesn't owe you simplicity. Over-attribution to single causes is dangerous.

**Red flags to catch:**
- "The problem is basically..."
- "It all comes down to..."
- Single-cause explanations for multi-symptom situations
- Forced consilience (making unrelated things fit one explanation)
- Oversimplification for comfort

**Action required:**
1. List all "symptoms" or manifestations of the problem
2. Challenge: Could these have MULTIPLE causes?
3. Apply Hickham's Dictum: "Problems can have as many causes as they damn well please"
4. Identify which simplifications carry risk

**Output format:**
```
OCCAM'S BIAS ANALYSIS:
Symptoms/manifestations observed: [list]
Single-cause explanation (tempting): [describe]
Alternative multi-cause hypothesis: [describe]
Simplifications made and their risk level:
  - [Simplification 1]: Risk = [low/medium/high], because [reason]
  - [Simplification 2]: Risk = [low/medium/high], because [reason]
Black boxes acknowledged: [areas of uncertainty we're accepting]
```

---

### 4. FRAMING BIAS CHECK 🖼️

**Default assumption:** The way a problem is presented is NOT necessarily the best way to think about it.

**Red flags to catch:**
- Accepting problem framing as given
- Using familiar frameworks because they're familiar
- "The issue is A, B, C" (as presented by user or context)
- Industry-standard categorizations applied without question

**Action required:**
1. Identify current framing of the problem
2. Generate 2-3 alternative framings
3. Evaluate: Which framing leads to better solutions?
4. Choose framing consciously, not by default

**Output format:**
```
FRAMING BIAS ANALYSIS:
Current framing: [how problem was presented]
Alternative framing 1: [reframe] → leads to solutions like [examples]
Alternative framing 2: [reframe] → leads to solutions like [examples]
Alternative framing 3: [reframe] → leads to solutions like [examples]
Most productive framing: [selection with justification]
```

---

### 5. ANTI-COMFORT CHECK 🔥

**Default assumption:** If you feel comfortable with your analysis, you might be missing something.

**Red flags to catch:**
- Feeling certain about the answer
- Analysis that confirms initial intuition
- No parts of the analysis feel difficult
- Quick arrival at "obvious" solution

**Action required:**
1. Identify what would make current conclusion WRONG
2. Steel-man the opposite position
3. Find the most uncomfortable implication of current analysis
4. Actively seek disconfirming evidence

**Output format:**
```
ANTI-COMFORT ANALYSIS:
Current comfortable conclusion: [state it]
What would make this wrong: [list conditions]
Steel-manned opposite view: [best argument against current conclusion]
Most uncomfortable implication: [what we're avoiding thinking about]
Confidence adjustment: [original confidence] → [adjusted confidence]
```

---

### 6. DELAYED DISCOMFORT CHECK ⏰

**Default assumption:** Discomfort is inevitable. Choose upfront discomfort over delayed discomfort.

**Red flags to catch:**
- Choosing easier analysis path
- Skipping "hard" parts of the problem
- Accepting surface-level solutions
- "Good enough for now" thinking on critical decisions

**Action required:**
1. Identify where you're tempted to take shortcuts
2. Calculate delayed discomfort: What problems does the shortcut create later?
3. Make explicit choice: Pay now or pay later?

**Output format:**
```
DELAYED DISCOMFORT ANALYSIS:
Shortcuts tempting to take: [list]
For each shortcut:
  - Upfront effort saved: [describe]
  - Downstream problems created: [describe]
  - Delayed discomfort multiplier: [estimate: 1x, 2x, 5x, 10x worse later?]
Recommendation: [which discomforts to take upfront vs. defer]
```

---

## APPLICATION PROTOCOL

### For Complex Problems (apply full protocol):

1. **INTAKE**: State the problem as presented
2. **NONLINEARITY**: Map the variable relationships
3. **GRAY THINKING**: Challenge binary framings
4. **OCCAM'S BIAS**: Check for dangerous oversimplification
5. **FRAMING BIAS**: Generate alternative problem framings
6. **ANTI-COMFORT**: Stress-test comfortable conclusions
7. **DELAYED DISCOMFORT**: Identify where to invest effort upfront
8. **SYNTHESIS**: Provide recommendation with explicit confidence level

### For Medium Complexity (apply abbreviated protocol):

Apply checks 1, 2, 4, and 5 only. Note which checks were skipped.

### For Quick Analysis (apply minimal protocol):

Apply check 4 (Framing Bias) and check 5 (Anti-Comfort) only. Explicitly flag that full analysis was not performed.

---

## OUTPUT STRUCTURE

When this skill is activated, structure response as:

```
## Meta-Model Analysis

[Apply relevant checks with their output formats]

## Synthesis & Recommendation

**Confidence Level**: [Low/Medium/High] 
**Key Uncertainties**: [list]
**Recommendation**: [clear recommendation]
**If Wrong, Likely Because**: [primary risk factor]
```

---

## IMPORTANT CAVEATS

This skill adds cognitive overhead. Apply proportionally to:
- Decision stakes (higher stakes = fuller analysis)
- Decision reversibility (irreversible = fuller analysis)
- Available time (less time = abbreviated protocol)
- User preference (if user wants quick answer, flag tradeoff)

Never use this skill to overcomplicate genuinely simple questions.
