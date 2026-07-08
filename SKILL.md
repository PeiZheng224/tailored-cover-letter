---
name: tailored-cover-letter
description: Generate tailored U.S.-style cover letters with company research, role-resume fit analysis, weak-match brainstorming, and polished drafting. Use when a user asks for a cover letter, application letter, company-specific application positioning, or help adapting their resume/profile to a target company and role.
---

# Tailored Cover Letter

## Core Rule

Treat this as a public, general-purpose cover letter strategy system. Do not store or include any specific user's resume, biography, private background, personal story, or private profile inside the skill itself.

Use current-invocation inputs such as a pasted resume, LinkedIn summary, project list, candidate profile, job description, networking notes, or stated preferences. Also use permitted personalization context when available under the rules below. If candidate-specific information is missing, ask for it when necessary or proceed with clearly labeled assumptions.

## Personalization Context

When available and permitted by the user and platform, use the current agent's visible user profile, memory, or saved preferences to personalize tone, framing, and recurring career positioning.

Do not assume memory exists. Do not claim to access hidden memory, prior conversations, private files, or user profile data that is not visible in the current environment.

If useful personalization context is unavailable or uncertain, ask the user to provide a resume, profile, positioning statement, preferences, or application history during the current invocation.

## Workflow

1. Intake inputs using `resources/intake_form.md`.
2. Research the company and role using `resources/company_research_framework.md`.
3. Compare the role with the candidate profile using `resources/role_resume_match_framework.md`.
4. If any match area is weak, missing, or non-obvious, use `resources/weak_match_brainstorming_framework.md`.
5. Draft the letter with `resources/cover_letter_structure.md` and `resources/output_template.md`.
6. Run `resources/quality_control_checklist.md` before finalizing.

## Required Inputs

- Target company name
- Target role title
- Job description, job posting text, or job posting link
- Candidate resume, LinkedIn summary, project list, or professional profile

## Optional Inputs

- Candidate's preferred career positioning
- Target industry or function
- Strongest experiences
- Weaker or non-obvious match areas
- Networking context, including employee conversations
- Recruiter name
- Company office address
- Target location
- Preferred tone
- Word limit
- Experiences to emphasize or avoid

## Missing Information Handling

If core information is missing, still help with the available inputs when feasible. Clearly list:

- Missing information
- Assumptions made
- What the user should verify before using the final letter

If a job posting link or company research is needed but web access is unavailable, ask the user to paste the posting or relevant company information. If proceeding without external research, state that the research brief is based only on the provided materials.

## Final Response Contract

Every invocation must return these sections:

A. Research Brief  
B. Candidate-Company Match Matrix  
C. Bridge and Expansion Ideas, only when weak, missing, or non-obvious match areas exist  
D. Final Cover Letter  
E. Customization Notes

Keep the final cover letter approximately 350-450 words unless the user requests a different length.
