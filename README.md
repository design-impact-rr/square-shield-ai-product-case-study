To quickly understand this work sample:
- Read the overview and problem section in README.md.
- Skim `research/insights-summary.md` for 100‑review insights.
- Review `product/prd.md` to see how insights translate into an AI‑native product.
- Check `ai-playbooks/discovery-prompts.md` to see how AI was used in discovery.

# Square Shield – AI‑Native Risk & Reliability Layer for Square Sellers

Work sample for the Square Associate Product Manager Program (APM) – AI‑native product case study.

---

## 1. Overview

**Problem:**  
Square sellers consistently report that their biggest pain is fragile, opaque access to their money and tools: unexpected account holds, chargebacks, outages, and unclear risk decisions that leave businesses unable to process payments or pay bills.

**Solution:**  
Square Shield – a risk and reliability layer that uses AI to detect, explain, and proactively mitigate issues for sellers. It combines a transparent risk dashboard, outage‑ready continuity mode, dispute assistant, and priority human support to reduce surprise and rebuild trust.

**Who it’s for:**  
- Reliability‑critical small businesses (e.g., coffee shops, cafes, food trucks, salons, service providers) that are highly sensitive to downtime and funds‑on‑hold moments.  
- Time‑bound, revenue‑dense operators where peak hours and large transactions make risk and reliability existential.

**My role:**  
Product lead for discovery, scoping, and defining the MVP (research, synthesis, requirements, and experience flows). Used qualitative analysis of 100 real seller reviews plus AI‑native workflows to shape the direction of Square Shield.

---

## 2. Problem & Context

### What specific problems are sellers facing today?

- **Funds held / accounts frozen:** Sudden holds or deactivations with little warning, no clear timelines, and limited recourse, often during peak revenue periods.  
- **Outages & reliability:** Full‑day or recurring outages during lunch/dinner rush, sometimes with no proactive communication.  
- **Disputes & chargebacks:** Belief that “you always lose” chargebacks, confusion about fee refunds, and opaque bank‑driven processes.  
- **Poor / slow support:** Long resolution times, being bounced between agents, and canned responses during high‑stress moments.

### Why is this costly or risky for them and for Square?

- **For sellers:**  
  - Immediate cash‑flow damage and inability to pay staff, rent, or suppliers.  
  - Emotional distrust and a rush to adopt backup tools or switch away from Square.  
- **For Square:**  
  - Erosion of trust in Square as an operating system for small businesses.  
  - Increased churn and support burden when minor incidents compound into existential crises for sellers.

### How did I ground this in real signals?

- Analyzed 100 public reviews and complaint threads (BBB, Square Community, Reddit, review sites, and industry coverage) to surface patterns around funds held, outages, disputes, and support.  
- Clustered recurring themes and representative quotes, then mapped them to candidate product opportunities in Square Shield.

### Constraints and assumptions

- **Constraints:**  
  - Card‑network and bank‑owned rules around dispute outcomes and chargeback timelines.  
  - Internal risk‑policy guardrails that limit how much risk Square can take on for merchants.  
  - Operational cost structure of priority human support.
- **Assumptions:**  
  - Sellers will pay more for reliability and predictability if value is obvious and outcomes are transparent.  
  - A focused, narrowly scoped MVP will yield stronger signals than an attempt to fix every POS or reporting pain.

---

## 3. Research & Insights

### 3.1 Inputs

**Sources used**

- Public reviews and complaints from:  
  - Better Business Bureau (BBB)  
  - Square Community forums  
  - Reddit r/smallbusiness  
  - Trustpilot, Capterra, Software Advice, and other review platforms  
  - Industry and news coverage of Square outages and disputes  
- Total: 100 public reviews and complaint threads selected for relevance to risk, reliability, disputes, and support.

**How they were analyzed**

- Manually read and tagged each item into one core theme (funds held, outages, disputes, support, hardware friction).  
- Summarized top patterns, representative quotes, and implications in `research/insights-summary.md`, with raw URLs in `research/raw-sources.md`.

### 3.2 Key Insights

**Insight 1 – Risk, reliability, and support are one trust problem**  
Sellers do not separate “funds frozen,” “outage,” and “slow support” in their heads; they see them as a single breakdown of trust in Square as an operating system.  
→ *Implication:* Square Shield must unify these experiences (risk, uptime, support) rather than treating them as siloed features.

**Insight 2 – Lack of communication hurts more than the event**  
Reviewers repeatedly call out surprise, black‑box status, and delayed communication as the main drivers of frustration, even when the technical outcome is “okay.”  
→ *Implication:* Square Shield should prioritize proactive alerts, clear timelines, and plain‑language explanations, not only improving the underlying event itself.

**Insight 3 – High‑risk, high‑revenue niches are the most vocal**  
Coffee shops, food trucks, cafes, and time‑based services (salons, appointments) show up repeatedly in complaints about holds and outages because every hour materially hurts revenue.  
→ *Implication:* The MVP should focus first on reliability‑critical verticals where the value of predictability is highest and most monetizable.

See `research/` for more detailed notes and structured findings.

---

## 4. Target Users & Use Cases

### 4.1 Personas

**Persona A – Busy Coffee Shop / Café Owner**

- Goals:  
  - Process every transaction quickly during morning and lunch rush.  
  - Avoid days‑long outages or account freezes that stop operations.  
- Pains:  
  - Outages during peak hours, account freezes right before payroll, and “funds under review” before a big event.  
- Relevant Square products:  
  - Square POS, hardware stands, Square Online (for orders), Square for Retail.

**Persona B – Time‑Bound Service Provider (Salon / Studio Owner)**

- Goals:  
  - Lock in deposits and large‑ticket appointments with confidence.  
  - Avoid disputes that eat into already tight margins.  
- Pains:  
  - Chargebacks on large deposits, slow resolution timelines, and lack of clear guidance on what evidence to provide.  
- Relevant Square products:  
  - Square Appointments, Square POS, Square for Retail.

### 4.2 Primary Use Cases

**Use case 1 – Understand why a payout is delayed**  
When a seller sees “funds held” or “account under review,” they want a clear explanation, realistic timeline, and concrete next steps, not a generic “under review” message.

**Use case 2 – Survive an outage without losing peak‑hour revenue**  
During a platform or connectivity outage, the seller wants a safe offline or continuity mode that keeps payments flowing within defined limits, plus clear guidance on how to reconcile afterward.

**Use case 3 – Navigate a dispute without feeling alone**  
When a chargeback is filed, the seller wants a guided flow that explains chances of success, what evidence to provide, and how long the process will take, with AI‑assisted drafting of responses and explanations.

---

## 5. MVP Definition

### 5.1 MVP Goals

**For sellers:**

- Reduce surprise and panic around funds held, outages, and disputes.  
- Give them control and clarity through proactive alerts, transparent timelines, and clear next steps.  
- Preserve access to revenue and protect against catastrophic business‑killing downtime.

**For Square:**

- Strengthen trust in Square as a dependable operating system for small businesses.  
- Reduce churn and support burden by preventing small incidents from becoming existential crises.  
- Test whether a focused reliability‑ and protection‑driven product can command a premium in key segments.

### 5.2 Core v1 Capabilities

**Capability 1 – Transparent risk and holds dashboard**

- Shows why a transaction or account is under review and the expected resolution timeline in plain language.  
- Provides status states (e.g., “Reviewing first large payment,” “Pattern flagged: high disputes”) and a checklist of what the seller can do now.  
- Sends proactive alerts as risk thresholds are approached (e.g., spike in ticket size or dispute rate).

**Capability 2 – Outage‑ready “continuity mode”**

- Automatically enables a safe “offline but controlled” acceptance mode when connectivity or platform issues are detected, with configurable limits (amount per transaction, total time).  
- Displays a simple continuity checklist in‑app (backup hotspot, QR for online pay, etc.).  
- Includes post‑incident reconciliation tools to match offline payments and notify customers if anything failed.

**Capability 3 – Dispute and chargeback assistant**

- Guides sellers through a step‑by‑step dispute flow that explains likelihood of success, required evidence, and deadlines.  
- Auto‑generates evidence packages from existing Square data (receipts, signatures, order history, chat, etc.).  
- Provides transparent status tracking with clear messages (e.g., “Bank is reviewing,” “Evidence submitted,” “Expected decision by X”) and clarifies Square’s obligations (when fees are refunded vs. not).

**Capability 4 – Priority human support for critical events**

- Surfaces a dedicated support channel (phone/chat) in‑product when an account is under review, a large portion of funds is held, or an outage is detected for that seller.  
- Defines SLAs for first response and updates (e.g., response within X business hours, daily status updates) for these events.  
- Ensures one clear owner of the issue rather than being bounced between agents.

### 5.3 Explicit Non‑Goals (v1)

**Non‑goal 1 – No overhaul of core POS inventory or reporting**  
Square Shield does not try to fix advanced inventory management, multi‑location reporting, or complex SKU workflows in v1. Those are separate, long‑term product lines.  
→ *Why out of scope:* They dilute focus from the core risk, reliability, and support narrative and increase complexity of the MVP.

**Non‑goal 2 – No guaranteed dispute outcomes**  
Square Shield does not promise to “win” disputes; it clarifies process, expectations, and evidence, but outcomes are still governed by banks and card networks.  
→ *Why out of scope:* Promising outcomes would be misleading and increase risk for both Square and sellers.

**Non‑goal 3 – No fully custom risk‑control knobs**  
Square Shield does not expose raw risk‑policy toggles to merchants (e.g., “turn off fraud checks”), which could materially increase fraud losses.  
→ *Why out of scope:* Such controls belong to a different risk‑policy layer; Shield focuses on transparency and support around existing policies.

---

## 6. How AI Is Used

### 6.1 AI Use Cases

**Discovery**

- Used AI to cluster 100 noisy reviews into themes, surface representative quotes, and highlight cross‑cutting patterns (e.g., funds held + outages + support as one trust problem).  
- Leveraged AI to draft concise insight statements and problem‑framing language that later became the core of `research/insights-summary.md`.

**Product**

- Uses AI to translate complex internal risk and dispute signals into plain‑language explanations and “what you can do next” recommendations surfaced in the dashboard and dispute assistant.  
- Employs AI‑assisted drafting of dispute narratives and evidence‑summary text, editable by the seller before submission.

**Operations**

- Assists internal teams (support, risk ops, sales) by auto‑summarizing incident patterns, flagging high‑risk accounts, and surfacing relevant policies and playbooks faster.  
- Supports faster first‑response triage for critical events flagged in‑product.

### 6.2 AI Workflows & Prompts

**Example workflow 1 – Theme clustering of reviews**

- Input: Raw review snippets and complaint text.  
- AI behavior: Cluster into 5–7 themes, generate short descriptions and impact statements.  
- Output: Seed input for the “Key Insights” section in the research summary and PRD.

**Example workflow 2 – Guided dispute‑flow drafting**

- Input: Open dispute, basic case details, and seller‑supplied evidence.  
- AI behavior: Draft a bank‑ready dispute narrative and bullet‑point summary of evidence.  
- Output: Editable text block surfaced in‑app for the seller to review and send.

See `ai-playbooks/` for concrete prompt examples and flows.

### 6.3 Risks & Guardrails

**Potential failure modes or biases**

- Over‑reliance on AI could mask nuanced seller context or lead to overly confident, generic explanations.  
- AI‑generated explanations may drift into legal or regulatory territory if not constrained by policy guardrails.  
- Too‑aggressive automation in critical events might erode the human‑support “safety net” sellers expect.

**Guardrails and product decisions**

- All AI outputs are reviewed and editable by the seller or a human agent; explanations are framed as guidance, not guarantees.  
- Clear disclaimers indicate where processes are governed by banks and card networks, not Square.  
- Priority human support remains the ultimate escalation path for money‑access and outage emergencies.

---

## 7. Experience Overview

### 7.1 Key Flows

**Flow 1 – Account under review**

1. Seller receives proactive in‑app notification: “Your account is under review because of [reason].”  
2. Dashboard shows: explanation, expected timeline, what documents or actions are needed, and an estimated “good‑to‑go” date.  
3. If the seller disagrees or wants to escalate, they can click into a guided flow that surfaces a support ticket and a summary of the situation to the human agent.

**Flow 2 – Outage during rush hour**

1. POS detects connectivity or platform issues and automatically switches to “continuity mode” within safe limits.  
2. Staff see a clear banner: “Accepting offline payments for up to $X per transaction; reconcile later.”  
3. After the incident, a reconciliation tool helps match offline payments, reconcile with Square, and notify customers of any discrepancies.

### 7.2 Sample Screens / Artifacts

- In a live implementation, Figma or mockups would show:  
  - The risk and holds dashboard with status cards, timelines, and checklists.  
  - The outage‑mode banner and reconciliation flow screens.  
  - The dispute assistant with guided steps, evidence checklist, and AI‑drafted narrative editor.

*(You can add links to Figma or PDFs here if you create them later.)*

---

## 8. Metrics & Success Criteria

### 8.1 Core Metrics

**Seller‑facing metrics**

- Reduction in time to resolution for account reviews and disputes.  
- Decrease in “funds‑held”‑related support tickets and negative reviews mentioning “no communication” or “no explanation.”  
- Increase in perceived trust and control scores (e.g., via surveys asking “I understand what’s happening when my account is under review”).

**Business / risk metrics**

- Volume and retention lift among Shield subscribers vs. non‑subscribers in the same risk and size segments.  
- Support ticket volume and escalation rates for holds, outages, and disputes among Shield users.  
- Fraud and loss impact under the new transparency and continuity policies.

### 8.2 How I’d Measure v1

- Instrument key events in the dashboard and assistant (e.g., “clicked explanation,” “sent dispute,” “used continuity mode”).  
- Run early pilots with reliability‑critical merchants to track churn, transaction volume, and support patterns.  
- After 3–6 months, define “good” as:  
  - Meaningful reduction in negative mentions of “funds held,” “no communication,” and “outage” for Shield users.  
  - Positive lift in retention and willingness to pay for the Shield tier.

---

## 9. V2+ Roadmap

**V2 idea 1 – Expanded outage protection and integrations**  
- Deepen continuity mode with integrations to backup processors or hardware partners (e.g., LTE‑enabled stands), so continuity is more seamless and less manual.  
- *Why it matters:* Reduces cognitive overhead and improves reliability for high‑volume merchants.

**V2 idea 2 – Risk‑based protection tiers**  
- Offer different Shield tiers with tradeoffs (e.g., faster review timelines, higher dispute‑fee‑credit caps, or more generous offline limits) based on risk profile.  
- *Why it matters:* Turns Square’s risk framework into a value‑based, monetizable protection layer.

**V2 idea 3 – AI‑driven incident summaries and learning**  
- After each outage or major incident, automatically generate a brief, human‑reviewable summary for the seller and internal teams, including “what happened, what changed, and how to prepare next time.”  
- *Why it matters:* Accelerates learning and trust recovery after incidents.

Optional: With access to internal data, I’d explore deeper risk‑policy and pricing experiments, tailored to different verticals and risk bands.

---

## 10. My Process & Learnings

**How I approached this project end‑to‑end**

- Started with open‑ended analysis of 100 reviews to ground the problem in real pain, not assumptions.  
- Used AI‑assisted clustering and framing to turn messy complaints into structured insights and a clear problem statement.  
- Translated insights into a narrow, MVP‑focused PRD and mapped pains to concrete capabilities and non‑goals.  
- Designed how AI would augment discovery, product experience, and internal operations, while respecting guardrails and human oversight.

**What I’d do differently with more time or internal data**

- Deep‑dive into Square’s internal data to triangulate review patterns with hold‑rates, outages, and dispute outcomes.  
- Run real user interviews or diary studies with 20–30 sellers to validate the most painful scenarios and test mocks.  
- Partner with engineering, design, and risk teams to pressure‑test feasibility and guardrails of the proposed workflows.

**How this reflects how I’d work as an APM at Square**

- Ground product ideas in real‑world signals first, then ruthlessly scope MVPs.  
- Use AI‑native workflows throughout discovery, requirements, and experimentation, always keeping humans in the loop.  
- Focus on rebuilding trust and reliability where it matters most for revenue‑critical sellers, not just shipping features.
