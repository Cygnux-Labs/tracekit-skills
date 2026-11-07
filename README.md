# Tracekit skills

Agent skills for [Tracekit](https://github.com/Cygnux-Labs/Tracekit), the open-source evidence and approvals layer for
AI agents: every tool call is signed and hash-chained by a signer the agent can't control, costly actions wait for a
person's approval, and anyone can verify the record offline.

## Install

```bash
npx skills add Cygnux-Labs/tracekit-skills
```

Then tell your coding agent: "set up Tracekit".

## Skills

| Skill | What it does |
|---|---|
| [`tracekit-setup`](skills/tracekit-setup/SKILL.md) | Sets Tracekit up for the person who runs the agent: it explains what Tracekit does, asks first, starts with a read-only look at last week (`tracekit audit --since 7d`), then installs the hooks for your agent (Claude Code, Codex, Cursor, Gemini CLI, OpenCode, goose and others) and checks them. When Tracekit holds a call, the agent waits for you and never answers the hold itself. |

Requires Tracekit 1.6.0 or later (`pip install -U tracekit-ai`).

## License

MIT, as Tracekit.
