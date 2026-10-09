# pair-with-me

Think a design or plan through with Claude as an equal partner until you both agree.

```bash
npx skills add mazzeb/skills --skill pair-with-me -g -a claude-code
```

Inspired by Matt Pocock's [grill-me](https://github.com/mattpocock/skills), which interviews
you one question at a time. pair-with-me flips the role: Claude is a sparring partner that lays
out options and costs, takes its own position, says plainly where you are wrong, and only moves
on once a topic is decided together. Built to plan a topic deeply, not to extract a plan from
your head.

Usage: `/pair-with-me <topic>` or `/pair-with-me <path to a handoff file>`. Only starts when
invoked explicitly (`disable-model-invocation: true`).

Full description in the [repository README](../../README.md#pair-with-me).
