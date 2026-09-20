# Web3 Clarity AI

### AI-powered communication intelligence for Web3 products

Web3 Clarity AI helps Web3 founders, product teams, developers, and innovators understand how clearly their products communicate with different audiences.

It analyzes Web3 messaging across six dimensions:

**Clarity · Readability · Value Proposition · Audience Fit · Trust & Credibility · Actionability**

The goal is simple:

> **Turn technical complexity into communication people can understand, trust, and act on.**

---

## 🚀 Project Overview

Web3 products can be technically sophisticated while their messaging remains difficult for users, customers, investors, and developers to understand.

I built Web3 Clarity AI to explore how artificial intelligence can be used not just to rewrite content, but to **diagnose communication problems, provide evidence from the original content, and generate actionable recommendations.**

The application supports both **direct text analysis** and **URL-based analysis** of Web3 websites and documentation.

### Core capabilities

* AI-powered communication analysis
* Six-dimension scoring framework
* Audience-specific analysis
* Goal-specific analysis
* Evidence-based recommendations
* Confusion heatmap
* Web3 website/URL analysis
* Authentication and persistent analysis history
* Supabase database integration
* Row Level Security
* URL validation and SSRF protection

---

## 🎯 The Problem

Web3 communication often contains technical language that creates a gap between the people building a product and the people trying to understand it.

A visitor may encounter complex terminology without immediately understanding:

**What does this product do?**
**Who is it for?**
**Why does it matter?**
**Why should I trust it?**
**What should I do next?**

Web3 Clarity AI was created to make these communication problems measurable and easier to improve.

---

## 💡 The Solution

Web3 Clarity AI evaluates communication through a structured workflow:

**Content → Context → AI Analysis → Evidence → Scoring → Recommendations**

The user provides content, selects the intended audience and communication goal, and receives a structured diagnostic report.

Rather than treating AI as a black-box writing tool, the application is designed to make the reasoning behind the analysis more visible through evidence and clearly defined evaluation dimensions.



## 🏗️ Architecture

Web3 Clarity AI follows a full-stack architecture designed to separate the user interface, application logic, AI analysis, and persistent data.

```text
                         ┌──────────────────────┐
                         │      User Input      │
                         │                      │
                         │  • Text              │
                         │  • Web3 URL          │
                         │  • Audience          │
                         │  • Goal               │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │   Content Processing │
                         │                      │
                         │ URL validation       │
                         │ Content extraction   │
                         │ Input preparation    │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │     AI Analysis      │
                         │                      │
                         │ 6 evaluation         │
                         │ dimensions           │
                         │                      │
                         │ Audience context     │
                         │ Goal context         │
                         └──────────┬───────────┘
                                    │
                                    ▼
                  ┌─────────────────┴─────────────────┐
                  │                                   │
                  ▼                                   ▼
        ┌─────────────────────┐             ┌─────────────────────┐
        │ Evidence & Scores   │             │ Recommendations     │
        │                     │             │                     │
        │ • Dimension scores  │             │ • Problems          │
        │ • Supporting text   │             │ • Improvements      │
        │ • Heatmap evidence  │             │ • Actionable advice │
        └──────────┬──────────┘             └──────────┬──────────┘
                   │                                   │
                   └─────────────────┬─────────────────┘
                                     │
                                     ▼
                         ┌──────────────────────┐
                         │    Analysis Report   │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │       Supabase       │
                         │                      │
                         │ Authentication       │
                         │ Database             │
                         │ Row Level Security   │
                         │ Analysis history     │
                         └──────────────────────┘
```

### Analysis Model

The communication analysis is based on six weighted dimensions:

| Dimension           | Weight |
| ------------------- | -----: |
| Clarity             |    20% |
| Readability         |    15% |
| Value Proposition   |    20% |
| Audience Fit        |    15% |
| Trust & Credibility |    15% |
| Actionability       |    15% |

The weighted dimensions are used to produce an overall communication assessment while preserving the individual dimension scores for deeper analysis.

---

## 🛠️ Technology Stack

### Frontend

**React** — component-based user interface
**TypeScript** — type-safe application development
**Material Design 3 principles** — interface and interaction design

### AI

**Google Gemini** — generative AI analysis and structured communication assessment

The AI layer is used to evaluate submitted content against the application's defined dimensions, audience context, and communication goals.

### Backend & Data

**Supabase** — authentication, PostgreSQL database, and persistent application data

**Row Level Security (RLS)** — database-level access control for user-associated analysis records

### Security

**URL sanitization and validation** — validates external URLs before processing

**SSRF protections** — helps prevent requests to loopback and internal network resources

### Product Features

* Direct text analysis
* Live word and character counts
* Estimated reading time
* Web3 URL analysis
* Audience profiles
* Communication goal selection
* Six-dimension scoring
* Evidence-based analysis
* Confusion heatmap
* AI recommendations
* Analysis history
* Search and filtering
* Authentication
