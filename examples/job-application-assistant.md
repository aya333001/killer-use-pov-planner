# Worked example: job application assistant

## Input

> Process: applying for jobs as a graduate student. I find a posting, read it, edit my resume to match, write a cover letter, proofread and submit. Each application takes me one to two hours, so when I'm busy I send generic versions. I'm switching from fashion communication into analytics, and the hard part is making my past experience make sense to an analytics recruiter without overstating it. I've already built a Claude skill that tailors my resume and cover letter to a posting from a bank of my experience.

## Output

### Part 1: The PoC

The PoC applies Generative AI to tailoring a job application: a job posting and a master profile go in, and a verified, tailored resume and cover letter come out in about 15 minutes instead of 1 to 2 hours (both times are estimates the PoV will measure).

**The current process**

1. Find a posting and decide whether to apply.
2. Read it for requirements, keywords and logistics.
3. Edit a general resume to match.
4. Write a cover letter, usually from an old one.
5. Proofread, export and submit.

**Where it breaks down.** Tailoring takes long enough that busy applicants send generic versions. Generic versions miss the posting's terms and get screened out. Applicants who do tailor tend to stretch the truth under time pressure. Career switchers have the hardest time, because their experience is real but written in another field's language.

**The GenAI solution**

1. **Master profile.** A one-time bank of the applicant's roles, outcomes, projects, skills and education. It is the only source of truth; the model may not invent anything.
2. **Posting analysis.** The model extracts must-haves, nice-to-haves, key terms, seniority and logistics.
3. **Fit map.** A table of each requirement, the evidence for it from the profile, and any gap.
4. **Check-in.** The applicant confirms gaps and any claim that is not yet verified.
5. **Draft.** A one-page resume with outcome-first bullets and a four-paragraph cover letter in the applicant's own voice.
6. **Verify.** Every claim is traced back to the profile, and length and format are checked.
7. **Learn.** Each correction the applicant makes is saved as a rule for the next application.

**Prototype.** Built as a Claude skill for one person's job search, delivering both documents as Google Docs. For the PoV it becomes a template: each participant loads their own master profile, and the rules stay the same.

### Part 2: Killer use

The killer use is **career-switch translation**: turning real experience from one field into the language of another without overstating it. It scored highest of four use cases against the killer-use criteria.

**Use cases and scenarios**

1. **Peak-season volume.** An MSMA student applies to 30 roles in three weeks of October recruiting. With the assistant, each application is tailored in about 15 minutes instead of being sent as a generic copy.
2. **Career-switch translation.** A fashion communication graduate applies for a pricing analyst role. The fit map recasts her presales client work as pricing and assortment analysis, flags that she has never held an analyst title, and the cover letter answers that gap with evidence instead of hiding it.
3. **Fit triage.** A student pastes ten postings before applying to any of them. The fit maps show which four have the fewest real gaps, so the time goes to those.
4. **Interview prep.** After an interview invitation, the same fit map becomes talking points: one story per requirement and an honest answer for each gap.

| Use case | Compelling | Unrecognized | Frequency | Spread | Low effort | Total (of 15) |
| --- | --- | --- | --- | --- | --- | --- |
| Career-switch translation | 3 | 3 | 2 | 3 | 3 | **14** |
| Peak-season volume | 3 | 1 | 3 | 2 | 3 | 12 |
| Fit triage | 2 | 2 | 3 | 2 | 3 | 12 |
| Interview prep | 2 | 1 | 2 | 1 | 3 | 9 |

**Why career-switch translation.** Switchers are often screened out before a person reads their application, so the need is compelling. It is also unrecognized: switchers think their problem is writing, when it is translation and honest handling of gaps, and generic chatbots tend to inflate experience rather than translate it. The result is easy to show, because a switcher can put the before and after side by side for a classmate, and most of the MSMA cohort is changing fields. Peak-season volume is the **hook** that gets people to try the tool; career-switch translation is the reason they keep using it and pass it on.

### Part 3: Proof of Value plan

A four-week randomized test with 40 MSMA students (20 per group, 200 applications in total). It checks whether the assistant produces better applications, faster, for students applying outside their previous field.

**Test question.** Among NYU SPS MSMA students applying for full-time roles outside their previous field, does the tailored application assistant, compared with their usual process, raise application quality and first-round interview rates while cutting time per application?

**Population (P).** 40 MSMA students recruited through the Management and Analytics Society and career services during the spring 2027 recruiting cycle. Each must apply to at least five roles outside their prior industry or function. Students are randomly assigned to two groups of 20, stratified by prior field and by domestic or international status so both groups match.

**Intervention (I).** 20 students build a master profile in a 30-minute setup session, then use the assistant for all five applications. They review and approve every draft before sending.

**Comparison (C).** 20 students apply to five roles in the same window using their usual process, including any general chatbot they already use, but not the assistant. They get the assistant once the test ends.

**Outcomes (O)**

- **Primary: application quality.** Two career advisers score every resume and cover letter on a 1 to 5 rubric (fit to the posting, translation of experience, accuracy, readability) without knowing which group it came from.
- **Time per application,** self-logged with a timer.
- **First-round interview invitations** per application, tracked for six weeks after submission.
- **Unsupported claims,** counted by checking each document against the student's own resume or profile.
- **Spread:** share of the intervention group who would recommend the tool, and how many classmates they refer to it.

**How differences are measured.** A baseline survey records each student's usual time per application and prior interview rate. Quality scores and time are averaged per student and compared with two-sample t-tests. Interview rates are compared with a chi-square test. With 20 per group, the test can detect a one-point difference in quality score at 80% power (assuming a standard deviation of about 1.1). 200 applications are too few to prove a change in interview rate, so that result is treated as directional.

**Expected outcomes.** Mean quality score rises from about 3.0 to 4.0. Time per application drops from about 90 minutes to 30. Interview rate roughly doubles, from about 5% to 10%. The intervention group has zero unsupported claims. At least 70% of users would recommend the tool, and at least one classmate is referred for every three users, which is the early sign that the killer use is driving adoption.
