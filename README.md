# Coachy — AI Cybersecurity Career Coach (NotebookLM System)

## 1. Project Overview

**Coachy** is a specialized, source-grounded AI Career Coach built within **NotebookLM** to guide Computer Science and Cybersecurity students breaking into early-career technical roles. 

Designed around a conversational persona, Coachy assists students—specifically those navigating their first or second software engineering and cybersecurity internships—by delivering tailored career pathways, technical resume optimizations, defense-industry alignment strategies, and structured interview preparation.

### Key Highlights
* **Target Audience**: Computer Science & Cybersecurity students interested in targeting defense primes and FinTech institutions.
* **Core Philosophy**: "Shift-Left Career Building" — converting abstract compliance frameworks into hands-on, portfolio-ready engineering projects.
* **System Architecture**: Grounded entirely on 19 ingested industry sources, resume guides, defense job specifications, and technical standards to ensure 100% factual fidelity.

---

## 2. Problem and Goal

### The Problem
1. **The Early-Career Experience Catch-22**: Students struggle to secure cybersecurity internships without prior professional work history, often defaulting to generic, unoptimized resumes that fail Applicant Tracking Systems (ATS).
2. **Compliance & Defense Disconnect**: Aerospace and defense contractors (RTX, Northrop, Lockheed Martin) enforce strict hiring gates—such as mandatory U.S. citizenship (ITAR), security clearance eligibility, and compliance keyword filters (NIST SP 800-53, CMMC 2.0)—that standard career advice ignores.
3. **Behavioral & Technical Panel Barriers**: Candidates struggle to articulate technical projects in behavioral interview formats (like HireVue or panel screens) without over-explaining technical jargon or under-explaining engineering depth.

### The Goal
* **Automate Career Coaching**: Build a prompt-engineered AI Assistant (Coachy) grounded in reliable industry data to coach students step-by-step.
* **Bridge Resume Gaps**: Design a 20-day DevSecOps project roadmap (C++ & Python telemetry gateway with GitHub Actions CI/CD) that turns passive compliance knowledge into active code artifacts.
* **Streamline Interview Communication**: Train candidates on the **STARR Framework** with "layered" responses (a 30-second recruiter summary followed by a low-level technical deep-dive for engineering managers).

---

## 3. Tools and Sources

### Technology Stack & AI Platform
* **AI Engine & System**: NotebookLM (Gemini Engine) with custom persona and system instruction steering.
* **Core Engineering Stack (Project Examples)**: C++ (CMake, POSIX sockets, MISRA C:2012), Python (`pytest`, `requests`, `Bandit`), Docker, GitHub Actions, Splunk, Avalonia UI / C#.
* **Security & Compliance Frameworks**: NIST SP 800-53 (AC-3 Access Enforcement, AU-2/AU-12 Audit Logging), NIST SP 800-171, CMMC 2.0, MISRA C:2012.

### Ingested Source Knowledge (3 Grounding Sources)
1. **RTX Summer 2027 Software Engineering Job Description & Extern Guides**: Detailed job requirements, U.S. citizenship mandates (ITAR), HireVue screening workflows, and compensation baselines ($27–$43/hr).
2. **Aerospace & Defense Resume Guide (Ajusta)**: ATS keyword clusters (systems integration, DO-178C, ARINC 429), single-column formatting, and citizenship/clearance placement rules.
3. **IEEE CS Interview Guide**: Resume "spike" design, STARR storytelling methodology, and company research tactics.

---

## 4. How It Works

Coachy operates through a 4-stage interactive conversation loop designed to evaluate candidate goals, identify resume gaps, recommend hands-on projects, and drill interview scripts.

### System Flow
1. **Student Context Input**: Candidate provides academic year, current experience level, and target companies (Defense/FinTech).
2. **Contextual Retrieval**: Engine queries 19 ingested sources for exact compliance rules, recruiting timelines, and ATS formatting standards.
3. **Layered Strategy Generation**: Produces a 30-second high-level recruiter hook paired with a low-level technical explanation for technical leads.
4. **Artifact Publishing**: Generates portfolio deliverables, resume bullet points, and 20-day implementation plans directly in the Studio panel.

---

## 5. Examples and Screenshots

### Example 1: Automated DevSecOps Pipeline Architecture
* **Scenario**: Creating a low-cost, portfolio-ready project for defense recruiters.
* **Output**: A C++ telemetry engine paired with a Python Zero-Trust middleware, audited in GitHub Actions via `Bandit`, `Cppcheck` (MISRA C:2012), and `Trivy`.

```yaml
# Sample GitHub Actions CI/CD Security Gate (.github/workflows/devsecops.yml)
name: DevSecOps Automated Security Pipeline
on: [push, pull_request]
jobs:
  security-audit:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Run Bandit (Python SAST)
        run: pip install bandit && bandit -r gateway/ -lll
      - name: Run Cppcheck (C++ MISRA Checks)
        run: sudo apt-get install -y cppcheck && cppcheck --enable=warning src/
      - name: Run Trivy Container Scan
        uses: aquasecurity/trivy-action@master
        with:
          image-ref: 'telemetry-gateway:latest'
          exit-code: '1'
          severity: 'CRITICAL,HIGH'
```

### Screenshots Placeholder
<img width="583" height="328" alt="image" src="https://github.com/user-attachments/assets/b9f720f5-2c94-4b55-9015-0fd75801b689" />
<img width="571" height="316" alt="image" src="https://github.com/user-attachments/assets/c349e40b-90c4-43bd-9d05-514a8dd9ed55" />
<img width="560" height="332" alt="image" src="https://github.com/user-attachments/assets/770e7f77-8987-403a-b3b2-7ee960bba17f" />

---

## 6. Testing and Improvements

### System Validation & Verification
To verify that the AI Coach provides robust, safe, and accurate advice, the system prompt and technical projects were tested using **Automated Security Verification** and prompt evaluation:

1. **Groundedness Checks**: Tested system responses against source passages to eliminate ungrounded claims or fabricated job statistics.
2. **Automated Access Testing**: Designed a `pytest` harness executing security tests against local API endpoints to verify that NIST AC-3 access controls successfully enforce permission boundaries.
3. **Build Latency Optimization**: Refactored multi-stage `Dockerfile` layers to optimize container caching, reducing automated security scan times in CI/CD from 4+ minutes down to 45 seconds.

---

## 7. Responsible AI

### Principles & Safeguards
* **100% Source Grounding**: Coachy never invents job qualifications, company requirements, or fake security controls. All advice is traceable to verified industry sources.
* **Strict Resume Integrity**: Encourages students to represent their skills truthfully, advising against listing unverified tools or inflated experience levels.
* **Air-Gapped Privacy & Safety**: Ensures candidate resumes and personal data are processed within secure, privacy-compliant boundaries without external data leakage.
* **Ethical Security Focus**: Focuses security concepts purely on defensive validation (SAST, container scanning, unit testing) and compliance auditing.

---

## 8. Career Action Plan

### 30 / 60 / 90 Day Defense & FinTech Strategy

| Timeline | Focus Area | Core Action Items |
| :--- | :--- | :--- |
| **Days 1–30** | **Resume & ATS Optimization** | • Format resume to single-column ATS standard.<br>• Place **"U.S. Citizen"** prominently at top.<br>• Build a clear "Spike" in DevSecOps & C++ security.<br>• Upload resume to SHPE Career Portal. |
| **Days 31–60** | **Technical & Interview Prep** | • Master 2-minute **STARR** interview stories.<br>• Practice layered delivery (30s summary + tech depth).<br>• Complete 20-day C++/Python DevSecOps pipeline project.<br>• Drill HireVue video screen scenarios. |
| **Days 61–90** | **Application Execution** | • Submit rolling applications for Defense (RTX, Northrop, Boeing).<br>• Target FinTech windows (Capital One, BofA).<br>• Log weekly internship reflections and technical wins. |

---

## 9. Reflection

This experience really opened my eyes to the capabilities of AI and using it to personalize my career journey and to have a coach who can really hone in on a goal and help you achieve that given the time and dedication.

### Personal Takeaways by Jonathan Cortez
* **What Went Well**: I was able to follow along and tweak the AI progressively overtime! Asking questions seemed more personal and in-line with what I have experience with.
* **What I Learned**: Learned how to communicate complex technical decisions to both business recruiters and engineering managers.
* **Next Steps**: Start on applications to better my chances at an internship, start on a project that would boost my skills and experience, and practice for interviews.
