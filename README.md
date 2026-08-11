# 📚 Prompt Library — Meridian Digital (Marketing Agency)

> **Assessment 1 | Generative AI for Business**
> Business Field: Marketing Agency — SME client services
> Model tested on: Claude
> Last updated: August 2026

---

## What This Library Does

This prompt library supports workflow automation for **Meridian Digital**, a 20-person digital marketing agency serving SME clients across retail, hospitality and professional services. It contains **10 documented, tested, and iterated prompts** organised by the business function they support.

Each prompt entry follows the same structure:
- The exact prompt text (with placeholders)
- The workflow task it supports
- The problem it solves
- Its automation potential
- Known risks and mitigations
- Version history

---

## 📂 Folder Structure

```
prompt-library/
│
├── README.md                          ← You are here (library index)
│
├── 01-research-strategy/
│   ├── README.md
│   ├── P01-competitor-research.md
│   ├── P02-audience-persona.md
│   └── P03-creative-brief.md
│
├── 02-content-production/
│   ├── README.md
│   ├── P04-social-captions.md
│   ├── P05-ad-ab-testing.md
│   ├── P06-seo-blog-brief.md
│   └── P07-email-nurture.md
│
├── 03-client-ops-reporting/
│   ├── README.md
│   ├── P08-meeting-followup.md
│   └── P09-client-reporting.md
│
└── 04-reputation-risk/
    ├── README.md
    └── P10-crisis-response.md
```

---

## 📊 Library Summary Table

| ID | Prompt Name | Workflow | Automation Level | Risk Level | Status |
|----|-------------|----------|-------------------|------------|--------|
| P01 | Competitor research | Research & Strategy | Medium | Low | ✅ Tested |
| P02 | Audience persona synthesis | Research & Strategy | Medium | Medium | ✅ Tested |
| P03 | Creative brief generation | Research & Strategy | High | Low | ✅ Tested |
| P04 | Social captions | Content Production | High | Low | ✅ Tested |
| P05 | Paid ad A/B variants | Content Production | High | Medium | ✅ Tested |
| P06 | SEO blog brief | Content Production | Medium-High | Low | ✅ Tested |
| P07 | Email nurture sequence | Content Production | High | Medium | ✅ Tested |
| P08 | Meeting follow-up | Client Ops & Reporting | High | Low | ✅ Tested |
| P09 | Client performance reporting | Client Ops & Reporting | High | Medium | ✅ Tested |
| P10 | Crisis/reputation response | Reputation & Risk | Low-Medium | High | ✅ Tested |

**Automation levels:** Very High / High / Medium / Low
**Risk levels:** High (always needs human review) / Medium (spot-check recommended) / Low (can automate with audit)

---

## 🔗 Prompt Chaining Map

```
RESEARCH → BRIEF CHAIN
P01 (Competitor research) ─┐
                            ├─► P03 (Creative brief) ─► feeds every prompt in 02-content-production
P02 (Audience persona)    ─┘

REPUTATION ESCALATION
Negative review received → P10 (Crisis response draft) → senior manager approval → published
```

---

## ⚙️ Prompting Strategies Used

| Strategy | Prompts | Why chosen |
|----------|---------|------------|
| Role framing | P04 | Consistent brand voice across multi-client accounts |
| Structured outputs | P03, P05, P06, P09 | Fixed fields/formats arrive ready to use, no reformatting |
| Constraints (limits + exclusions) | All | Keeps drafts safe, on-brief, and publish-ready |
| Decomposition | P08 | Chains "extract action items" then "draft email" in one call |
| Refinement (self-check) | P10 | Model checks its own draft against the client tone guide before returning it |
| Grounding (real data only) | P02, P09 | Reduces hallucination and bias in research/reporting outputs |

---

## 📝 Iteration Evidence

All prompt versions are documented in the individual prompt files below. Commit this repository to GitHub or OneDrive and use commit/save history as your version log — each commit message should describe what changed and why.

| Prompt | Versions | Key improvement |
|--------|----------|-----------------|
| P02 | v1.0 → v1.2 | Added grounding constraint after v1.0 invented demographic detail not in the source notes |
| P04 | v1.0 → v1.1 | Added role framing + format constraints; drafts went from a rewrite to a 2-minute edit |
| P05 | v1.0 → v1.1 | Added character limits + a testing angle; fixed platform-policy rejections |
| P08 | v1.0 → v1.1 | Decomposed into "action items, then email"; nothing gets missed |
| P09 | v1.0 → v1.1 | Added word limit + what/why/next-step structure + no-jargon rule |
| P10 | v1.0 → v1.2 | Added format constraints, then a refinement/self-check step against the tone guide |

---

## 📖 References

- CFO Dive 2025, *Deloitte AI debacle seen as wake-up call for corporate finance*, CFO Dive, 14 October, viewed 8 August 2026, <https://www.cfodive.com/news/deloitte-ai-debacle-seen-wake-up-call-corporate-finance/802674/>.
- McKinsey & Company 2023, *The economic potential of generative AI: the next productivity frontier*, McKinsey & Company, 14 June, viewed 8 August 2026, <https://www.mckinsey.com/capabilities/mckinsey-digital/our-insights/the-economic-potential-of-generative-ai-the-next-productivity-frontier>.
