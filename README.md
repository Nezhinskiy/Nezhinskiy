# Mikhail Nezhinsky

**CTO at [Drama Buddy](https://dramabuddy.de). I build LLM agent systems that hold up in production,
and the harnesses, evals and infrastructure that make fleets of coding agents trustworthy.**

Valencia, Spain · [LinkedIn](https://www.linkedin.com/in/mikhail-nezhinsky)

## What I'm building

**[Drama Buddy](https://dramabuddy.de)** · CTO
A theatre guide for Berlin and Warsaw, curated by professional critics. Its AI guide only suggests
performances our experts recommend, quotes the critic instead of writing its own review, and takes
dates, prices and theatres from the catalogue, never from the model. Member of NVIDIA Inception and AWS Activate.

**[LiveBridge](https://github.com/getLiveBridge/LiveBridge)** · Swift · TypeScript · [site](https://getlivebridge.com)
Talk to an open Claude Code session by voice. GPT-Live is the front desk: it talks with you, asks
what you mean and gives the real work to Claude Code. A macOS menu bar app plus a Claude Code plugin.

**[genokeeper](https://github.com/genokeeper/genokeeper)** · Python · Docker
A local analyser for your own whole genome sequencing data. It calls variants on your Mac, grades
findings against ClinVar, gnomAD and ClinGen, and checks them again every month. A research tool,
not medical advice.

**[stayfixed](https://github.com/stayfixed/stayfixed)** · Python · [PyPI](https://pypi.org/project/stayfixed/)
A methodology harness for coding agents, shipped as a Claude Code plugin. Gates start advisory and
turn on one by one as the repository passes them; gate policy is read from the base branch, so a PR
cannot loosen it; fixed bugs keep a regression that is re-run. Its own suite: 6,900+ tests and 2,500+
declared mutations checked in CI.

**[ai-daybook](https://github.com/Nezhinskiy/ai-daybook-showcase)** · Python · Temporal · [live demo](https://ai-daybook.cc/app/demo.html)
A production life-logging system run by eleven long-lived LLM agents on Temporal. The model gets
exactly one decision per request, inside a boundary computed in advance by ordinary code. An LLM
writes SQL against production behind an AST validator, a read-only role and row-level security.
Releases are gated by evals.

**[coreslot](https://github.com/core-slot/coreslot)** · Go · `brew install core-slot/tap/coreslot`
A memory guard for the heavy commands that coding agents run in parallel. A command starts when the
machine has the memory for it, and if the machine is really in danger, the newest commands stop and
restart later. No daemon and no root: state is files and `flock(2)` locks, so a killed run never
leaks its reservation.

**[local-ci-pool](https://github.com/Nezhinskiy/local-ci-pool)** · Go · Docker
A shared self-hosted GitHub Actions runner pool: the Macs you already own run private-repo jobs in
ephemeral containers while they are awake, and GitHub-hosted runners take over when none is.

**[reask](https://github.com/Nezhinskiy/reask)** · agent skill · [PyPI](https://pypi.org/project/reask/)
When your agent asks a question you can't answer, `/reask` makes it ask again as a self-contained
briefing: context from zero, every option's trade-offs, and a recommendation.

## How I work

- **The model decides; code owns everything else.** Lifecycle, retries, timers, permissions and data
  boundaries belong to deterministic code and durable workflows, not to prompts.
- **Evals are a release gate, not a dashboard.** A flaky case is a defect to root-cause.
- **Agents' claims are checked, not trusted.** "Tests pass" counts when the test runner says so.
- **I ship by directing fleets of coding agents** under specs, reviewed plans and enforced checks,
  and I build the tools that make that safe.

## Before this

Tech Lead at Athena AI (London; Startups 100 UK, 2024): LLM products from MVP to production.
Earlier: founded and ran a B2B equipment-supply company and built its internal systems.

<sub>Most of my production work lives in private repositories; the contribution graph counts it.</sub>
