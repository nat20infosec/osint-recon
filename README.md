# osint-recon

A [Claude Code](https://claude.com/claude-code) skill for passive, public-source security recon on a vendor, product, domain, or your own organization's footprint. Produces a graded, sourced **OSINT Intelligence Brief** — not a verdict, but the evidence a security or platform review needs to start from.

> **This repo has moved.** The `osint-recon` skill now lives and gets updates at [nat20infosec/skills](https://github.com/nat20infosec/skills) — `/plugin marketplace add nat20infosec/skills` then `/plugin install osint-recon@nat20infosec`. This repo is archived and kept for reference only.

Security/technical scope only — not financial, legal, or sanctions due diligence, and not a people-search tool. See [SKILL.md](SKILL.md) for the full scope, guardrails, and output format.

## What it does

- Investigates vendor/organizational security posture, domain & infrastructure footprint, product architecture risk, and current threat context.
- Grades every finding on two independent axes — **source reliability** and **corroboration** — plus severity where relevant, so confidence is never overstated.
- Strictly passive: search engines, public DNS/WHOIS, certificate transparency, web archives, published trust pages, public filings, public threat-intel. No scanning, probing, or authentication attempts against the target.
- Outputs a single Markdown brief: assessment up front, findings with sources, recommendations tied to findings, and an honest gaps section.

## Install

Claude Code loads skills from `~/.claude/skills/`. Clone this repo directly into that directory:

```bash
git clone https://github.com/nat20infosec/osint-recon.git ~/.claude/skills/osint-recon
```

(On Windows, that's typically `%USERPROFILE%\.claude\skills\osint-recon`.)

Restart Claude Code (or start a new session) and the skill will be available.

## Use

Invoke it directly, or just ask naturally and Claude Code will pick it up when the request fits:

```
/osint-recon acme-vendor.com — checking their security posture before we sign an integration
```

## License

[MIT](LICENSE)
