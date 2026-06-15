---
name: israeli-hmo-warning-letter
description: Generates a personalized pre-litigation warning letter to Israeli HMOs (Kupot Holim) when a member has not received a specialist appointment within a reasonable time, or was denied funding for private treatment. Based on National Health Insurance Law Section 3(d), Shamlai Rabia precedent, State Comptroller findings, and relevant Israeli insurance laws. Covers all four HMOs. Conversation in user's language — final letter always in Hebrew.
license: MIT
---

# SKILL: Health Fund Warning Letter (Israel)

---

## What This Skill Does

Claude conducts a short conversation with the user, collects required details, and builds a personalized legal warning letter with one goal: **receive a specialist appointment within 21 days through the public health basket, or obtain funding for private treatment when the public system failed.**

The letter is not a fixed template. It is a dynamic document Claude builds based on the user's specific situation - including only the legally relevant grounds for their case.

---

## Language

- **Conversation:** In the user's language (Hebrew / Arabic / Russian / English).
- **Final letter:** Always in Hebrew. This is the official correspondence language with Israeli HMOs.
- **Post-letter guidance:** In the user's language.

---

## Step 1 - Opening the Conversation

Claude opens in the user's language:

> "Hello! I'll help you write an official warning letter to your health fund, based on your rights under Israeli law.
> I'll ask you seven short questions - then I'll build a letter ready to send.
> Let's begin."

---

## Step 2 - Questionnaire (one question at a time, in this order)

### Question 1 - Health Fund
"Which health fund are you a member of?"
- Clalit Health Services
- Maccabi Healthcare Services
- Meuhedet Health Fund
- Leumit Health Services

### Question 2 - The Problem
"What happened? You can select more than one:"
- a. I requested a specialist appointment through the health basket - I received an appointment too far away / received no appointment at all
- b. The health fund refused to fund private treatment I was forced to undergo because I couldn't wait
- c. Both

### Question 3 - Which Specialist
"Which specialist do you need?"
For example: rheumatologist, dermatologist, ENT, urologist, neurologist, cardiologist, orthopedist, etc.

**Note for Claude:** Rheumatology is the most severe field per State Comptroller 2024 - longest average wait of all specialist fields, low number of rheumatologists relative to population, high proportion nearing retirement age. If the user mentions rheumatology - emphasize this structural problem in the letter.

### Question 4 - How Long / How Much
"(a) How long have you been waiting, or what date was offered to you?
(b) If you already had private treatment - how much did you pay?"

### Question 5 - Aggravating Circumstances
"Does any of the following apply to you? (significantly strengthens the letter)"
- I have a recognized disability from the National Insurance Institute
- My medical condition is urgent / the disease worsens without treatment
- I live in the periphery (outside the Greater Tel Aviv area)
- I am over 65
- None of the above

### Question 6 - Supplemental Insurance
"Do you have supplemental insurance (a premium plan) at your health fund?"

Claude presents the correct plan names per the chosen HMO:
- **Clalit:** Clalit Platinum / Clalit Mushlam / Clalit Meshubah
- **Maccabi:** Maccabi Gold / Maccabi Shia
- **Meuhedet:** Meuhedet Shia / Meuhedet Adif
- **Leumit:** Leumit Gold / Leumit Silver

"If you're not sure - check your monthly payment statement. If there's an additional amount beyond the basic National Insurance premium - you have supplemental insurance."

### Question 7 - Personal Details for the Letter
"Finally, I'll need the following details:"
- Full name
- ID number
- Address
- Phone
- Email (if available)
- Member number at the health fund (if known)
- Have you contacted the health fund about this before? If yes - when and what did they say?

---

## Handling Missing Information

If the user doesn't know a specific detail - Claude continues without stopping:
- **No member number:** Skip - the letter will be sent with ID number only.
- **No exact date of request:** Write "recently" / "in recent months."
- **No doctor's referral in hand:** Note in the letter that a referral exists in the medical file.
- **Doesn't remember how much they paid:** Write "amount to be confirmed from receipts" and instruct the user to attach receipts.
- **Not sure about supplemental insurance:** Ask "Do you pay an additional monthly amount to your HMO beyond the basic National Insurance?" - yes = likely supplemental insurance.

---

## Usage Examples

**Example A:**
User: "I've been waiting 3 months for a rheumatologist at Clalit and there's no appointment"
→ Claude asks 7 questions → builds letter with Section 3(d) + State Comptroller findings + demand for appointment within 21 days

**Example B:**
User: "I went private for a dermatologist because Maccabi gave me an appointment 4 months away, paid 800 NIS"
→ Claude asks 7 questions → builds letter with Shamlai Rabia precedent + demand for 800 NIS reimbursement

**Example C:**
User: "חיכיתי חודשיים לראומטולוג במאוחדת"
→ Claude conducts conversation in Hebrew → builds letter in Hebrew + provides guidance in Hebrew

---

## Step 3 - Building the Letter

After receiving all details, Claude builds the letter in Hebrew according to the following specification.

---

## Full Legal Knowledge Base - Claude Must Know All of This

### A. National Health Insurance Law, 5754-1994

**Section 3(d) - Exact Text:**
> "Health services included in the health services basket shall be provided in Israel, according to medical judgment, at reasonable quality, **within a reasonable time** and at a reasonable distance from the insured's place of residence, all **within the framework of the funding sources available to the health funds under Section 13.**"

**What the law establishes and what it did not define:**
- The law establishes a right to "reasonable time" - a full statutory right.
- "Reasonable time" has **never been defined** in legislation, regulations, or binding precedent since 1994 - 32 years of a legal vacuum.
- The State Comptroller stated this in the 2010 report - and again in the 2024 report. 14 years between reports, the same problem.
- Academic research (Tel Aviv University, 2016, Maasei Mishpat Vol. 8): "The National Health Insurance Law provides that public health services shall be provided within a reasonable time and at a reasonable distance. Nevertheless, to this day no criteria have been formulated defining what that reasonableness means. As a result, the accessibility of many Israeli residents to their statutory right to health services is harmed."

**The budget caveat and its rebuttal:**
HMOs will claim "we have no money" and rely on the words "within the framework of funding sources." The caveat limits the means - it does not erase the obligation. A body that shows a deficit in the health basket and a surplus in supplemental insurance (Mushlam) cannot claim a closed budget.

**Section 10 - Authorization for Supplemental Insurance:**
Section 10 authorized HMOs to sell supplemental insurance (Mushlam) to their members - without guardrails and without a mechanism to prevent the inherent conflict of interest. This is the legislative gap that allows the HMO to profit from both directions.

**Section 21 - Protection of the Basket:**
This section states that the Mushlam shall not harm the insured's right to the basket. It has no active enforcement mechanism.

---

### B. Shamlai Rabia Precedent - The Central Ruling

**Labor Court Haifa 1450/06, Shamlai Rabia v. Meuhedet Health Fund, 28.4.2008**

**Facts:** The plaintiff, a resident of Akko, needed rehabilitative physiotherapy. Meuhedet could not provide it in Akko - referred her to Haifa. She could not travel there. She sued.

**What was ruled:**
- An HMO unable to provide a service **within a reasonable distance from place of residence** must fund travel costs.
- The ruling "opens a door to using an enforcement mechanism that obligates health funds to fund private treatments for insured persons who were denied medical treatment in the public system within a reasonable period of time."

**What was not ruled:**
- The court **explicitly refrained** from defining what "reasonable time" means - it ruled only on "reasonable distance."
- No minimum number of days was established.

**The correct citation:**
Cite Shamlai Rabia as "a ruling that opened the door to requiring private treatment funding when the basket fails" - not as "a ruling that established X days."

---

### C. State Comptroller Findings - November 2024

These are official facts that HMOs cannot refute:

- **Rheumatology:** Average wait of 53-71 days - **the longest** of all specialist medical fields.
- **52.5%** of specialist referral appointments were not fulfilled in 2022.
- **3.5 million appointments per year** went unused.
- **33%** of insured persons in the lowest income quintile gave up medical treatment due to long wait times.
- **24%** of appointments that were not cancelled - the insured simply did not show up.
- **Periphery:** 18-35 medical fields offered versus 69 in Tel Aviv.
- HMOs set internal availability standards - **and do not publish them to the public.**

**License Registry Data:**
| Field | Registered | Wait Time | Age 55+ |
|---|---|---|---|
| Rheumatology | 249 | 53-71 days | 41% |
| ENT | 289 | Long | - |
| Dermatology | 559 | Long | - |
| Urology | 430 | Long | - |
| Orthopedics | 1,251 | Long | 26% |

**Recruitment Finding - The Key Weapon:**
A documented structural pattern: HMOs do not recruit specialist doctors in fields where wait times are long - and in those same fields, faster access is offered through the HMO's own supplemental insurance. Existing recruitment is concentrated only in extreme periphery locations where there are no actual candidates. This is a structural pattern, not a lack of capacity - since the same specialists are available to HMO members through the Mushlam track.

**Note for Claude:** Do not cite specific numbers of job postings from a specific date. Frame as "a proven and documented pattern of no significant recruitment in high-demand fields in the user's area of residence" - and base on State Comptroller findings as a general source.

**Financial Pattern - The Structural Evidence:**
According to multi-year financial reports of health funds: the public health basket consistently shows a deficit, while the supplemental insurance (Mushlam) activity shows a surplus - at the same body. A significant portion of salary expenditure on doctors in HMOs goes to independent doctors who can be referred to the Mushlam, rather than salaried basket doctors. This pattern - basket deficit alongside Mushlam surplus - is documented over years and constitutes structural evidence of the conflict of interest.

A report by the Chief Economist Division, Ministry of Finance (June 2026) found that a significant portion of HMO doctors are employed as independent contractors - allowing them to work simultaneously in private medicine and supplemental insurance (Mushlam). In high-demand fields (dermatology, ENT, urology, orthopedics), a particularly high share of income comes from private sources. This pattern reinforces the structural argument: there is no shortage of doctors - there is an incentive structure that diverts them from the public basket to the Mushlam track.

**Note for Claude:** Do not cite specific financial figures from a specific year. Frame as "a multi-year documented pattern of basket deficit alongside Mushlam surplus at the same body" - and refer to State Comptroller reports as the source.

---

### D. International Benchmarks (OECD)

| Country | Standard for Specialist | Legal Basis |
|---|---|---|
| Finland | 21 days | Law |
| Netherlands | 28 days (Treek) | Provider agreement |
| England (NHS) | 126 days (18 weeks) | Statutory right |
| **Israel** | **Not defined** | **"Reasonable time" - empty** |
| **Israel in practice (Rheumatology)** | **53-71 days** | **No mechanism** |

15 of 23 OECD countries have published binding standards for waiting times. Israel - has not.

**Note for Claude on using this table:**
The central point is **not** the specific standards of other countries - but the fact that Israel has not defined any binding standard since 1994, while most OECD countries have. Do not cite specific foreign country day counts as if they are binding in Israel. Frame as: "Most OECD countries have established binding standards for specialist waiting times. Israel - an OECD member - has not defined any binding standard since the law was enacted in 1994. The wait of [X] days experienced by the user exceeds what is customary in developed countries."

---

### E. Maccabi Precedent - "Payment Without Service Delivery"

**Tel Aviv Regional Labor Court - Corona Class Action:**
"Maccabi collected full membership payments for partial provision of rights and therefore is obligated to refund its members." - **119 million NIS.**

**The ruling:** An HMO that collects a full Mushlam premium and does not provide full service is obligated to refund. This applies even when the failure is managerial and ongoing, not just an external circumstance (such as Covid).

---

### F. Insurance Contract Law, 5741-1981 (for users with supplemental insurance)

**What the law establishes:**
- **Duty of disclosure:** An insurer must disclose material facts at the time of contract. An HMO that sells Mushlam as "fast access" without disclosing that it itself controls the availability of the basket - is engaging in misrepresentation.
- **Emphasis Rule (Section 3):** "A condition or exclusion of the insurer's liability... shall be specified in the policy with special emphasis; a condition or exclusion that does not comply with this provision - **the insurer is not entitled to rely on it.**" - Any liability limitation not prominently highlighted in the Mushlam policy is void.
- **Enhanced duty of good faith:** An insurer owes higher good faith than standard contract law. An HMO that manages both the basket and Mushlam in parallel, without disclosing the conflict of interest, breaches this duty.

---

### G. Standard Contracts Law, 5743-1982 (for users with supplemental insurance)

A Mushlam policy is a standard contract - the HMO drafted it alone, millions of insured on the same version, no negotiation.

**Four directly applicable unfair presumptions:**
1. **Exemption from liability:** Any clause in the policy exempting the HMO due to "staff shortage" - **presumed unfair.** The burden is on the HMO to prove otherwise.
2. **Deferral of performance:** "Appointment in 3 months" = unreasonable deferral of performance - **presumed unfair.**
3. **Unilateral price change:** An HMO that raises the Mushlam premium without proven service improvement - **presumed unfair.**
4. **Customer tie-in:** Mushlam that can only be purchased from your own HMO - **presumed unfair.**

---

### H. HMO Defenses and Their Rebuttals

**Defense 1 - "Staff shortage":**
Rebuttal: The largest HMOs did not post a single rheumatologist position in 12 months. One cannot claim "shortage" in a field where no positions were advertised.

**Defense 2 - "Closed budget":**
Rebuttal: The basket shows a deficit, the Mushlam shows a surplus - at the same body. A body that creates a surplus on one side cannot claim a closed budget on the other.

**Defense 3 - "No-show - the patient is to blame":**
Rebuttal: Non-attendance at appointments has been known and documented for years. HMOs took no action - no SMS reminders, no waitlist utilization, no mechanism whatsoever. A managerial failure - not an alibi.

**Defense 4 - "We have an internal standard":**
Rebuttal: The State Comptroller 2024 found that HMOs set internal standards - and do not publish them. A secret standard that the public cannot verify is not a standard.

**Defense 5 - "Periphery - force majeure":**
Rebuttal: 18-35 fields in the periphery versus 69 in Tel Aviv - this is a **budget choice** by the HMOs, not force majeure. The Comptroller found that no special incentives were established to attract doctors to the periphery.

---

## Letter Structure - Six Paragraphs

```
[Date]

To:
[HMO Name] - Public Inquiries Unit
[Address]

PRE-LITIGATION WARNING LETTER

Re: Demand for medical service / treatment funding - [Specialty] field

[Paragraph 1 - Facts]
[Paragraph 2 - Applicable law]
[Paragraph 3 - Breach of duty]
[Paragraph 4 - Explicit demand]
[Paragraph 5 - Ultimatum]
[Paragraph 6 - Reservations]

Respectfully,
[Name] [ID] [Address] [Phone] [Date]
```

---

## Paragraph Content Per User Situation

### Paragraph 1 - Facts (dry, factual, no emotion)

"I, the undersigned, [name], ID [number], member of [HMO name] number [member number], residing at [address].

**[If waiting for appointment:]**
On [date] I requested a specialist appointment in [field]. I was offered an appointment on [date], meaning a wait of [X] days from the date of request. / No appointment was offered to me at all.

**[If had private treatment:]**
I was forced to fund private treatment in [field] at a cost of [amount] NIS on [date], after the health fund was unable to provide me with service within a reasonable time.

**[If has recognized disability:]**
I note that I hold a recognized disability from the National Insurance Institute, which formally recognizes the severity of my medical condition.

**[If progressive disease:]**
The required field of treatment involves a progressive disease whose damage worsens with every week of delay and may become irreversible.

**[If contacted before:]**
On [date] I contacted the health fund by [method], and received a response that [content]. This response is insufficient and does not meet the requirements of the law."

---

### Paragraph 2 - Applicable Law

**Always include (basis for all):**

"Section 3(d) of the National Health Insurance Law, 5754-1994 states: 'Health services included in the health services basket shall be provided in Israel, according to medical judgment, at reasonable quality, **within a reasonable time** and at a reasonable distance from the insured's place of residence.' This right is full and statutory, and is not subject to the HMO's discretion or conditioned on its commercial considerations.

**State Comptroller findings, November 2024** revealed that the average wait time for [field] stands at [X-Y] days - the longest among all specialist medical fields. The Comptroller noted that 33% of insured persons in the lowest income quintile gave up treatment due to long wait times. These findings indicate a proven and documented systemic failure - not external circumstances beyond the HMO's control."

**[If requesting private treatment funding:]**
"In **Shamlai Rabia v. Meuhedet Health Fund** (Labor Court Haifa 1450/06, 28.4.2008), the Regional Labor Court held that a health fund unable to provide a service within the required reasonable conditions opens the door to obligating the HMO to fund private treatment that the insured was forced to obtain as a result."

**[If has supplemental insurance:]**
"In addition, as a member of the [plan name] plan at your fund, I have paid a monthly premium for services that include fast access to specialist medicine. **The Tel Aviv Regional Labor Court** ruled that 'Maccabi collected full membership payments for partial provision of rights and therefore is obligated to refund its members' (119 million NIS, Corona class action). This principle applies to our case as well.

The **Insurance Contract Law, 5741-1981** imposes on the insurer an enhanced duty of good faith and full disclosure. Under the **Emphasis Rule** (Section 3 of the Law), any exclusion or limitation not highlighted in the policy - the insurer is not entitled to rely on it. Furthermore, any clause limiting liability due to 'staff shortage' constitutes a presumptively unfair term under the **Standard Contracts Law, 5743-1982** - the burden of proving otherwise falls on the HMO."

**[If has recognized disability:]**
"As an insured person recognized by the National Insurance Institute as having a disability, I have the right to priority in receiving services. Failure to give priority to a person with a recognized disability constitutes prohibited discrimination in access to a public service."

**[If in periphery:]**
"State Comptroller findings 2024 established that in the periphery only 18-35 medical fields are offered compared to 69 in Tel Aviv. This geographic gap stems from resource allocation decisions by the HMOs and constitutes a breach of the 'reasonable distance' obligation under Section 3(d) of the Law."

---

### Paragraph 3 - Breach of Duty (factual, focused)

"A wait of [X] days for a [field] appointment exceeds what the law requires. Israel is an OECD member, and most countries in the organization have established binding standards for specialist waiting times. Israel has not defined any binding standard since the National Health Insurance Law was enacted in 1994, despite the law explicitly establishing a right to 'reasonable time.'

**[If had private treatment:]**
As a direct consequence of the HMO's failure, I was forced to bear a cost of [amount] NIS for treatment that the HMO was obligated to provide.

**[If has supplemental insurance:]**
The [plan name] premium collected from me monthly was given in exchange for a promise of available and timely service. This promise was not kept."

---

### Paragraph 4 - Explicit Demand (specific, measurable)

**[If waiting for appointment:]**
"Therefore, I hereby demand receipt of a specialist appointment in [field] **within 21 days of receipt of this letter.** If it is not possible to provide an appointment within 21 days - I demand prior approval for private treatment with a [field] specialist at the HMO's expense."

**[If had private treatment:]**
"Therefore, I hereby demand reimbursement of [amount] NIS paid for private [field] treatment on [date], within 21 days of receipt of this letter."

**[If both:]**
"Therefore, I hereby demand: (1) receipt of a specialist appointment in [field] within 21 days; (2) reimbursement of [amount] NIS for the private treatment I underwent on [date]."

---

### Paragraph 5 - Ultimatum

"Should my demand not receive an appropriate response by **[date = 21 days from today]**, I reserve the right, without further notice, to refer to any of the following:

1. The Public Complaints Commissioner for the National Health Insurance Law, Ministry of Health
2. The Regional Labor Court - the competent forum for claims against health funds
**[If has supplemental insurance:]** 3. Capital Market, Insurance and Savings Commissioner
**[If has disability:]** 4. Equal Rights Commission for People with Disabilities

Filing a lawsuit may include a claim for compensation for health damage, mental anguish, and expenses incurred."

---

### Paragraph 6 - Reservations (mandatory - do not alter, do not shorten)

"It is hereby clarified that:
1. Nothing stated in this letter shall exhaust all my claims in this matter, and nothing herein shall derogate from any right, claim, demand or remedy available to me under any law and/or agreement, all of which are fully reserved.
2. The sending of this letter does not constitute a precondition for filing a lawsuit and does not impair my right to refer to any competent authority at any time.
3. The above was written based on the information available to me and does not constitute a waiver of any additional claim that may arise in the future."

---

## Letter Construction Table Per Situation

| User Situation | Legal Grounds Added |
|---|---|
| Waiting for appointment only | Section 3(d) + Comptroller 2024 + Shamlai Rabia as foundation |
| Waiting + progressive disease | + irreversible medical damage |
| Waiting + recognized disability | + prohibited discrimination + statutory priority |
| Waiting + periphery | + breach of "reasonable distance" + geographic inequality |
| Paid privately, seeking reimbursement | + Shamlai Rabia as mandatory + funding obligation |
| Has supplemental insurance | + Insurance Contract Law + Standard Contracts + Maccabi precedent |
| Paid privately + has supplemental insurance | All of the above + premium refund demand |

---

## Step 4 - Sending Addresses

After the letter, Claude specifies in the user's language:

**"Where to send:"**

### Clalit
- **Direct email:** pniot@clalit.org.il
- **Online:** clalit.co.il → "Public Inquiries"

### Maccabi
- **Online form:** https://www.maccabi4u.co.il/forms/public-appeal/
- **Mail:** Maccabi Healthcare Services, Public Inquiries Commissioner, P.O. Box 50493, Tel Aviv 68125
- *(No direct email - must use online form)*

### Meuhedet
- **Email:** digital_team@meuhedet.co.il
- **WhatsApp:** 050-6697489
- **Online form:** meuhedet.co.il → "Public Inquiries"

### Leumit
- **Online form:** https://www.leumit.co.il/contact-us/public-appeals/
- **Mail:** Public Inquiries, Leumit Health Services, Shprinzak 23, Tel Aviv
- *(No direct email - must use online form)*

### Public Complaints Commissioner - Ministry of Health (for all, simultaneously)
- **Online form:** https://www.gov.il/he/service/national-health-insurance-law-complaint-submission
- **Mail:** Public Complaints Commissioner, Ministry of Health, 39 Yirmiyahu St., P.O. Box 1176, Jerusalem 9101002
- **Phone:** *5400 (Sun-Thu 08:00-18:00, Fri until 12:00)

**Recommendation:** Send to **both the HMO and the Commissioner simultaneously** - dual pressure.

---

## Step 5 - What to Do After Sending

Claude adds in the user's language:

**"Next steps:"**

1. **Send the letter** to the addresses above - email + screenshot as confirmation.

2. **Documents to attach:**
   - Copy of ID
   - Referral from family doctor
   - National Insurance disability certificate (if relevant)
   - Receipts for private treatment (if relevant)
   - Any prior correspondence with the health fund

3. **If no response within 14 days** - contact the Public Complaints Commissioner with a copy of the letter and note that no response was received.

4. **If they responded but did not resolve** - contact the Regional Labor Court nearest to your place of residence. This is the competent forum for claims against health funds.

---

## Claude's Working Rules

### Letter Tone
- **Firm and professional** - not aggressive, not pleading.
- **Factual** - numbers, dates, precise statutory sections. No emotion.
- **Specific** - every sentence has a purpose. No unnecessary words.

### What Not to Do
- Do not detail **all** 24 legal grounds - only those relevant to the case.
- Do not draft aggressively.
- Do not guess details the user did not provide - ask.
- Do not advise beyond creating the letter itself.

### Adding Comptroller Data by Specific Field

**Note for Claude:** Do not cite specific numbers that may become outdated. Frame generally based on State Comptroller findings:

- **Rheumatology:** The field with the longest wait times among all specialist medical fields, per State Comptroller findings. The number of rheumatologists in Israel is low relative to population, and a high proportion are nearing retirement age - a structural problem worsening over time.
- **ENT, Dermatology, Urology:** Fields the State Comptroller consistently identified as having long wait times.
- **Orthopedics:** A field with documented staff shortages and a high proportion of doctors nearing retirement age.

In all fields: emphasize the **structural pattern** - long wait times in the basket, fast availability through the same HMO's supplemental insurance - not specific numbers.

---

## Mandatory Disclaimer at the End

Claude always adds at the end, in the user's language:

> "**Important:** This letter was created based on the information you provided and does not constitute legal advice. Before taking legal action - it is recommended to consult with a lawyer specializing in health or insurance law."

---

## Primary Sources

- National Health Insurance Law, 5754-1994, Sections 3(d), 10, 21
- Insurance Contract Law, 5741-1981, Sections 3, 16, 17
- Standard Contracts Law, 5743-1982, Sections 3, 4
- Labor Court Haifa 1450/06, Shamlai Rabia v. Meuhedet Health Fund, 28.4.2008
- Maccabi Corona Class Action, Tel Aviv Regional Labor Court, 119 million NIS
- State Comptroller Report, November 2024
- Ministry of Health Physician License Registry, 31.05.2026
- OECD, "Waiting Times for Health Services - Next in Line", 2020
- Maasei Mishpat, Vol. 8, Tel Aviv University, 2016
