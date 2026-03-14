# Security Policy

## Clinical Safety First

CQAI tools are designed for **educational and reference purposes only**. They support but do not replace clinical judgment. If you identify a clinical inaccuracy that could cause patient harm, please treat it as a critical security issue and follow the process below.

## Supported Tools

All tools actively maintained under [NurseCitizenDeveloper](https://huggingface.co/NurseCitizenDeveloper) on Hugging Face Spaces receive updates. Tools marked 🔧 *In Development* may have known limitations.

## Reporting a Vulnerability or Clinical Safety Issue

### Critical Clinical Safety Issues
If you find content that could cause **direct patient harm** (e.g. dangerously incorrect drug dosages, wrong NEWS2 thresholds, unsafe clinical advice):

**Email immediately:** nursingcitizendevelopment@gmail.com
**Subject line:** `URGENT: Clinical Safety — [Tool Name]`

We aim to acknowledge within **24 hours** and resolve within **48 hours**.

### Technical Security Vulnerabilities
For technical vulnerabilities (e.g. injection attacks, data exposure, dependency exploits):

**Do not open a public GitHub issue.**

Please report privately via email:
📧 nursingcitizendevelopment@gmail.com
**Subject line:** `SECURITY: [Brief Description]`

Include:
- Tool name and URL
- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Your suggested fix (if any)

We will acknowledge within **72 hours** and aim to patch within **7 days**.

## Scope

In scope:
- All Streamlit apps deployed to Hugging Face Spaces under NurseCitizenDeveloper
- All repositories under the Clinical-Quality-Artifical-Intelligence GitHub organisation
- Clinical content accuracy in any tool

Out of scope:
- Hugging Face platform infrastructure (report to HF directly)
- GitHub platform vulnerabilities (report to GitHub directly)
- Third-party APIs used by tools (NCBI, openFDA, RxNorm, ClinicalTrials.gov)

## Clinical Safety Standards

CQAI tools are developed with reference to:
- **DCB0129** — Clinical Risk Management: its Application in the Manufacture of Health IT Systems
- **DCB0160** — Clinical Risk Management: its Application in the Deployment and Use of Health IT Systems
- **NMC Standards of Proficiency (2018)**
- **NICE Evidence Standards Framework for Digital Health Technologies**

All tools include the clinical disclaimer:
*"This tool supports but does not replace clinical judgment."*

## Responsible Disclosure

We are committed to working with security researchers and clinicians in good faith. We will not take legal action against anyone who:
- Reports vulnerabilities privately before public disclosure
- Gives us reasonable time to respond and fix
- Does not exploit vulnerabilities maliciously

Thank you for helping keep nursing students and patients safe. 💙
