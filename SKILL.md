---
name: job-search-assistant
description: Automated job search agent for Document Controller and Procurement roles in Saudi Arabia/GCC. Searches 50+ job portals, outputs tailored ATS resumes and cover letters, generates downloadable CSV reports, and tracks application status via Gmail.
---

# Job Search Automation Protocol

## 1. Candidate Profile & Core Targets
- *Candidate Name:* Sohib Ahmad
- *Target Roles:* Document Controller, Procurement Manager, Procurement Support, Purchasing Executive
- *Primary Locations:* Saudi Arabia (Jeddah, Riyadh, Dammam) & GCC Countries (UAE, Qatar, Kuwait, Oman, Bahrain)
- *Status:* Transferable Iqama (Saudi Arabia) — Immediately Available

---

## 2. Directory of Target Portals (50 Platforms)

### Regional & GCC General Portals
- LinkedIn Jobs (https://www.linkedin.com/jobs/)
- Bayt (https://www.bayt.com/)
- Naukrigulf (https://www.naukrigulf.com/)
- GulfTalent (https://www.gulftalent.com/)
- Foundit Gulf (https://www.founditgulf.com/)
- Tanqeeb (https://saudi.tanqeeb.com/)
- Laimoon (https://www.laimoon.com/)
- Qureos (https://www.qureos.com/)

### Saudi Arabia Specific Portals
- Jadarat (https://jadarat.sa/)
- Taqat (https://www.taqat.sa/)
- Expatriates KSA (https://www.expatriates.com/cls/saudi-arabia/)
- Mihnati (https://www.mihnati.com/)
- Indeed KSA (https://sa.indeed.com/)
- GetSaudiJobs (https://getsaudijobs.com/)
- Saudi Employment (https://saudiemp.com/)
- First Access Careers (https://firstaccess.sa/)

### UAE, Qatar, Kuwait, Oman & Bahrain Portals
- Dubai Careers (https://dubaicareers.ae/)
- TAMM Abu Dhabi (https://www.tamm.abudhabi/)
- Dubizzle Jobs (https://dubizzle.com/jobs/)
- Qatar Living Jobs (https://www.qatarliving.com/jobs)
- QatarEnergy Careers (https://career.qatarenergy.qa/)
- e.gov.kw Kuwait (https://www.e.gov.kw/)
- Oman Jobs (https://www.omanjobs.om/)
- Bahrain eGov (https://www.bahrain.bh/)

### Global Aggregators
- Google Jobs (https://www.google.com/search?q=jobs+Saudi+Arabia)
- Indeed Global (https://www.indeed.com/)
- Careerjet (https://www.careerjet.com.sa/)
- Jooble (https://sa.jooble.org/)
- Talent.com (https://sa.talent.com/)
- Glassdoor (https://www.glassdoor.com/)
- SimplyHired (https://www.simplyhired.com/)

### Executive Recruitment Agencies (GCC Offices)
- Michael Page Middle East (https://www.michaelpage.ae/)
- Hays Middle East (https://www.hays.ae/)
- Robert Walters Middle East (https://www.robertwalters.ae/)
- NADIA Global (https://www.nadia-me.com/)
- Cooper Fitch (https://cooperfitch.ae/)
- Charterhouse Middle East (https://www.charterhouseme.ae/)
- TASC Outsourcing (https://tascoutsourcing.com/)
- Airswift (https://www.airswift.com/)
- NES Fircroft (https://www.nesfircroft.com/)

### Niche & Construction/Energy Boards
- Rigzone (https://www.rigzone.com/)
- Energy Jobline (https://www.energyjobline.com/)
- Oil and Gas People (https://www.oilandgaspeople.com/)
- CareerStructure (https://www.careerstructure.com/)
- GulfJobs (https://www.gulfjobs.com/)
- GCCRecruitments (https://www.gccrecruitments.com/)
- Wuzzuf (https://wuzzuf.net/)
- Akhtaboot (https://www.akhtaboot.com/)
- Arbete Careers (https://arbetecareers.com/)
- ACUC Jobs (https://acuc.jobs/)

---

## 3. Workflow Execution Steps

Whenever a search is triggered or a job posting/URL is provided:

### Step A: Match Analysis & Scoring
1. Parse requirements (systems: Aconex, EDMS, SAP, Tally; duties: POs, transmittals, vendor management).
2. Compare against master_resume.md.
3. Calculate a *Match Score (0–100%)*.

### Step B: ATS Resume & Cover Letter Generation
1. *ATS-Optimized Resume:* Generate a clean, single-column Markdown resume tailored specifically to the target role's keywords.
2. *Targeted Cover Letter:* Draft a 3-paragraph professional email/cover letter highlighting relevant GCC project experience and immediate availability (Transferable Iqama).

### Step C: Tabular Report Generation (Excel/CSV Compatible)
Output a structured CSV table ready for download and import into Microsoft Excel:
Date Found | Job Title | Company Name | Location | Match Score | Job Direct URL | Application Status | Cover Letter Snippet

---

## 4. Application Status & Gmail Tracking

When integrated with Gmail or processing email updates:
1. Automatically scan inbox for keywords: "Interview", "Application Received", "Regret", "Status", "Acknowledge".
2. Categorize status into:
   - Applied
   - Acknowledged
   - Interview Invited
   - Rejected
3. *Fallback:* If Gmail is disconnected, set status to Manual Tracking Required.

---

## 5. Nightly Automated Search Routine
- Execute automatically during off-peak hours (03:00 AM local time).
- Scan primary GCC search aggregators (Google Jobs, Expatriates, Indeed KSA) for active openings posted in the last 24 hours.
- Append all new matches, tailored resumes, and cover letters directly into the daily report CSV file

---
## 6. Activation Triggers (When to Run This Skill)
Activate this protocol immediately if the user's prompt includes any of the following intents:
- "Find job openings" or "Search jobs in Saudi / GCC"
- "Analyze this job description / URL"
- "Tailor my resume for this role"
- "Draft a cover letter / HR email"
- "Check my email for job application updates"

---

## 7. Mandatory Output Schemas

### A. CSV / Excel Report Structure
When generating tabular results, enforce this EXACT header and structure so it opens cleanly in Microsoft Excel:
```csv
"Date","Job Title","Company","Location","Match Score","Portal Name","URL","Status","Email Subject Line"
"2026-09-02","Document Controller","Al-Bawani","Riyadh, KSA","88%","Expatriates","https://...","Applied","Application: Document Controller - Sohib Ahmad
