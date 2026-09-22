## 🔄 How It Works

Web3 Clarity AI transforms raw Web3 messaging into a structured communication assessment.

The application supports two primary input paths:

**1. Direct Text Analysis**
A user pastes messaging directly into the workspace.

**2. URL Analysis**
A user submits a publicly accessible Web3 website or documentation URL for analysis.

Both paths converge into the same analysis workflow.

### Step 1 — Define the Analysis Context

Before running an analysis, the user can specify:

* **Target audience**
* **Communication goal**
* **Content source**

The audience can be:

**Beginner · Customer · Investor · Developer**

The communication goal can be:

**Explain Clearly · Convert Visitors · Investor Messaging · Simplify Technical Docs**

This context helps the system evaluate communication according to the intended reader and purpose.

---

### Step 2 — Validate and Prepare the Input

For text analysis, the submitted content is prepared for evaluation.

For URL analysis, the application first validates and sanitizes the URL before attempting to process external content.

Security checks are applied before URL processing to reduce the risk of unsafe destinations and server-side request forgery.

The application then prepares the available page content for analysis.

---

### Step 3 — Analyze the Communication

The prepared content is evaluated against the six communication dimensions:

| Dimension               | What it examines                                                 |
| ----------------------- | ---------------------------------------------------------------- |
| **Clarity**             | How easily the main message can be understood                    |
| **Readability**         | Complexity, structure, and reading difficulty                    |
| **Value Proposition**   | Whether the value of the product is clearly communicated         |
| **Audience Fit**        | Whether the message matches the intended audience                |
| **Trust & Credibility** | Whether the communication provides reasons to believe the claims |
| **Actionability**       | Whether the reader knows what to do next                         |

Each dimension contributes to the overall assessment using the predefined weighting model.

---

### Step 4 — Generate Evidence

The system does not rely only on a final score.

The analysis identifies relevant evidence from the submitted content so the user can understand **why** a communication issue was identified.

This creates a relationship between:

**Original Content → Evidence → Diagnosis**

The evidence is used to make the report more actionable and easier for users to review.

---

### Step 5 — Produce the Analysis Report

The results are organized into a structured report containing:

* Overall communication assessment
* Individual dimension scores
* Supporting evidence
* Identified communication problems
* Areas of confusion
* Recommendations for improvement

The product also provides a **confusion heatmap** to help surface areas that may create friction for the intended audience.

---

### Step 6 — Save the Analysis

Authenticated users can save their analysis to their workspace.

The application stores the analysis data in Supabase so users can return to previous reports.

The **My Analyses** workspace allows users to:

**Search → Filter → Reopen → Review → Delete**

previous analyses.

---

## 🧠 Example User Journey

A founder launches a new Web3 protocol and wants to test the clarity of its landing page.

```text
Founder
   │
   ▼
Selects "Investor"
   │
   ▼
Selects "Investor Messaging"
   │
   ▼
Submits Web3 website URL
   │
   ▼
URL validation & security checks
   │
   ▼
Content extraction
   │
   ▼
AI communication analysis
   │
   ├── Clarity
   ├── Readability
   ├── Value Proposition
   ├── Audience Fit
   ├── Trust & Credibility
   └── Actionability
   │
   ▼
Evidence + Scores
   │
   ▼
Confusion Heatmap
   │
   ▼
Recommendations
   │
   ▼
Structured Report
   │
   ▼
Saved to My Analyses
```

## 🎯 Design Principle

The product is designed around a simple principle:

> **Don't just tell the user that their communication has a problem. Show them where the problem is, explain why it matters, and give them a path to improve it.**

This principle influenced both the AI evaluation framework and the product interface.
