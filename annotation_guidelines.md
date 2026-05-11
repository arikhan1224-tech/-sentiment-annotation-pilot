# Annotation Guidelines: Sentiment Classification Pilot

**Project:** Short Text Sentiment Annotation
**Annotator:** [Abdul Rahman]
**Dataset:** dair-ai/emotion (test split sample, 50 examples)
**Tool:** Label Studio (open source)
**Date:** [11/may/2026]

---

## 1. Task Overview

Assign one sentiment label to each short text. Single-label, mutually exclusive.

Labels:
- **positive**
- **negative**
- **neutral**

---

## 2. Label Definitions

### positive
The author expresses happiness, joy, love, gratitude, excitement, satisfaction, or any clearly favorable emotional state.

### negative
The author expresses sadness, anger, fear, frustration, disappointment, regret, or any clearly unfavorable emotional state.

### neutral
The author conveys facts, observations, or descriptions without a clear emotional charge. Mixed or balanced cases where positive and negative are roughly equal also fall here.

---

## 3. Decision Rules

### 3.1 Annotate the author's emotion, not the topic's emotion
A tweet about a sad event written in a detached tone is neutral, not negative.

### 3.2 Sarcasm flips the label
"Oh great, another rainy Monday" is negative, not positive. Label by underlying intent, not surface words.

### 3.3 Dominant signal wins
If both positive and negative cues are present, label whichever drives the tweet. Use neutral only when they balance out.

### 3.4 Punctuation and casing carry meaning
ALL CAPS and multiple exclamation points usually intensify the emotion already present, not change its valence.

### 3.5 No emotion expressed
Pure factual statements ("ate lunch, going back to work") are neutral.

---

## 4. Edge Cases Encountered


### My encountered cases

> **Example #6:** "Oh great another Monday meeting that could have been an email"
> **Considered:** positive, negative
> **Chosen:** negative
> **Rule applied:** 3.2 (sarcasm flips the label). Surface positive "great" is undercut by the complaint that follows ("could have been an email").

> **Example #7:** "My grandmother passed away last night"
> **Considered:** negative, neutral
> **Chosen:** negative
> **Rule applied:** 3.5 vs context. The tweet is technically factual, but the absence of any detached framing means the implied grief reads as the author's expressed emotion. Borderline case worth flagging.

> **Example #19:** "Cannot tell if I am happy or just relieved that it is over"
> **Considered:** positive, neutral
> **Chosen:** positive
> **Rule applied:** 3.3 (dominant signal). "Happy" is named directly and leads the framing; relief supports the positive valence rather than overriding it.

> **Example #22:** "First snowfall of the year, looks beautiful outside"
> **Considered:** positive, neutral
> **Chosen:** positive
> **Rule applied:** 3.3 (dominant signal). "Beautiful" carries genuine positive evaluation, not just neutral description.

> **Example #25:** "Got an unexpected bonus this month, did not see that coming"
> **Considered:** positive, surprise-leaning
> **Chosen:** positive
> **Rule applied:** 3.3 (dominant signal). The unexpectedness is mentioned but the underlying feeling is satisfaction, which dominates.
---

## 5. Quality Process

- Annotated all 50 examples in a single pass
- Edge cases logged inline during the pass
- Final review pass to check label consistency before export
- Optional: compared against source dataset gold labels for an agreement-rate sanity check

---

## 6. Out of Scope

- Multi-label assignment
- Intensity scoring
- Emotion sub-categories (joy vs love, anger vs fear) - collapsed into positive / negative / neutral for this pilot
