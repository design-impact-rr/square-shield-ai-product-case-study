# Square Shield – Product Requirements (PRD)

## 1. Product overview

### Vision

Make Square the most trusted way for reliability‑critical small businesses to accept payments by giving them predictable access to funds, continuity during incidents, and clear, human support when things go wrong. Square Shield is designed and iterated with AI‑native workflows, using AI to analyze seller feedback, surface risk patterns, and power in‑product guidance throughout the experience.

### Problem

Square sellers consistently report that their biggest pain is not “missing features” but fragile, opaque access to their money and tools: unexpected account holds, outages, hardware disconnects, and slow, hard‑to‑reach support that leave businesses unable to take payments or pay bills.

### Target users

- Small to mid‑size, volume‑sensitive businesses: coffee shops, cafes, food trucks, fast‑casual, salons, and appointment‑based services.
- Heavy dependence on peak hours (morning rush, lunch, evening service, booked slots).
- Limited staff and owner time to fight disputes, chase support, or manage multiple providers (owner‑operator heavy).
- Moderate to high chargeback exposure (online orders, phone orders, deposits, large tickets).

---

## 2. User research plan

### 2.1 Objectives (questions to answer)

- How do funds holds, disputes, outages, and support gaps actually impact day‑to‑day operations and cash flow for small businesses using Square?
- At what points in the lifecycle (onboarding, first large transaction, disputes, busy hours) do breakdowns most often occur?
- What “workarounds” are businesses using today (backup processors, manual invoicing, cash, PayPal/Stripe) and what do they wish Square did instead?
- Which segments are most vulnerable (by size, vertical, ticket size, risk profile) and least well‑served by current tools and policies?
- What does “feeling protected and supported” concretely mean in terms of SLAs, visibility, communication, and workflows during issues?

### 2.2 Hypotheses

- Unpredictable account reviews and fund holds are the single most damaging issue because they freeze operating cash without clear timelines or recourse.
- Outages and hardware connectivity issues, even if infrequent, disproportionately hurt high‑volume, time‑sensitive businesses.
- Chargeback handling feels one‑sided and opaque, leading sellers to perceive that Square “takes the customer’s side” and keeps its own fees regardless of outcome.
- Many merchants already maintain a backup payment flow and will move more volume away from Square if a more protective alternative is available.
- A targeted product that combines clear risk terms, proactive alerts, alternative payout options, and live assistance would command a premium from higher‑risk or time‑sensitive sellers.

### 2.3 Methods (how to fill gaps)

**Qualitative**

- 1:1 interviews with 20–30 sellers who have experienced: holds >7 days, more than one dispute, or outages during busy hours.
- Diary studies for 2–4 weeks with 10 sellers, tracking every friction around payouts, disputes, outages, and support contacts.

**Quantitative**

- Cohort analysis of merchants with holds, disputes, or outage exposure vs. churn and volume drop.
- In‑product surveys triggered after disputes, holds, or prolonged support response times.

**Market and competitive**

- Benchmark Stripe, PayPal, and others on dispute flows, fee refunds, communications, and premium support offerings.

---

## 3. Problem definition

### 3.1 Most common problems

From reviews, forums, and social posts, the same themes repeat:

- **Funds held / accounts frozen**
  - Complaints about funds being held or accounts canceled with little warning or recourse.
  - Sudden “under review” or deactivation with no clear explanation or path to resolution.

- **Outages and reliability**
  - Outages that shut merchants down during peak hours, sometimes described as happening “once per quarter.”
  - Reports of full‑day disruptions and significant lost revenue.

- **Disputes and chargebacks**
  - Sellers feel they “lose 100% of cases” and that there is “no real protection,” even with signed policies and documentation.
  - Confusion about why fees are kept and what support is actually provided.

- **Weak, slow, or canned support**
  - “No communication,” “support is horrible,” “stopped responding to my emails,” and no clear escalation path.
  - Long back‑and‑forth with many agents and no owner of the issue.

- **Hardware and scale friction (secondary)**
  - Hardware disconnecting mid‑payment, forcing restarts and lost sales.
  - Weak support for multi‑location reporting and large SKU catalogs (important, but secondary to money‑access issues).

### 3.2 The real pain behind these problems

- **Operational paralysis:** sellers cannot accept payments or access cash to pay staff, rent, or suppliers during outages or holds.
- **Asymmetric risk:** sellers perceive that Square always gets paid and keeps its fees, while merchants absorb chargebacks, losses, and cash‑flow shocks.
- **Emotional distrust:** language like “never again” and “greedy” reflects a collapse of trust, not just annoyance with UX.
- **Cognitive overhead:** merchants resort to backup tools, manual invoicing, or switching platforms, increasing complexity and error risk.

### 3.3 Reframed problem statement

Small businesses using Square feel that they lack control and protection over their revenue at the moments that matter most (peak sales, large transactions, disputes), due to opaque risk decisions, unreliable uptime, and weak support, forcing them to cobble together backups and eroding trust in Square as a dependable operating system for their business. The requirements in this PRD are derived directly from these observed pains and the 100‑review analysis in research/insights-summary.md.

---

## 4. Target niche and product vision

### 4.1 Underserved niche

The most exposed and vocal group share these traits:

- Small to mid‑size but volume‑sensitive businesses.
- Highly time‑bound revenue where every lost hour materially hurts sales.
- Often single‑provider or very lean teams with limited bandwidth for back‑and‑forth with support.
- Moderate to high chargeback and fraud exposure.

**Target niche for MVP:**  
“Reliability‑critical” small businesses (roughly 5–50 employees) in food & beverage and personal services that primarily use Square but frequently cite outages, account holds, and disputes as existential threats.

### 4.2 Product vision

A new product (working name): **Square Shield — a reliability and protection layer for revenue‑critical sellers.**

Square Shield gives small businesses predictable access to their money and clear support when things go wrong, combining proactive risk transparency, fail‑safe payment continuity, and priority human assistance so owners can trust that “if something breaks, I won’t be left stranded.”

---

## 5. MVP scope and rationale

The MVP should not try to fix every POS or reporting complaint. It should deliver a narrow but powerful promise: **“No surprises when it comes to your cash and uptime.”**

### 5.1 Core MVP capabilities

#### A. Transparent risk and holds dashboard

**What it does**

- Shows a clear, human‑readable explanation of why any transaction or account is under review and the expected resolution timeline.
- Provides status states (e.g., “Reviewing first large payment,” “Pattern flagged: high disputes”) and a checklist of what the seller can do now.
- Sends proactive alerts before funds are held when risk thresholds are approached (e.g., spike in ticket size or dispute rate).
- Uses AI to translate complex internal risk signals into plain‑language explanations and recommended next steps.

**Why it’s needed**

- Reviews show the worst pain is not just funds being held, but the lack of visibility or timelines, which drives panic and distrust.

---

#### B. Outage‑ready “continuity mode”

**What it does**

- Automatically enables a safe “offline but controlled” acceptance mode when connectivity or platform issues are detected, with clear limits (amount, time).
- Provides a simple continuity checklist in‑app (verify backup hotspot, alternate device, QR for online pay, etc.).
- Includes post‑incident reconciliation tools to match offline payments and notify customers if anything failed.

**Why it’s needed**

- Merchants report repeated outages and hardware disconnects that stall lines and lose peak‑hour revenue.

---

#### C. Dispute and chargeback assistant

**What it does**

- Guides sellers through a step‑by‑step dispute flow that explains likelihood of success, required evidence, and deadlines.
- Auto‑generates evidence packages from existing Square data (receipts, signatures, order history, messages).
- Provides transparent status tracking with clear messages (e.g., “Bank is reviewing,” “Evidence submitted,” “Expected decision by X.”)
- Clarifies Square’s obligations (when fees are refunded vs. not, what “fighting for you” concretely means).
- Uses AI to draft dispute narratives and summarize evidence into bank‑ready language, editable by the seller.

**Why it’s needed**

- Sellers feel alone and blindsided when chargebacks hit, often after delivering goods, and believe Square doesn’t defend them or explain the process.

---

#### D. Priority human support for critical events

**What it does**

- Surfaces a dedicated support channel (phone/chat) in‑product when an account is under review, a large portion of funds is held, or an outage is detected for that seller.
- Defines SLAs for first response and updates during investigations (e.g., response within X business hours, daily status updates).

**Why it’s needed**

- Reviews show extreme frustration with email‑only or non‑responsive support, especially when money is locked.

---

### 5.2 Explicit non‑goals for MVP

- No overhaul of core POS inventory, multi‑location reporting, or advanced SKU management (treated as separate product lines/pains).
- No guarantee of dispute outcomes controlled by banks or card networks; focus is on clarity, evidence, and expectations.
- No fully custom risk controls for merchants that would meaningfully increase fraud losses.
- No broad “all‑purpose insurance” product in v1; start with clearer policies and processes, then explore financial coverage later if validated.
- Does not replace existing Square risk policies; it improves transparency and experience around them.

---

## 6. Alternate revenue models

Given the sensitivity around fees, any monetization must clearly tie to perceived protection and uptime value.

### 6.1 Potential models

- **Tiered subscription add‑on**
  - Monthly fee for Square Shield with defined SLAs, dispute assistance, and continuity tools.
  - Higher tiers unlock faster response times and more generous offline/continuity limits.

- **Risk‑based premium**
  - Slightly higher processing fee for high‑risk categories in exchange for clearer coverage terms (e.g., dispute fee credits, faster reviews).

- **Incident‑based coverage (later phase)**
  - Optional “incident protection” where, for an added percentage, Square partially absorbs the cost of certain disputes or outages under transparent rules.

**MVP recommendation:** Start with a simple subscription add‑on for reliability‑critical segments, tested carefully on willingness to pay vs. churn risk.

---

## 7. Strategic partnerships

To close gaps quickly and avoid building everything from scratch, Square Shield can lean on partners:

- **Fraud and chargeback intelligence providers**  
  Enhance risk models and evidence recommendations with specialized dispute tools.

- **Telco / connectivity partners**  
  Offer bundled LTE backup or routers for key hardware, ensuring connectivity during local ISP outages.

- **Insurance / fintech partners**  
  Explore underwritten coverage products that help reimburse certain verified losses from fraud or outages in later phases.

These partnerships help Square improve protection and continuity without diluting focus from core POS and payments.

---

## 8. Constraints and assumptions

### 8.1 Constraints

- **Regulatory and card‑network rules:** Disputes and chargeback flows are governed by card networks and issuing banks, limiting the ability to promise outcomes.
- **Risk and fraud exposure:** More lenient holds or higher offline limits can increase fraud losses for Square and sellers.
- **Support cost structure:** Priority human support is expensive and must be scoped to high‑impact events and paying segments.

### 8.2 Assumptions

- Sellers will pay more for reliability and predictability if the value is obvious and communicated clearly.
- Transparent communication and better tools will reduce the emotional intensity of negative reviews, even when some outcomes don’t change.
- Focusing on the most reliability‑critical verticals first will yield strong product‑market fit signals before broader rollout.

---

## 9. Success metrics

### 9.1 Primary product success metrics

- Reduction in support volume and negative reviews mentioning “held funds,” “account under review,” “outage,” and “no communication.”
- Increase in retention and processing volume among Shield subscribers vs. a matched control group.
- Decrease in time‑to‑resolution for account reviews and disputes where Shield tooling is used.
- Number of merchants who successfully use continuity mode during incidents without abandoning Square.

### 9.2 User‑centric outcome metrics

- Percent of Shield users who agree with statements like “I understand what’s happening when my account is under review” and “I feel supported when something goes wrong.”
- Net sentiment (NPS/CSAT) on post‑incident surveys for outages, chargebacks, and holds.
- Drop in churn reasons citing “trust,” “outages,” “support,” or “funds held” among Shield users.

---

## 10. Summary for stakeholders

**Product:** Square Shield (Reliability & Protection Layer)  
**Vision:** Make Square the safest, most dependable way for reliability‑critical small businesses to accept payments by improving trust, uptime, and support at the moments that matter most.  
**MVP focus:** Serve a clearly underserved, reliability‑critical niche with a product that makes Square feel safe and dependable where it hurts most today, while leaving advanced POS and long‑tail scenarios for future iterations.

