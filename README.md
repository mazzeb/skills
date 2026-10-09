# mazzeb/skills

Skills for [Claude Code](https://claude.com/claude-code) and other coding agents.

## Install

```bash
# global, for Claude Code
npx skills add mazzeb/skills --skill pair-with-me -g -a claude-code

# project-local, for Claude Code
npx skills add mazzeb/skills --skill pair-with-me -a claude-code

# other agents: drop -a to pick interactively
npx skills add mazzeb/skills --skill pair-with-me

# later
npx skills update
```

Uses the [skills CLI](https://github.com/vercel-labs/skills). Without it, copy
`skills/pair-with-me/SKILL.md` into `~/.claude/skills/pair-with-me/` (global) or
`.claude/skills/pair-with-me/` (project).

## Skills

| Skill | What it does |
|-------|--------------|
| [pair-with-me](skills/pair-with-me/) | Think a design or plan through with Claude as an equal partner until you both agree. |

## pair-with-me

Claude pairs with you on a design or plan as an equal partner, in prose, until the two of you
agree. No menus, no interview.

### Where it comes from

This skill is inspired by Matt Pocock's well-known
[grill-me](https://github.com/mattpocock/skills) skill. grill-me interviews you relentlessly,
one question at a time, each with a recommended answer, until every branch of the design tree is
resolved. That works well when the plan is already in your head and needs to be extracted.

pair-with-me flips the role. Claude is not an interviewer but a sparring partner. For every
topic it lays out the options and what each costs, then takes its own position and says why. It
tells you plainly where you are wrong, changes its position only for a new argument or fact, and
names it when it does. Nothing is decided until you both agree. The goal is to plan a topic
deeply, together.

### How it works

- Walks down the decision tree one topic at a time, taking first what the others depend on.
- Closes each topic with one line on what was agreed before opening the next.
- While you disagree, looks for the arguments and requirements still unstated: by discussing,
  by what-if scenarios, or by an outside opinion given both positions neutrally.
- Starts from what the project already states (docs, code, issues) and looks it up instead of
  asking you. None of it is beyond change.

### Usage

```
/pair-with-me <topic>
/pair-with-me <path to a handoff file>
```

The skill has `disable-model-invocation: true`, so it only starts when you invoke it.

## License

[MIT](LICENSE)
