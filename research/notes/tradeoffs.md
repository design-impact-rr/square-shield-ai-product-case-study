# Square Shield – MVP Tradeoffs

This document walks through the most important tradeoffs made in the Square Shield MVP, and why they exist.

---

## 1. Focus on risk, reliability, and support vs. POS features

**Tradeoff:**  
MVP focuses on funds held, outages, disputes, and support, not broad POS or inventory improvements (multi‑location reporting, complex SKU management, advanced reporting, etc.).

**Why:**

- The core “trust in Square” problem for revenue‑critical sellers is about access to cash and uptime, not missing advanced features.  
- Too many feature axes dilute the product’s clarity and make it harder to show impact on churn, support burden, and trust.  
- POS and reporting can evolve as separate product lines; Square Shield is intentionally a focused reliability and protection layer.

---

## 2. Transparency vs. “no surprises” vs. user psychology

**Tradeoff:**  
Square Shield exposes more risk‑related information (e.g., “pattern flagged: high disputes”) but avoids overwhelming sellers with technical jargon.

**Why:**

- Sellers want to know *why* holds or reviews happen and when they can reasonably expect to be back to normal.  
- Over‑sharing or overly technical language increases anxiety and confusion.  
- The balance is: expose enough so it feels fair and explainable, but keep it human, action‑oriented, and grounded in what the seller can control.

---

## 3. Proactive holds vs. fraud risk

**Tradeoff:**  
You can raise alerts as risk thresholds are approached, but not eliminate risk‑based holds or reviews entirely.

**Why:**

- Removing holds would increase Square’s and sellers’ exposure to fraud and losses, especially in high‑risk categories.  
- Instead, the MVP chooses to make holds more predictable and transparent (clear reasons, timelines, and next steps) without changing core risk appetite.  
- This protects the business while still improving the experience for the seller.

---

## 4. AI‑assisted dispute assistant vs. outcome control

**Tradeoff:**  
Use AI to surface better evidence, draft narratives, and explain probabilities, but not to guarantee or “win” disputes.

**Why:**

- Dispute outcomes are ultimately controlled by card networks and issuing banks, not Square.  
- Promising “we’ll win your dispute” would be misleading and set wrong expectations.  
- The MVP focuses on *control and clarity* (what you can do, what to expect, and why) rather than attempting to override external actors.

---

## 5. Priority support vs. cost and scale

**Tradeoff:**  
Offer priority human support for critical money‑access and outage events, but not for every standard ticket or inquiry.

**Why:**

- Always‑on human support for every issue is not cost‑feasible at scale and would dilute the “critical‑event” signal.  
- The MVP scopes “priority” support to high‑impact events (large funds‑held, outages, complex disputes) and clearly defined SLAs, while lighter‑weight issues remain in the standard support path.  
- This keeps the product focused on the moments that matter most to revenue‑critical sellers.
