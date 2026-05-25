# Contributing to Clinical Quality Artificial Intelligence

Thank you for your interest in contributing to CQAI. We welcome contributions from nurses, nursing students, healthcare educators, clinical specialists, and developers at all levels of experience — **no computer science degree required**.

> 💙 *"Every nurse has expertise that can improve these tools. Your clinical knowledge is as valuable as any code."*

---

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Ways to Contribute](#ways-to-contribute)
- [Clinical Accuracy Standards](#clinical-accuracy-standards-mandatory)
- [Development Setup](#development-setup)
- [Commit & Branch Conventions](#commit--branch-conventions)
- [Pull Request Process](#pull-request-process)
- [Reporting Issues](#reporting-issues)
- [Clinical Safety Escalation](#clinical-safety-escalation)

---

## Code of Conduct

All contributors must follow our [Code of Conduct](CODE_OF_CONDUCT.md). We are committed to a welcoming, inclusive environment — especially for nursing and healthcare professionals who may be new to open-source development.

---

## Ways to Contribute

### 🩺 No Coding Required
- **Review clinical content** — check drug dosages, NEWS2 thresholds, assessment scale criteria against current UK guidelines (BNF, NICE, RCP)
- **Write or improve questions** — contribute NCLEX or NMC CBT practice questions with rationales and source citations
- **Test tools as a user** — try tools on desktop and mobile, report anything unexpected
- **Improve documentation** — fix typos, improve clarity, add missing clinical context
- **Suggest new tools** — open a [Feature Request](https://github.com/Clinical-Quality-Artifical-Intelligence/.github/issues/new?template=feature_request.md)

### 💻 Technical Contributions
- **Fix bugs** — pick up a [`good first issue`](https://github.com/issues?q=is%3Aopen+is%3Aissue+org%3AClinical-Quality-Artifical-Intelligence+label%3A%22good+first+issue%22) label
- **Improve UI/UX** — Streamlit layout, accessibility improvements, mobile responsiveness
- **Add features** — implement requests from the issues list
- **Improve CI/CD** — GitHub Actions, automated testing, deployment pipelines
- **FHIR / interoperability** — contribute to the [Open Nursing Core IG](https://github.com/Clinical-Quality-Artifical-Intelligence/open-nursing-core-ig)

---

## Clinical Accuracy Standards (Mandatory)

Any contribution that touches clinical content **must** meet these standards:

1. **Source everything.** All clinical information must be traceable to a primary source:
   - British National Formulary (BNF) — current edition
   - NICE guidelines (specify guideline number, e.g. NG50)
   - NMC Standards of Proficiency for Registered Nurses (2018)
   - RCP NEWS2 (2017)
   - BAPEN MUST (2003, reviewed)
   - Other peer-reviewed UK clinical guidance

2. **Include the disclaimer.** Every tool and page that presents clinical information must include:
   > *"This tool supports but does not replace clinical judgment. Always follow your organisation's policies and current clinical guidelines."*

3. **No absolute recommendations.** Do not present clinical guidance as absolute fact without appropriate caveats (e.g. patient-specific factors, local protocol variation).

4. **Flag uncertainty.** If you are unsure about the clinical accuracy of content you're changing, open the PR as a draft and request clinical review.

5. **Critical safety check.** If a change affects drug dosages, NEWS2 scoring, assessment scale criteria, or anything that could directly affect patient care — ensure it has been reviewed by a registered healthcare professional before merging.

---

## Development Setup

Most CQAI tools are Python/Streamlit applications. For TypeScript projects, see the individual repository README.

### Prerequisites
- Python 3.10+ ([download](https://python.org))
- `git` ([download](https://git-scm.com))
- A code editor (VS Code recommended)

### Steps

```bash
# 1. Fork the repository on GitHub, then clone your fork
git clone https://github.com/YOUR-USERNAME/REPO-NAME.git
cd REPO-NAME

# 2. Create a virtual environment
python -m venv .venv
source .venv/bin/activate      # macOS/Linux
.venv\Scripts\activate         # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the app locally
streamlit run app.py
```

The app will open at `http://localhost:8501`.

### TypeScript / Node.js Projects
```bash
npm install
npm run dev     # or npm start
```

---

## Commit & Branch Conventions

### Branch Naming
```
feat/short-description        # new feature
fix/short-description         # bug fix
clinical/short-description    # clinical content update
docs/short-description        # documentation only
refactor/short-description    # code quality, no behaviour change
```

### Commit Messages
Use [Conventional Commits](https://www.conventionalcommits.org/):
```
feat: add Abbey Pain Scale to assessment hub
fix: correct NEWS2 SpO2 Scale 2 threshold for COPD patients
clinical: update metformin dosage to BNF 2024 edition
docs: add ORCID to CITATION.cff
```

For clinical content changes, include your source in the commit body:
```
clinical: correct NEWS2 respiratory rate scoring

Threshold corrected from ≥25 to ≥25 breaths/min (Score 3).
Source: RCP National Early Warning Score (NEWS) 2, 2017, p.12.
```

---

## Pull Request Process

1. **Open a draft PR early** — this allows discussion before you invest significant time
2. **Fill in the PR template** completely — the clinical accuracy checklist is mandatory for clinical content changes
3. **Link the related issue** using `Closes #123` in the PR description
4. **Include screenshots** for any UI changes
5. **Test on Hugging Face Spaces** for production tools where possible
6. **Request review** — tag `@ClinyQAi` for clinical content review, or any contributor for technical review
7. **Respond to feedback** — we aim to review PRs within 7 days

### Merging Criteria
- All checklist items completed
- No unresolved review comments
- Clinical content reviewed by a registered nurse or healthcare professional (for clinical PRs)
- Tests pass (where applicable)
- No new Python errors or warnings in the Streamlit terminal

---

## Reporting Issues

Use the appropriate issue template:

| Issue Type | Template | Use For |
|---|---|---|
| 🐛 Bug Report | [`bug_report.md`](ISSUE_TEMPLATE/bug_report.md) | Unexpected app behaviour, errors, crashes |
| ⚠️ Clinical Inaccuracy | [`clinical_inaccuracy.md`](ISSUE_TEMPLATE/clinical_inaccuracy.md) | Wrong drug doses, incorrect clinical thresholds, outdated guidelines |
| 💡 Feature Request | [`feature_request.md`](ISSUE_TEMPLATE/feature_request.md) | New tools, new features, improvements |

---

## Clinical Safety Escalation

If you discover content that could **cause direct patient harm** (e.g. dangerously incorrect drug dosages, wrong emergency thresholds):

**Do not wait.** Email immediately:

📧 **nursingcitizendevelopment@gmail.com**
Subject: `URGENT: Clinical Safety — [Tool Name]`

We aim to acknowledge within **24 hours** and resolve within **48 hours**.

See our full [Security Policy](SECURITY.md) for the complete responsible disclosure process.

---

## Questions?

Open a [Discussion](https://github.com/orgs/Clinical-Quality-Artifical-Intelligence/discussions) or email [nursingcitizendevelopment@gmail.com](mailto:nursingcitizendevelopment@gmail.com).

We especially encourage questions from nurses who are new to open source — your clinical expertise is what makes these tools trustworthy.

---

*Thank you for helping make evidence-based digital tools available to every nurse. 💙*
