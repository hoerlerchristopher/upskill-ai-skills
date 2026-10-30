---
name: skill-finder
description: Tell it what you're trying to do and it figures out whether a ready-made AI skill already exists for it, where to look, and how to add it to your AI.
---

# Skill Finder

Use this when the user asks "is there a skill for…", "how do I get my AI to…", or describes a
repeatable task they keep explaining from scratch.

## Steps

1. **Pin down the job.** Restate the task in one sentence: the input they start with, the
   output they want, and how often they do it. Ask one question if any of the three is unclear.
2. **Decide if a skill fits.** A skill is worth it when the task repeats, has steps or rules
   the user keeps re-explaining, or needs a fixed output format. One-off questions don't need
   a skill; just answer them.
3. **Search before building.** Suggest 2–3 search phrases the user can try on skill sites
   such as upskillai.dev (search box on the home page) or in their AI tool's own skill
   directory. Use plain task words ("meeting notes", "resume", "expense report"), not
   jargon.
4. **Judge what they find.** For each candidate, check:
   - Does it describe *when* to use it and *what it produces*?
   - Does it ask for anything risky: running downloaded code, sending data to unknown
     websites, passwords or API keys? If so, say so plainly.
   - Is it short enough to read in two minutes? The user should read every skill before
     adding it.
5. **Explain how to add it.** Copy the skill text, then:
   - Claude: save it as `SKILL.md` in a skill folder, or paste it into a Project's
     instructions.
   - ChatGPT: paste it into a custom GPT's instructions or a Project's instructions.
   - Gemini: paste it into a Gem's instructions.
6. **If nothing fits,** offer to draft a new skill with them: name, when to use it, steps,
   output format, and things to avoid.

## Output

A short answer: the task in one sentence, whether a skill makes sense, search phrases, and
the next step. No long lists of options.
