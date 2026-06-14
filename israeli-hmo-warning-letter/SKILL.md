---
name: health-fund-warning-letter
description: Generates a personalized pre-litigation warning letter to Israeli HMOs (Kupot Holim) when a member has not received a specialist appointment within a reasonable time, or was denied funding for private treatment. Built on comprehensive Israeli legal research including National Health Insurance Law Section 3(d), the Shamlai Rabia precedent, State Comptroller findings 2024, and relevant insurance laws. Covers all four HMOs. Conversation in user's language (Hebrew/Arabic/Russian/English) — final letter always in Hebrew.
metadata:
  display_name: HMO Warning Letter
  display_name_he: מכתב התראה לקופת החולים
  display_description: Generate a legally grounded pre-litigation warning letter to your Israeli HMO when specialist appointment wait times are unreasonable or private treatment funding was denied.
  display_description_he: יצירת מכתב התראה משפטי מותאם אישית לקופת החולים — כשהמתנה לתור ארוכה מדי או שנסרב לך מימון טיפול פרטי.
  tags:
    - health
    - legal
    - HMO
    - patient-rights
    - warning-letter
    - insurance
    - בריאות
    - משפטי
    - קופת-חולים
    - זכויות-חולה
    - מכתב-התראה
  language: he
  supports_languages:
    - he
    - ar
    - ru
    - en
---

# SKILL: Health Fund Warning Letter (Israel)

See `SKILL_HE.md` for full Hebrew instructions and legal knowledge base.

---

## What This Skill Does

Claude conducts a short conversation with the user, collects required details, and builds a personalized legal warning letter with one goal: **receive a specialist appointment within 21 days through the public health basket, or obtain funding for private treatment when the public system failed.**

The letter is not a fixed template. It is a dynamic document Claude builds based on the user's specific situation — including only the legally relevant grounds for their case.

---

## Language

- **Conversation:** In the user's language (Hebrew / Arabic / Russian / English).
- **Final letter:** Always in Hebrew. This is the official correspondence language with Israeli HMOs.
- **Post-letter guidance:** In the user's language.

---

## Legal Basis

**Primary statute:**
Section 3(d), National Health Insurance Law 5754-1994:
> "Health services included in the health services basket shall be provided in Israel, according to medical judgment, at reasonable quality, **within a reasonable time** and at a reasonable distance from the insured's place of residence."

"Reasonable time" has never been defined in legislation, regulation, or binding precedent since 1994 — 32 years. The State Comptroller noted this in 2010 and again in 2024.

**Key precedent:**
Shamlai Rabia v. Meuhedet (Labor Court Haifa 1450/06, 28.4.2008) — established that an HMO unable to provide a service within reasonable conditions is obligated to fund private treatment.

**Key data (State Comptroller findings):**
- Rheumatology has the longest average wait time of all specialist fields, per State Comptroller reports
- 33% of lowest income quintile gave up treatment due to long wait times
- Over half of specialist referral appointments were not fulfilled
- The number of rheumatologists in Israel is low relative to population, with a high proportion nearing retirement age — a structural problem worsening over time
- HMOs show a documented pattern of not recruiting specialists in high-demand fields where those same specialists are available through the HMO's own supplemental insurance (Mushlam) plans

**Additional legal layers (when user has supplemental insurance / Mushlam plan):**
- Insurance Contract Law 5741-1981 (duty of disclosure, emphasis rule, enhanced good faith)
- Standard Contracts Law 5743-1982 (four unfair presumptions)
- Maccabi Corona class action precedent — 119 million NIS for collecting premiums without full service delivery

---

## HMO Supplemental Insurance Plan Names

- **Clalit:** Clalit Platinum / Clalit Mushlam / Clalit Meshubah
- **Maccabi:** Maccabi Gold / Maccabi Shia
- **Meuhedet:** Meuhedet Shia / Meuhedet Adif
- **Leumit:** Leumit Gold / Leumit Silver

---

## Sending Addresses

| HMO | Contact |
|---|---|
| Clalit | pniot@clalit.org.il |
| Maccabi | Form: maccabi4u.co.il/forms/public-appeal/ |
| Meuhedet | digital_team@meuhedet.co.il |
| Leumit | Form: leumit.co.il/contact-us/public-appeals/ |
| Public Complaints Commissioner (all) | gov.il/he/service/national-health-insurance-law-complaint-submission |

**Recommendation:** Send to both the HMO and the Commissioner simultaneously.

---

## Full Instructions

See `SKILL_HE.md` for complete Claude instructions including:
- Full 7-question intake questionnaire
- Complete legal knowledge base (all statutes, precedents, Comptroller findings)
- Dynamic letter construction logic per user situation
- All six letter paragraphs with conditional content
- Mandatory disclaimer language
- Post-letter guidance for users

**Note on data use:** Claude should not cite specific numbers (days, counts, percentages) that may become outdated. All factual claims should be framed as documented structural patterns based on State Comptroller findings, not point-in-time statistics.
