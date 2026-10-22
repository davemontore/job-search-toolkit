---
name: resume-reforger
description: >
  Use this skill whenever a user wants to tailor their resume to a job description. Triggers include: uploading a resume + job description, "tailor my resume", "customize my resume for this job", or any request to match a resume to a job description. This skill covers the resume only, not interview preparation. Always use this skill for US military service members or veterans pivoting into civilian tech roles — especially entry-level or junior positions in cloud application development, server and cloud administration, or cybersecurity operations. Use even if the user only mentions one of the inputs (resume or JD) — they may upload the rest next.
---

# Resume Reforger

Helps users, particularly US military service members and veterans transitioning into civilian tech careers, tailor their resume to one specific job description. It produces a list of exact wording changes the user can apply to their own file (and a Word .docx that mirrors the original format, if your environment can create files), plus a keyword gap analysis.

This skill covers the resume only. Behavioral interview preparation is a separate tool, STAR Strategizer.

### Context: Who this skill is built for

The users of this skill are often current or former US military service members pivoting into entry-level or junior roles in one of three tech tracks:
- **Cloud application development** (software engineering, DevOps, CI/CD)
- **Server and cloud administration** (infrastructure, Azure/AWS/GCP, networking)
- **Cybersecurity operations** (SOC analyst, threat detection, incident response)

Their resumes will typically already use civilianized job titles (e.g., "Operations Manager", "Logistics Specialist", "IT Systems Administrator") rather than military ranks or MOS codes. **Do not assume seniority from title.** Read the bullet content instead. Their military writing culture often leads them to understate individual ownership — using collective or passive language ("supported", "maintained", "assisted") even when they had real authority and accountability. One of the most valuable things this skill can do is surface that pattern and help them represent their actual scope of contribution more accurately.

---

## Inputs

The user should provide:
1. **Their current resume** — uploaded as a file (.docx, .pdf, or image)
2. **The job description** — uploaded as a file or pasted as text
3. **The company website URL** — optional; used for tone/culture context
4. **A background document** — optional; an About Me, a brag sheet, evaluations, or anything else that gives context the resume leaves out

If the resume or the job description is missing, ask for it before proceeding. Treat anything in the background document as the user's own information: you may draw on it when tailoring, exactly as you would the resume.

---

## Step 1: Read the Uploaded Resume

Read the full text of the resume however it reached you: an attached file, pasted text, a PDF, or an image. You need no tools or scripts for this. If you can see the file's contents, you have what you need. If the attachment came through empty or unreadable, ask the user to paste the text instead.

Note its structure as well as its words. Your changes have to fit it exactly.

Identify and note:
- Section order (e.g., Summary → Skills → Experience → Education)
- Heading styles and font choices
- Bullet point style
- Whether dates are right-aligned or inline
- Any other structural patterns

Also note anything that could keep hiring software from reading the resume correctly: two or more columns, text in tables or text boxes, content in headers or footers, icons, photos, graphics, skill bars or rating charts, unusual section headings, or a PDF whose text can't be highlighted and copied. You won't change any of this (see the format rule in Step 5). You will point it out in Step 7.

---

## Step 2: Read the Job Description

Extract the following from the JD:
- **Job title**
- **The problems the employer needs solved**: what needs fixing, building, or running that made them post this role. Read everything else in the JD through this.
- **Required skills and technologies** (hard skills, tools, languages, platforms)
- **Preferred/bonus skills**
- **Key responsibilities**
- **Soft skills and leadership language** used in the JD
- **Keywords and phrases** that appear repeatedly. These are the words a recruiter will scan for.

---

## Step 3: Analyze the Company Website (if URL provided)

If you can browse the web, open the company URL. If you can't browse, or the page fails, is behind a login, or returns no useful content, skip this step entirely and proceed with the JD only.

If successful, extract:
- Mission/values language (e.g., "customer-obsessed", "mission-driven")
- Technical identity (startup vs. enterprise, product vs. services)
- Any language that suggests cultural tone

Use this to subtly calibrate the tone of the tailored resume — not to invent content.

---

## Step 4: Assess Resume Register and Determine Target Register

Before tailoring, determine where the resume currently sits on the IC-to-leader spectrum, and what register the JD requires. This drives how bullets are reframed.

### Reading the Resume Register

Do NOT use job titles as a proxy for seniority — they've often been civilianized and may not reflect actual scope. Instead, read the bullet language.

**Individual contributor (tactical) signals:**
- Action verbs: *executed, maintained, operated, processed, tracked, coordinated, supported, assisted, performed, utilized*
- Subject is a task or system, not a team or outcome: "Maintained inventory records for 200+ items"
- No mention of scope over other people, budgets, or cross-functional work

**Leader / strategic signals:**
- Action verbs: *led, managed, directed, developed, established, oversaw, supervised, trained, advised, spearheaded*
- Scope indicators: "a team of N", "across X departments", "$Xk budget", "responsible for the performance of"
- Outcomes framed at a program or organizational level, not task level

**The military understatement pattern — watch for this carefully:**
Military writers often use collective or passive language even when they had real ownership: *"Supported the unit's mission..."*, *"Maintained readiness of..."*, *"Assisted in the coordination of..."*. A bullet like this may be hiding genuine leadership, ownership, or cross-functional impact. Flag these as candidates for perspective elevation (see Tier 2 below).

### Reading the JD Register

- **IC/junior role signals**: "you will execute", "hands-on", "individual contributor", "support the team", no mention of direct reports
- **Lead/manager role signals**: "you will lead", "manage a team", "direct reports", "strategic", "develop and mentor", "cross-functional stakeholder"
- **Ambiguous**: Many entry-level tech roles want someone who can grow — they may use both tactical and soft leadership language

### Three-Tier Perspective Handling

**Tier 1 — Register already matches, or resume is already strategic:**
If the resume's register and the JD's register are aligned, proceed with tailoring. No perspective elevation needed.

**Tier 2 — Resume reads tactical, JD has leadership indicators, AND bullets show possible hidden ownership:**
Identify bullets that are written tactically but may reflect more ownership than the language conveys. For each candidate bullet, prepare a proposed reframe. After delivering the tailored resume, present these candidates to the user in a single consolidated block (not one at a time) formatted like this:

> **Perspective Check**
> The role you're applying for values [leadership/strategic/ownership language]. Some of your bullets may undersell your actual level of responsibility. For each one below, I've suggested a reframe — but only use it if it's genuinely accurate for you. If you were just executing, keep the original.
>
> - **Original:** "Maintained training records for assigned personnel"
>   **Proposed:** "Managed training compliance tracking for assigned personnel"
>   *(Use this if you owned the process, not just entered data. If you know how many people it covered or what the completion rate was, tell me and I'll add it.)*
>
> - **Original:** "Assisted in coordinating logistics for quarterly equipment inspections"
>   **Proposed:** "Coordinated logistics for quarterly equipment inspections"
>   *(Use this if you drove the coordination, not just supported it. If you know how many sections or units were involved, tell me and I'll add it.)*

A reframe changes how ownership is described. It never adds facts. No numbers, team sizes, departments, percentages, or outcomes that are not already in the resume or the background document. If a detail like that would make the bullet stronger, ask for it (see Step 9) and add it only once the user gives it to you.

The user can then confirm which reframes are accurate and the tailored resume can be updated if needed.

**Tier 3 — Resume reads purely tactical, JD is clearly managerial, and no ownership signals exist:**
Do not attempt to elevate the register. Instead, flag this in the gap report at the end:

> "This role appears to require people management or team leadership experience. Your resume doesn't currently reflect this. If you've informally led others, trained teammates, mentored junior colleagues, or coordinated cross-functional work — even without a formal title — consider whether any of your experience could be described in those terms. If so, we can add a bullet or revise together."

### When the Resume Reads Too Senior for the Role

The opposite problem is common when senior service members apply for entry-level tech roles. If the resume shows command-level scope (leading large teams, owning budgets, directing operations) and the JD is clearly entry-level or hands-on, recruiters tend to read the gap as risk: that the person will get bored, leave when something more senior opens up, or turn down the pay.

When you see this:
- Lead each job with the hands-on and technical work the JD asks for.
- Move command-level scope lower in each job and condense it. Keep it accurate; do not delete it or make it sound smaller than it was.
- Keep official titles.
- If the resume has a summary, make it say why this role makes sense for them now, using only reasons the resume or background document gives. If none is given, ask in Step 9.
- In the gap report, tell them recruiters may question whether they will stay in a role this junior, so they should have a clear, honest answer for why they want it.

---

## Step 5: Perform the Tailoring

### What you MAY change (no user input required):
- **Rephrase existing bullets** to mirror JD language, where the underlying experience matches
- **Reorder bullet points** within a job to front-load the most JD-relevant achievements
- **Rewrite the summary/objective** to speak directly to this role and company
- **Translate military jargon** to civilian equivalents — but ONLY when the term is clearly military-specific (e.g., "MOS", "OIC", "NCO", "TDY", "OCONUS", "Battle Rhythm", "SITREP", "OPORD"). Do not translate terms civilians would understand (e.g., "logistics", "operations", "network", "team leadership")
- **Mirror JD keyword phrasing** where the skill already exists (e.g., resume says "managed a team" → JD says "people management" → use "people management"). Map keywords; don't stuff them. Use a JD keyword only where a real experience backs it, and don't chase full coverage. Resumes crammed with every phrase from the JD get fewer interviews than ones with moderate coverage.
- **De-emphasize or condense** experience clearly irrelevant to this role
- **Elevate Tier 1 register** where the resume already supports it (see Step 4)

### What you MUST NOT change:
- Do NOT add skills, tools, technologies, or certifications not present anywhere in the resume or the background document
- Do NOT invent or embellish metrics (e.g., do not add "improved efficiency by 30%" if not already stated)
- Do NOT add job responsibilities not described in the original
- Do NOT add new jobs, roles, or credentials
- Do NOT assume a skill gap is filled — if Python is required and not mentioned, do not add it
- Do NOT rewrite a tactical bullet as strategic unless it clears the Tier 2 check with the user

### How a strong bullet reads:
- **Result first, then how.** Where the resume or background document gives a result, write the bullet as: accomplished X, as measured by Y, by doing Z. Example: "Decreased duplicate tickets by 50% by writing a shared refund guide for sales and support." Where no result is given, keep the action and ask about the result in Step 9. A number alone can read as luck. If the user tells you what was going wrong before they stepped in, add it in a few words to the job's top bullet or two.
- **Specific over polished.** No stock phrases like "results-driven professional," "proven track record," or "spearheaded cross-functional initiatives to drive operational excellence." If twenty other applicants could have written the line, rewrite it from the person's actual details.
- **Defensible in an interview.** Keep only wording the user could explain naturally if asked about it. Don't use words that sound impressive but aren't backed by anything.
- **One keyword where it fits.** A bullet that repeats a keyword several times ("delivered customer support, customer service, and customer-focused communication") is stuffing. Rewrite it around what they did.
- **Show AI use; a tool name alone proves nothing.** If the JD asks for AI skills and a job on the resume shows real AI use, move that bullet to the top of the job and make it say what they used the tool for and what changed.

### Format rule:
Mirror the exact structure and layout of the uploaded resume. Do not reorganize sections, change heading styles, or alter the visual identity of the document. Only the wording changes.

---

## Step 6: Identify Gaps

Before writing, compile a list of **significant gaps** — JD requirements that do not appear anywhere in the resume and cannot be addressed through rephrasing.

Categorize gaps as:
- **Hard gaps**: Required skills/tools explicitly listed in JD that are absent from resume (e.g., "AWS certification required" — not in resume)
- **Soft gaps**: Preferred or implied skills that are absent (e.g., "experience with Agile/Scrum" — not mentioned)

If the resume and the JD barely overlap, say so plainly at the top of the gap report in Step 8: there isn't much natural overlap between their background and this role. The resume can still be as strong as their background allows, but they should apply with clear eyes.

You will surface these to the user AFTER producing the document (see Step 8).

---

## Step 7: Deliver the Tailored Resume

**Always deliver the change list in chat.** It works in every tool, and because the user pastes the changes into their own file, their formatting survives untouched.

Go section by section in the resume's own order. For every line you changed:

> **[Section / job title]**
> **Was:** "[original line, exactly as written]"
> **Now:** "[tailored line]"

Lines you did not change are not listed. Reordered bullets are shown as the new order, by their opening words. End the list with one line saying how many lines changed and in which sections.

**If your environment can create files**, also offer a Word .docx of the full tailored resume. Mirror the original's section order, heading styles, fonts, bullet style, and margins, on US Letter paper. If you cannot create files, do not mention a .docx and do not apologize for it. The change list is the deliverable.

**If Step 1 found anything software might misread, or the resume has no summary**, add a short Formatting Notes block after the change list. Name each problem and its fix: one column, conventional headings (Summary, Experience, Education, Skills), no graphics, icons, or skill bars, and saved as a PDF under 2.5 MB whose text can be highlighted and copied. If Education sits above Experience and the user is not a recent graduate, suggest putting Experience first. If there is no summary, suggest adding two or three lines at the top that connect them to this role; it is the first thing a recruiter reads, and it matters most for career changers. If they want one, draft it from what the resume and background document already say. These are for the user to make. The .docx still mirrors their original.

---

## Step 8: Produce the Keyword Analysis

After the change list, output a concise keyword analysis **in the chat** (not as a separate file). Format it like this:

---

### Keyword Analysis

**Note:** No hiring system gives your resume a universal keyword score. The software stores and searches applications, and a recruiter decides in a quick read. This shows which key terms from the JD a recruiter will find in your tailored resume.

**✅ Keywords present in tailored resume:**
- [keyword] — found in [section]
- ...

**⚠️ Keywords missing from tailored resume:**
- [keyword] — this was not in your original resume; consider adding it if you have this experience
- ...

**📋 Gaps to consider:**
These items from the JD were not in your resume. If you have relevant experience not captured in your current resume, consider adding it:
- [Hard gap 1]: [brief explanation]
- [Soft gap 1]: [brief explanation]

If the JD asks for AI skills and the resume only names tools, list that as a gap: hiring managers want to see how the person used AI to solve a problem. If they have no work example, suggest a small project aimed at this kind of role, listed in a Projects section with a link a hiring manager can open (a GitHub repo, or a shared document explaining the situation, how they used AI, and what changed).

If you don't have experience with any of the above, that's okay — this resume represents your actual background as strongly as possible for this role.

---

## Step 9: Ask What Would Make It Stronger

After the keyword analysis, ask the user up to five questions whose answers would make the resume clearer or more compelling. Five is the most, ever. Ask fewer if fewer are needed.

Ask only about things you could not work out from the resume or the background document:
- A bullet that is vague about what they did or what came of it: what changed because of it, how many, how often, for whom. Revenue is rarely the only measure: time saved, speed, scale, accuracy, error rates, and cost all count.
- A strong result with no context: what was going wrong before they stepped in
- Why they want this role, if the resume reads too senior for it (see Step 4) and nothing they gave you says why
- An AI tool the resume names without saying what they used it for or what came of it
- A gap from Step 6 they might have experience for that never made it onto the resume
- A JD keyword that sits close to their experience but that you could not honestly work in

Never ask for anything you can already read, such as names, dates, titles, or contact details. Tie each question to the bullet or gap it is about. This is a tailoring conversation, not an interview.

Ask them together, numbered, and tell the user to answer whichever they can. When they answer, give a new Was / Now list covering only the lines their answers change. Never fill in a number or detail they did not give you.

---

## Handling Edge Cases

- **Resume has no summary section**: Do not create one in the tailored resume. Only rework sections that already exist in the resume. Adding a summary would be a structural change, not a wording change. Suggest one in the Formatting Notes instead (Step 7).
- **JD is very long or vague**: Focus on the top 5–7 most repeated or bolded requirements.
- **Company website is inaccessible**: Skip Step 3 silently — do not mention this to the user unless they ask.
- **Resume is image-only (scanned PDF, photo, or screenshot)**: Read the text directly from the image if you can see it. Proceed as normal once content is read. Only if the image is unreadable, ask the user to paste the text.
- **Military service details (unit names, deployment references, etc.)**: Retain these — service history is an asset. Only translate the *function* into civilian language, not the identity.
- **Resume has no tech skills but JD requires them**: Flag clearly in gap report. Do not invent technical proficiency. Suggest the user consider whether any adjacent experience applies (e.g., "maintained network equipment" → may be relevant to a sysadmin role even without formal credentials).
- **Role is entry-level tech but resume is entirely non-technical**: This is common for career-changers. Focus the tailoring on transferable skills — reliability, attention to detail, mission focus, operating under pressure, following and creating procedures — which map well to cybersecurity ops, cloud administration, and junior dev roles. Flag the technical skill gaps honestly.

---

## Final Checklist Before Delivering

- [ ] Every change is grounded in content from the original resume
- [ ] No new skills, tools, or credentials were invented
- [ ] Military jargon translated only where clearly branch-specific
- [ ] Resume register assessed; perspective elevation handled via correct tier
- [ ] Tier 2 candidates (if any) presented to user as a consolidated Perspective Check block
- [ ] A resume that reads too senior for the role leads with hands-on work, and the gap report tells them to have a clear reason for wanting it
- [ ] Keywords mapped to real experience, not stuffed; no stock phrases the user couldn't explain in an interview
- [ ] Format mirrors the uploaded resume exactly, with Formatting Notes if software might misread it or there is no summary
- [ ] Change list delivered in chat (plus a .docx only if the environment can create files)
- [ ] Keyword analysis delivered in chat
- [ ] Gaps flagged honestly and encouragingly, with a low-overlap warning if the fit is thin
- [ ] Five questions or fewer asked to make the resume clearer or stronger

---

## Requirements

None. This file works when attached to any AI chat tool. Two optional extras are used only if the environment has them:

- Web browsing: company website research in Step 3
- File creation: the optional .docx in Step 7
