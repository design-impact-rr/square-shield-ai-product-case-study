This file is intentionally concrete to show how I work with AI during discovery, not just that I use it.

# Square Shield – Discovery AI Prompts

This file summarizes example AI prompts and workflows I used (and in some cases would use) during discovery for Square Shield. The goal is to show how AI helped me synthesize noisy feedback, sharpen the problem, and explore options without replacing direct judgment.

---

## 1. Synthesizing seller reviews and complaints

### 1.1 Clustering themes across 100 reviews

**Prompt template**

> I will paste a set of [N] public reviews and complaints from small businesses using Square for payments and POS.  
> 1. Identify the top 5–7 recurring themes you see (e.g., funds held, outages, disputes, support).  
> 2. For each theme, list: a short name, 2–3 sentences describing the pain, and a rough sense of frequency.  
> 3. Highlight any themes that directly affect cash flow or the ability to process payments in real time.  
> Output as a markdown table with columns: Theme, Description, Impact on seller, Approx. frequency.

**How I used it**

- Validated my manual coding of the 100‑review dataset and ensured I was not missing smaller but important themes.
- Used “Impact on seller” language as a starting point for the “real pain behind these problems” section in the PRD.

---

### 1.2 Extracting representative quotes (then paraphrasing)

**Prompt template**

> I will paste multiple reviews about [topic: e.g., funds held / account frozen].  
> 1. Extract 3–5 representative quotes that illustrate the core sentiment.  
> 2. For each quote, add a one‑sentence explanation of what the seller is afraid of or frustrated by.  
> 3. Suggest a neutral, paraphrased version of each quote that can be used in a product document without exposing personal details.

**How I used it**

- Pulled out strong, emotionally clear lines about funds holds, outages, disputes, and support.
- Used the paraphrased versions in `insights-summary.md` and `prd.md` to avoid copying raw reviews.

---

## 2. Sharpening the problem statement

### 2.1 Converging on a single problem statement

**Prompt template**

> Here is a summary of user pains and patterns related to Square (funds held, outages, disputes, support).  
> Draft 5 different one‑sentence problem statements that:  
> - Focus on the seller’s point of view.  
> - Emphasize loss of control and trust, not missing features.  
> - Avoid jargon.  
> Then suggest one that feels the most specific and high‑stakes, and explain why in 2–3 sentences.

**How I used it**

- Iterated on wording until I landed on the reframed problem statement in prd.md.
- Checked that the final statement was grounded in the 100‑review analysis, not in hypothetical problems.

---

## 3. Exploring user segments and jobs‑to‑be‑done

### 3.1 Identifying the most exposed niche

**Prompt template**

> Based on the following patterns of pain (funds held, outages, disputes, support), suggest 3–4 concrete seller segments that are most exposed to these risks.  
> For each segment, describe:  
> - Typical business type and size  
> - Why outages / holds / disputes are especially damaging  
> - What “a bad week” looks like for them when Square fails  
> Keep it specific (e.g., “busy coffee shop doing 400 tickets/day”) rather than generic.

**How I used it**

- Sanity‑checked my focus on “reliability‑critical” food & beverage and personal services.
- Borrowed phrases like “a bad week looks like…” to inform the Target users and Underserved niche sections in prd.md.

---

### 3.2 Drafting jobs‑to‑be‑done

**Prompt template**

> Using the pains and segments described here, write 3–5 jobs‑to‑be‑done statements for sellers who rely on Square.  
> Use this format:  
> “When [situation], I want [motivation], so I can [desired outcome].”  
> Focus on situations involving outages, account reviews, disputes, and support interactions.

**How I used it**

- Used JTBD to ensure the MVP capabilities (dashboard, continuity mode, dispute assistant, priority support) directly mapped to real jobs.

---

## 4. Designing research questions and interviews

### 4.1 Drafting interview guides

**Prompt template**

> Help me design a 45‑minute interview guide for Square sellers who have experienced one or more of the following:  
> - Account holds longer than 7 days  
> - Chargebacks or disputes  
> - Outages during peak hours  
> 1. Start with 3–4 warm‑up questions about their business.  
> 2. Add 8–10 questions about how these incidents unfolded, how they found out, and what they did next.  
> 3. Add 3–4 questions about backup tools and what “feeling protected” would look like.  
> Output as a numbered list.

**How I used it**

- Quickly generated a first‑pass interview guide, then edited it for tone and flow.
- Ensured coverage of lifecycle moments (onboarding, first big transaction, first outage, first dispute).

---

### 4.2 Drafting survey questions

**Prompt template**

> I want to design a short, in‑product survey triggered after a seller experiences a hold, dispute, or outage.  
> 1. Propose up to 5 multiple‑choice questions that measure trust, clarity, and perceived support.  
> 2. Propose 2–3 optional free‑text questions to capture what they did next and what “good” would have looked like.  
> Make sure the language is simple and neutral.

**How I used it**

- Used this to outline the “in‑product surveys” piece in the research plan and to seed potential future instrumentation.

---

## 5. Translating insights into requirements

### 5.1 Mapping pains → MVP features

**Prompt template**

> I will paste a list of seller pains and a draft list of potential features for a product called “Square Shield.”  
> 1. Create a table that maps each pain to one or more features.  
> 2. For each mapping, explain in 1–2 sentences how the feature addresses the pain.  
> 3. Flag any pains that do not have a clear feature mapping yet.

**How I used it**

- Checked that each core MVP capability tied back to specific patterns from the 100‑review analysis.
- Used gaps to refine non‑goals and identify future roadmap ideas.

---

### 5.2 Stress‑testing non‑goals

**Prompt template**

> Here is a draft list of explicit non‑goals for the Square Shield MVP.  
> For each one:  
> - Rephrase it to be as clear and specific as possible.  
> - Suggest a one‑sentence rationale that a stakeholder would understand.  
> - Suggest a risk if we accidentally try to include it in v1.

**How I used it**

- Clarified non‑goals in the PRD and made the tradeoffs more explicit.
- Ensured I could explain “why not v1” in concrete terms.

---

## 6. Guardrails and limitations

I treated these AI prompts as accelerators, not decision‑makers:

- Always cross‑checked AI‑generated themes against the actual reviews and my own synthesis.
- Re‑wrote any phrasing that felt too generic or confident where the underlying data was thin.
- Used AI mainly to structure thinking, explore alternative wordings, and pressure‑test my logic before committing it into insights-summary.md and prd.md.
