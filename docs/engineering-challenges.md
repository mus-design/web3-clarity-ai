## 🧩 Engineering Challenges & Decisions

Building Web3 Clarity AI involved more than implementing individual features. Several parts of the project required me to make architectural and product decisions based on the problems I encountered.

### Challenge 1 — Turning AI output into a measurable product

A general AI response can sound convincing without providing a consistent way to evaluate communication.

I therefore created a structured evaluation framework around six dimensions:

**Clarity · Readability · Value Proposition · Audience Fit · Trust & Credibility · Actionability**

Each dimension has a defined weight and contributes to the overall assessment.

This gave the product a repeatable structure instead of relying on an unstructured AI opinion.

**Engineering decision:**
Use a defined scoring model and structured report format around the AI output.

---

### Challenge 2 — Making the AI analysis evidence-based

Another challenge was preventing the application from producing generic statements such as:

> "Your messaging is unclear."

That kind of feedback is difficult for a user to act on.

I designed the analysis to connect findings to evidence from the submitted content.

The intended workflow became:

```text id="j8tfxr"
Original Content
      ↓
Detected Issue
      ↓
Supporting Evidence
      ↓
Why It Matters
      ↓
Recommended Improvement
```

**Engineering decision:**
Treat evidence as part of the analysis output rather than generating recommendations independently of the source content.

---

### Challenge 3 — Supporting different audiences

The same technical explanation may be appropriate for a developer but confusing for a beginner.

I therefore introduced audience context into the analysis workflow.

The system can evaluate communication for:

**Beginner · Customer · Investor · Developer**

This means the application is not only asking:

> "Is this content good?"

It is asking:

> "Is this content appropriate for this audience and this goal?"

**Engineering decision:**
Make audience and communication goal part of the analysis context.

---

### Challenge 4 — URL analysis and external content

Allowing users to analyze live websites introduced a completely different class of engineering problems.

The system has to deal with:

**URL validation → network access → content extraction → content cleanup → AI analysis**

External webpages may also contain scripts, styles, navigation elements, or other content that is not relevant to communication analysis.

This required a controlled content-processing workflow rather than sending arbitrary webpage content directly into the analysis system.

**Engineering decision:**
Treat external URLs as untrusted input and process extracted content through a controlled pipeline.

---

### Challenge 5 — SSRF and network security

URL-based analysis also introduced the risk of Server-Side Request Forgery.

A malicious URL could attempt to make the application access an internal or protected resource.

I therefore implemented URL sanitization and protections around internal destinations, including loopback and private-network targets.

**Engineering decision:**
Build security controls into the URL-processing path before external content is fetched.

This reinforced an important software engineering principle for me:

> **User-controlled network requests create a security boundary.**

---

### Challenge 6 — Persistent user data

Once I added authentication and analysis history, the product became more than a stateless AI interface.

Users needed to be able to save, revisit, search, filter, and delete their previous reports.

That required a persistent database model and user-specific access control.

I integrated Supabase and created an analysis data structure containing the information required to reconstruct previous reports.

**Engineering decision:**
Store structured analysis results in a persistent database rather than treating every AI response as temporary.

---

### Challenge 7 — Protecting user-specific data

Persistent analysis history introduced another important question:

> How does the application ensure that one user's analysis records are not accessible to another user?

I used authentication together with Supabase Row Level Security to place authorization controls at the database layer.

This means access control is not dependent only on what the frontend chooses to display.

**Engineering decision:**
Use database-level security policies as an additional authorization boundary.

---

### Challenge 8 — Building a usable analysis interface

The application can generate a large amount of information.

During testing, I received feedback that the interface could feel too text-heavy, particularly on smaller screens.

That exposed an important product lesson:

> A feature can be technically correct and still produce a poor user experience.

I therefore began treating responsive design, information hierarchy, progressive disclosure, and mobile readability as part of the engineering work.

**Engineering decision:**
Optimize the interface around the user's cognitive load, not simply the amount of information the system can generate.

---

## 📚 What These Challenges Taught Me

Working through these problems changed how I approach software development.

I learned to think about a feature across multiple layers:

```text id="v0wb8k"
User Need
    ↓
Product Workflow
    ↓
Application Architecture
    ↓
Data
    ↓
AI Behavior
    ↓
Security
    ↓
User Experience
```

A feature is not truly finished because it works in the happy path.

It also needs to be:

**Understandable · Secure · Testable · Maintainable · Useful**

That mindset became one of the most important outcomes of building Web3 Clarity AI.
