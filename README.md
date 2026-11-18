# Agent Incident Recorder

**A flight recorder for AI agents.**

AI coding agents now run commands, edit files, call APIs and use real credentials on their own. When something goes wrong, most teams can't answer basic questions: which agent did it, what exactly it did, whose access it used, and what it touched.

Agent Incident Recorder captures every action an agent takes into a tamper-evident log and turns it into an incident report that a security team, auditor or insurer can trust.

## The problem

- Agents act faster and more often than any human, and their activity is scattered across tools and logs.
- Existing logs can be edited or deleted, so they don't hold up as evidence.
- Security teams have no standard way to investigate an "agent incident".

## How it works

1. **Capture.** Hooks into the agent (Claude Code first) and records every tool call: commands, file reads and writes, web requests, sub-agents.
2. **Protect.** Secrets, file contents and prompts are masked before anything is saved.
3. **Flag.** Risky behavior is tagged as it happens, such as reading credentials and then uploading data, piping a download into a shell, destructive commands, or acting on hidden instructions in a web page.
4. **Seal.** Each event is chained to the one before it, and the chain is signed regularly. Editing, deleting or reordering anything is detectable.
5. **Report.** Any time window becomes a clear incident report or a signed evidence bundle that someone else can verify independently.

## Who it's for

- Security teams letting developers use AI agents
- Companies facing audits (SOC 2, ISO 27001, the EU AI Act)
- Cyber insurers that need proof of what an agent did

## Status

Working prototype (v0.1). It records, flags, seals and reports for Claude Code, and the core is covered by tests.

**Next:** test in real agent sessions, a remote evidence vault, a team dashboard, and support for more agent platforms.

## Author

Abdimajid Mohamed, Information Technology Infrastructure, University of Minnesota Twin Cities
