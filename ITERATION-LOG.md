# Iteration Log — Meridian Digital Prompt Library

## Assessment 1 — Generative AI for Business



---

## 1. Purpose of This Iteration Log

This document records the development and improvement of prompts in the Meridian Digital Prompt Library.

The prompt library contains 10 documented prompts covering research and strategy, content production, client operations and reporting, and reputation/risk workflows.

The purpose of the iteration process is to show:

- what was tested;
- what problem was identified;
- what was changed in the prompt;
- why the change was made;
- what improvement was expected or observed; and
- how the version history can be demonstrated through GitHub commits.

The original prompt library states that GitHub commit/save history should be used as the version log, with each commit message explaining what changed and why.

---

## 2. Prompt Library Scope

| ID | Prompt | Workflow | Automation | Risk | Current status |
|---|---|---|---|---|---|
| P01 | Competitor research | Research & Strategy | Medium | Low | Tested |
| P02 | Audience persona synthesis | Research & Strategy | Medium | Medium | Tested |
| P03 | Creative brief generation | Research & Strategy | High | Low | Tested |
| P04 | Social captions | Content Production | High | Low | Tested |
| P05 | Paid ad A/B variants | Content Production | High | Medium | Tested |
| P06 | SEO blog brief | Content Production | Medium-High | Low | Tested |
| P07 | Email nurture sequence | Content Production | High | Medium | Tested |
| P08 | Meeting follow-up | Client Ops & Reporting | High | Low | Tested |
| P09 | Client performance reporting | Client Ops & Reporting | High | Medium | Tested |
| P10 | Crisis/reputation response | Reputation & Risk | Low-Medium | High | Tested |

---

# 3. Iteration Evidence

The source prompt library identifies the following documented iterations:

| Prompt | Version change | Main improvement |
|---|---|---|
| P02 | v1.0 → v1.2 | Added a grounding constraint after v1.0 invented demographic details that were not present in the source notes. |
| P04 | v1.0 → v1.1 | Added role framing and format constraints so the output required substantially less editing. |
| P05 | v1.0 → v1.1 | Added character limits and a testing angle to address platform-policy rejections. |
| P08 | v1.0 → v1.1 | Decomposed the task into action-item extraction followed by email drafting so important actions were less likely to be missed. |
| P09 | v1.0 → v1.1 | Added a word limit, a what/why/next-step structure, and a no-jargon rule. |
| P10 | v1.0 → v1.2 | Added format constraints and a refinement/self-check against the client tone guide. |

---

# 4. Detailed Iteration Records

## P02 — Audience Persona Synthesis

### Version 1.0

**Initial problem:**  
The initial prompt could produce demographic details that were not supported by the supplied research notes.

**Observed issue:**  
The model introduced information that was not present in the source material.

**Change made:**  
A grounding constraint was added so the model must base the persona on the supplied research rather than inventing unsupported demographic information.

### Version 1.2

**Improvement:**  
The revised prompt is more evidence-based and reduces the risk of unsupported assumptions.

**Reason for iteration:**  
To improve factual reliability and reduce hallucination/bias in audience research.

**GitHub commit message:**

`Update P02 with grounding constraint to prevent unsupported demographic details`

---

## P04 — Social Captions

### Version 1.0

**Initial problem:**  
The prompt did not provide enough role framing or formatting constraints.

**Observed issue:**  
The output required more manual rewriting and was less consistent across client accounts.

### Version 1.1

**Changes made:**

- Added role framing for the social copywriter.
- Added clear output requirements.
- Added character limits.
- Added hashtag and CTA requirements.

**Expected improvement:**  
More consistent, client-ready first drafts with less manual editing.

**GitHub commit message:**

`Improve P04 with role framing and social caption format constraints`

---

## P05 — Paid Ad A/B Testing

### Version 1.0

**Initial problem:**  
The prompt did not sufficiently constrain ad variants for the platform.

**Observed issue:**  
Some outputs created platform-policy problems and did not provide a clear testing angle.

### Version 1.1

**Changes made:**

- Added headline character limits.
- Added description character limits.
- Added a specific testing angle.
- Made the output more suitable for A/B testing.

**Expected improvement:**  
More usable ad variants and fewer platform-policy rejections.

**GitHub commit message:**

`Refine P05 with character limits and A/B testing angle`

---

## P08 — Meeting Follow-Up

### Version 1.0

**Initial problem:**  
A single drafting step could cause important action items from meeting notes to be missed.

### Version 1.1

**Change made:**  
The workflow was decomposed into two steps:

1. Extract action items, including owner and due date.
2. Draft the client follow-up email.

**Expected improvement:**  
Important actions are identified before the email is written, reducing the likelihood of omissions.

**GitHub commit message:**

`Decompose P08 into action-item extraction and follow-up email`

---

## P09 — Client Performance Reporting

### Version 1.0

**Initial problem:**  
The output could be too long, too technical, or insufficiently structured for a client audience.

### Version 1.1

**Changes made:**

- Added a 150-word limit.
- Added a clear what happened / why / next step structure.
- Added a no-jargon requirement.

**Expected improvement:**  
Shorter, clearer and more client-friendly performance summaries.

**GitHub commit message:**

`Refine P09 with word limit, client structure and no-jargon rule`

---

## P10 — Reputation/Crisis Response

### Version 1.0

**Initial problem:**  
A crisis-response prompt needs stronger controls because reputational and legal risks are high.

### Version 1.1

**Change made:**  
Format constraints were added to make the response more controlled and consistent.

### Version 1.2

**Further change:**  
A refinement/self-check step was added. The model checks its draft against the client's tone guide before returning the final response.

**Expected improvement:**  
More appropriate, empathetic and brand-consistent drafts while retaining human approval as a mandatory step.

**GitHub commit message:**

`Add self-check and format constraints to P10 crisis response`

**Important:**  
P10 is a drafting tool only. The prompt library identifies this workflow as high risk and states that it should never be automatically published.

---

# 5. GitHub Commit Plan

Use one commit for each meaningful iteration. This makes the development process easy for an assessor to follow.

Recommended commit sequence:

| Step | Suggested commit message |
|---|---|
| 1 | `Initial prompt library and README` |
| 2 | `Add initial prompt versions and workflow documentation` |
| 3 | `Update P02 with grounding constraint` |
| 4 | `Improve P04 with role framing and format constraints` |
| 5 | `Refine P05 with character limits and testing angle` |
| 6 | `Decompose P08 into action items and email drafting` |
| 7 | `Refine P09 with client reporting structure and word limit` |
| 8 | `Add format constraints and self-check to P10` |
| 9 | `Add iteration log and final documentation` |

**Do not create fake commits just to match this list.**  
If you are completing the work now, make the commits as you actually perform the corresponding changes.

---

# 6. Beginner GitHub Instructions

## Step 1 — Create a GitHub account

1. Go to GitHub.
2. Sign in or create an account.
3. Click the **+** button in the top-right corner.
4. Select **New repository**.

## Step 2 — Create the repository

Use a simple name such as:

`meridian-digital-prompt-library`

Recommended settings:

- **Visibility:** Public, if your assessment permits a public repository.
- Add a README only if you are starting a completely new repository.
- Do not add unnecessary files at this stage.

Click **Create repository**.

---

## Step 3 — Upload your existing files

Your supplied project already contains:

- `README.md`
- `Prompt-Library.md`

The README describes the folder structure and the prompt library, while the Prompt-Library document provides the workflow prompts and their risks/limitations.

On GitHub:

1. Open your repository.
2. Click **Add file**.
3. Click **Upload files**.
4. Drag your project files into the upload area.
5. Add a commit message, for example:

`Initial prompt library and documentation`

6. Click **Commit changes**.

---
