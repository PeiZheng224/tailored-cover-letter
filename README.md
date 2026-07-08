# Tailored Cover Letter Strategist

A reusable Codex skill for generating tailored U.S.-style cover letters with company research, role-resume fit analysis, honest weak-match brainstorming, and polished drafting.

This skill is designed to be general-purpose. It does not contain any real person's resume, biography, private background, or personal profile. It uses only the candidate information provided during the current invocation.

## What It Does

- Collects the target company, role, job description, and candidate profile.
- Researches the company from credible sources when web access is available.
- Compares the job description with the candidate's resume, LinkedIn summary, project list, or professional profile.
- Produces a concise candidate-company fit matrix.
- Identifies weak or non-obvious match areas and suggests honest ways to bridge them.
- Drafts a four-paragraph U.S.-style cover letter.
- Provides customization notes before submission.

## Expected Inputs

Required:

- Target company name
- Target role title
- Job description, job posting text, or job posting link
- Candidate resume, LinkedIn summary, project list, or professional profile

Optional:

- Preferred career positioning
- Target industry or function
- Strongest experiences
- Weaker or non-obvious match areas
- Networking context
- Recruiter name
- Company office address
- Target location
- Preferred tone
- Word limit
- Experiences to emphasize or avoid

## Example Request

```text
Use the tailored-cover-letter-strategist skill to write a cover letter for [Company] [Role Title].

Here is the job description:
[Paste job description]

Here is my resume:
[Paste resume or candidate profile]

My preferred positioning is:
[Paste positioning]
```

## Output Format

Each invocation returns:

1. Research Brief
2. Candidate-Company Match Matrix
3. Bridge and Expansion Ideas, when useful
4. Final Cover Letter
5. Customization Notes

## Installation

Clone this repository into your Codex skills directory:

```bash
mkdir -p "$HOME/.codex/skills"
git clone https://github.com/PeiZheng224/tailored-cover-letter-strategist.git "$HOME/.codex/skills/tailored-cover-letter-strategist"
```

Then invoke it in Codex by name:

```text
Use the tailored-cover-letter-strategist skill...
```

## Privacy Principle

This skill should never assume access to prior conversations, ChatGPT memory, personal files, hidden profile data, or private background information. If candidate-specific information is missing, it should ask for it or proceed with clearly stated assumptions.

## Repository Structure

```text
tailored-cover-letter-strategist/
├── SKILL.md
├── resources/
│   ├── intake_form.md
│   ├── cover_letter_structure.md
│   ├── company_research_framework.md
│   ├── role_resume_match_framework.md
│   ├── weak_match_brainstorming_framework.md
│   ├── output_template.md
│   └── quality_control_checklist.md
└── examples/
    ├── sample_request.md
    └── sample_output_structure.md
```
