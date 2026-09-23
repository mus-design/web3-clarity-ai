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
