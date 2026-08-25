# Write with Life

A writing skill for drafts that are clean, correct, and somehow still dead on the page.

Most humanizers work at sentence level. They remove stock phrases, vary sentence length, soften formal language, and clean up familiar AI habits. The draft often keeps the same predictable shape: an introduction that announces itself, several equally weighted sections, and a conclusion that repeats the premise.

`write-with-life` starts earlier. It finds the piece's governing idea, chooses a structure, decides where the emphasis belongs, and establishes a credible narrator before it edits individual sentences.

## What it changes

The skill can:

- rebuild a draft around one clear spine;
- choose an architecture that fits the available material;
- give consequential ideas more space and supporting material less;
- establish the narrator's authority, distance, temperature, and relationship with the reader;
- control pace through paragraph movement and sentence rhythm;
- preserve deliberate fragments, repetition, triads, dashes, and other useful irregularities;
- remove stock AI language during a final sentence-hygiene pass;
- identify missing reporting material and leave unsupported details out.

It is designed for essays, articles, reports, launch posts, profiles, newsletters, scripts, and other nonfiction whose grammar may already be fine.

## How it works

The skill selects the depth of edit that the request requires:

1. **Sentence polish** keeps a structure that already works.
2. **Developmental rewrite** changes order, proportion, transitions, openings, and endings.
3. **Reporting assist** improves the available prose and surfaces the few details needed to take it further.

For a developmental rewrite, it maps the material, finds a governing movement, ranks each beat by importance, chooses the narrator, and drafts from that new plan. Sentence cleanup comes last.

## Guardrails

Liveliness cannot come at the expense of truth. The skill preserves supported facts, qualifications, quotations, citations, and technical terms. It will not manufacture:

- scenes or anecdotes;
- sensory details;
- first-person experience;
- emotions or opinions;
- quotations or sources;
- names, dates, numbers, or examples.

A sample written by the user is treated as the strongest evidence of voice. Published writers contribute craft principles; the resulting voice remains the user's.

The sentence audit also rejects canned reversal templates such as `not X, but Y` and `it isn't X; it's Y`. Important claims should earn their weight through evidence, position, specificity, and space.

## Install

Install globally with the Skills CLI:

```bash
npx skills add JavierDiaz90/write-with-life --global
```

Or clone it directly into your Codex skills directory:

```bash
git clone https://github.com/JavierDiaz90/write-with-life.git ~/.codex/skills/write-with-life
```

Reload your agent's skill list after installation if it does not appear immediately.

## Use

Invoke the skill directly:

```text
Use $write-with-life to recompose this draft:

[paste draft]
```

Match your own voice by including a sample:

```text
Use $write-with-life to rewrite the draft below.

Here is a sample of my writing:
[sample]

Here is the draft:
[draft]
```

Ask for the editorial reasoning when you want to inspect the structural decisions:

```text
Use $write-with-life to diagnose this draft, explain the structural problem, and rewrite it.
```

By default, the skill returns the finished prose without exposing its private beat map or emphasis ranking.

## Package structure

```text
write-with-life/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── sentence-hygiene.md
    ├── structure-and-emphasis.md
    └── voice-rhythm-and-tone.md
```

`SKILL.md` contains the shared workflow. The references are loaded only when the task needs deeper structural, voice, rhythm, or sentence-level guidance.

## Craft foundation

The skill draws on published craft discussions by John McPhee, Jon Franklin, Kim Cross, Lauren Kessler, Michael Pollan, Mark Kramer, Jim Collins, Joan Didion, and Roy Peter Clark. Source links and the principles derived from them appear in the relevant reference files.

The final sentence-hygiene pass was developed in conversation with [blader/humanizer](https://github.com/blader/humanizer), an MIT-licensed skill based on Wikipedia's [Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing). `write-with-life` keeps that cleanup work in its proper place: after the piece has found its structure, emphasis, and voice.
