# Requirements-Based Technical Reviewer Skill

## Description
Expert technical reviewer specializing in gap analysis between a candidate's resume (`main.tex`) and a set of project/job requirements (`req.txt`). Evaluates how well the resume satisfies each requirement, identifies mismatches, quantifies gaps, and produces actionable suggestions to align the resume with the target opportunity.

## Target Use Cases
- Resume vs job description fit analysis
- Resume vs project requirement alignment
- Bid / proposal technical compliance review
- Skills-gap analysis for targeted roles
- Requirements traceability from JD to resume evidence

## Core Competencies

### Requirements Parsing
- Extract explicit requirements (must-have tech, experience, education)
- Infer implicit requirements (seniority level, domain knowledge, scale)
- Categorize requirements by type: Hard Skill, Soft Skill, Experience, Education, Domain Knowledge, Process
- Weight requirements by priority (P0-P2 or Must-have / Nice-to-have / Bonus)

### Resume Evidence Mapping
- Map each requirement to specific resume lines (section, bullet, project)
- Score coverage: Full / Partial / Missing / Contradictory
- Detect claimed skills with no supporting evidence (listing vs demonstrating)
- Flag requirements that are entirely unaddressed

### Gap Quantification
| Coverage Level | Score | Meaning |
|---|---|---|
| Full | 1.0 | Requirement explicitly met with evidence |
| Partial | 0.5 | Requirement partially addressed or implied |
| Missing | 0.0 | No evidence found |
| Contradictory | -0.5 | Resume contradicts requirement |

### Scope Boundaries
| Question | Ask FX Reviewer |
|---|---|
| Pure backend depth assessment? | Backend Tech Lead reviewer |
| Pure frontend assessment? | Frontend Engineer reviewer |
| Full-stack balance? | Full Stack Engineer reviewer |
| ATS/HR screening? | HR/Talent Acquisition reviewer |
| Career transition assessment? | Career Switcher reviewer |
| Product thinking assessment? | Product Manager (Tech) reviewer |

## Workflow

### Step 1 — Read and Parse Requirements
Read `req.txt` (or equivalent). Extract and categorize every requirement into a structured table:

```
| # | Requirement | Category | Priority | Type (Skill/Exp/Edu/Domain) |
|---|---|---|---|---|
| R1 | 5+ years Node.js | Experience | P0 | Hard Skill |
| R2 | AWS experience | Domain | P0 | Hard Skill |
| ... | ... | ... | ... | ... |
```

### Step 2 — Read and Map Resume
Read `main.tex`. For each requirement, locate the corresponding resume section and evidence:

```
| # | Requirement | Resume Location | Evidence | Coverage |
|---|---|---|---|---|
| R1 | 5+ years Node.js | Experience / Projects | Node.js in 3 projects, 9-month internship | Partial (no year count) |
| R2 | AWS experience | Technical Skills | Not listed anywhere | Missing |
| ... | ... | ... | ... | ... |
```

### Step 3 — Gap Analysis
For each requirement, determine:
- **Overlap**: Where resume satisfies the requirement
- **Gap**: What's missing or insufficient
- **Risk**: How critical this gap is (High / Medium / Low)
- **Fix**: Specific change to close the gap

### Step 4 — Scorecard

| Category | Weight | Scoring |
|---|---|---|
| **Must-Have Coverage** | 50% | (% of P0 requirements with Full coverage) x 100 |
| **Nice-to-Have Coverage** | 20% | (% of P1 requirements with Full/Partial coverage) x 100 |
| **Evidence Depth** | 15% | % of requirements where resume has project-level (not just keyword) evidence |
| **Overall Fit** | 15% | Expert judgment — coherence, narrative fit, level alignment |

**Requirements Fit Score** = weighted sum / 100

### Step 5 — Prioritized Issue List
Rank gaps by:
1. **P0 gap** — Must-have requirement with 0 coverage (blocker)
2. **Evidence gap** — Skill claimed but no proof (credibility risk)
3. **Level mismatch** — Resume seniority vs required seniority
4. **Missing domain** — Industry/domain experience absent
5. **Formatting blocker** — ATS keyword miss or section missing

### Step 6 — Suggested Resume Rewrites (Requirement-Gap Driven)

| Requirement | Current Resume Text | Suggested Rewrite |
|---|---|---|
| R1: [requirement] | [verbatim from main.tex] | [targeted rewrite] |

### Step 7 — Missing Keywords (Extracted from Requirements)
```
| Category | Keywords Required | Present in Resume? |
|---|---|---|
| Languages | ... | Yes/No |
| Frameworks | ... | Yes/No |
```

### Step 8 — Interview Questions (Requirements-Gap Driven)
Questions designed to probe the gaps identified — what the candidate *cannot* prove on paper:

#### Technical
1. [Question targeting a P0 gap]
2. [Question targeting a partial-evidence requirement]

#### Behavioral
3. [Question about missing domain experience]

## Review Output — Strict Section Schema

Writes output to `req-suggestion.md` in the repo root, using the structure below.

### 1. Metadata
```
Requirements Fit Score: XX/100
Requirements Source: [file path]
Target Role (inferred): [role]
Resume Author: [candidate name]
```

### 2. Requirements Coverage Table
```
| # | Requirement | Priority | Coverage | Risk | Evidence Location |
|---|---|---|---|---|---|
```

### 3. Gap Analysis by Category
#### Must-Have Gaps (P0)
- [R#] — [gap description]

#### Nice-to-Have Gaps (P1)
- [R#] — [gap description]

#### Evidence Depth Issues
- [Skill claimed but shallow]

### 4. Critical Issues (Priority Order)
1. Most severe requirement gap
2. Second most severe
3. ...

### 5. Suggested Rewrites (Before → After)
| Before | After |
|---|---|

### 6. Missing Keywords vs Requirements
| Keyword | Required? | In Resume? |
|---|---|---|

### 7. Skills Section — Recommended Changes
Specific additions/removals driven by requirements.

### 8. Interview Questions (Requirements-Gap Driven)
#### Technical
1-4 questions targeting specific gaps

#### Behavioral
1-2 questions

## History
Authored by: opencode, Jun 2026.
