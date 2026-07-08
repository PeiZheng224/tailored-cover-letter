# Tailored Cover Letter

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
Use the tailored-cover-letter skill to write a cover letter for [Company] [Role Title].

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

## Use With Codex

Clone this repository into your Codex skills directory:

```bash
mkdir -p "$HOME/.codex/skills"
git clone https://github.com/PeiZheng224/tailored-cover-letter.git "$HOME/.codex/skills/tailored-cover-letter"
```

Then invoke it in Codex by name:

```text
Use the tailored-cover-letter skill...
```

## Use With Other AI Platforms

This repository is also usable as a portable prompt pack for AI assistants that do not natively support Codex skills, including Claude, Gemini, ChatGPT, Perplexity, and other LLM tools.

### Option 1: Upload or Attach the Repository Files

If your AI platform supports file uploads or project knowledge:

1. Upload `SKILL.md`.
2. Upload the files in `resources/`.
3. Optionally upload the files in `examples/`.
4. Ask the assistant to follow `SKILL.md` as the main instruction file and use the `resources/` files as supporting references.

Use a request like:

```text
Use the attached tailored-cover-letter instructions to write a tailored U.S.-style cover letter.
Follow SKILL.md as the main workflow and use the resources files as supporting frameworks.

Company:
[Company]

Role:
[Role Title]

Job description:
[Paste job description]

Candidate profile:
[Paste resume, LinkedIn summary, project list, or professional profile]
```

### Option 2: Paste the Core Instructions

If your AI platform does not support multiple file uploads:

1. Open `SKILL.md`.
2. Paste its contents into the AI assistant.
3. Add any relevant resource files, especially:
   - `resources/intake_form.md`
   - `resources/company_research_framework.md`
   - `resources/role_resume_match_framework.md`
   - `resources/cover_letter_structure.md`
   - `resources/output_template.md`
   - `resources/quality_control_checklist.md`
4. Then paste the job description and candidate profile.

Use a request like:

```text
Follow these instructions as a reusable cover letter workflow. Use only the candidate information I provide in this chat. Do not assume access to memory, prior conversations, or personal files.

[Paste SKILL.md and relevant resource files]

Now write a tailored cover letter for:
Company: [Company]
Role: [Role Title]
Job description: [Paste JD]
Candidate profile: [Paste resume/profile]
```

### Platform Notes

- Claude Projects: add `SKILL.md` and `resources/` as project knowledge.
- Gemini: upload the files into the current chat or Gem, then ask it to follow `SKILL.md`.
- ChatGPT: upload the files in a chat or add them to a custom GPT's knowledge.
- Any text-only assistant: paste `SKILL.md` plus the most relevant resource files into the prompt.

Not every platform will preserve the folder structure or automatically load referenced files. When in doubt, paste `SKILL.md` and the relevant `resources/` files directly into the same conversation.

## Privacy Principle

This skill should never assume access to prior conversations, ChatGPT memory, personal files, hidden profile data, or private background information. If candidate-specific information is missing, it should ask for it or proceed with clearly stated assumptions.

## Repository Structure

```text
tailored-cover-letter/
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
