# AI Study Helper — FlyRank Capstone

A Claude-powered study assistant that helps with any subject, plus a personal portfolio site showcasing the build.

## What it does

The AI Study Helper is a custom Claude Project built for general-purpose academic support. It's set up with custom instructions so that instead of just giving direct answers, it helps you actually understand the material — explaining concepts, breaking down problems step by step, and helping with writing and revision across any subject (not locked to one topic).

Alongside it, I built and published a personal portfolio site that documents the project and the process behind it.

Who it's for: Students who want a study partner that adapts to whatever subject they're working on that day, rather than a single-subject tutor tool.

## Setup — how to use it

1. Go to claude.ai and log in (or create a free account).
2. Open Projects in the sidebar and create a new Project.
3. Paste in the custom instructions below (or your own version) into the Project's "Custom Instructions" field.
4. Start a new chat inside that Project — it will now follow the study-helper behavior automatically, no need to re-explain the setup each time.

Custom instructions used (example):

"You are a study assistant. When I ask you something, don't just give me the final answer — walk me through the reasoning or the concept first, check my understanding, and then confirm the answer. Adapt to whatever subject I bring you. If I ask for essay/writing help, give feedback and suggest improvements rather than rewriting the whole thing for me."

A stranger can reproduce this in under 5 minutes — no code, no API key, no installation required.

## Usage example

Prompt: "Can you help me understand photosynthesis for my bio test?"
Response behavior: Instead of a dumped definition, it breaks the process into stages, checks if I know the inputs/outputs, and quizzes me briefly before summarizing.

Prompt: "Can you review this paragraph of my essay?"
Response behavior: Gives specific line-level feedback on clarity and argument structure instead of rewriting it wholesale.

## Architecture (simple sketch)

Student types question into Claude Project (custom instructions applied) → Claude interprets subject + intent → responds with guided explanation / feedback (not just raw answer) → Portfolio site documents the build, links to demo + README.

No backend, no database — this runs entirely on Claude.ai's Project feature. The portfolio site is a static site hosted on the FlyRank domain, linking back to this README and the demo video.

## Eval results (v2)

- Tested with ~15 sample questions across 4 subjects (math, biology, history, English writing).
- Correctly adapted tone/approach in 13/15 cases without being told the subject explicitly.
- Writing feedback mode stayed consistent (gave feedback, didn't rewrite) in all test cases.
- 2 cases where it slipped into giving a direct answer instead of guiding — noted as a limitation below.

## Limitations

- Not subject-specialized: since it's general-purpose, it doesn't go as deep as a subject-specific tutor tool would for advanced/niche topics.
- Inconsistent guided-mode adherence: in a couple of test cases it gave the direct answer instead of walking through the concept first — the custom instructions aren't 100% reliable at holding the behavior.
- No memory across separate chats outside the Project: if you start a chat outside this specific Project, none of this behavior applies.
- No progress tracking: it doesn't remember what you've studied across sessions in a structured way (no dashboard, no history log).

## What I built with AI, and how

I built this using Claude.ai's Project feature — the custom instructions above are the core of the "build." I wrote and iterated on the instructions myself, tested them against real study questions, and adjusted wording where the assistant wasn't behaving as intended (e.g., tightening the instruction after it kept skipping the "check understanding" step). I did not write backend code for this — the "build" is the prompt design and testing, not software engineering, and I'm naming that directly rather than overstating it.

## Demo

[Add your 3–5 minute demo video link here]

## Links

- Portfolio site: [add your FlyRank domain URL here]
- Demo video: [add your video link here]
