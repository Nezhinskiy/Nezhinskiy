# Mikhail Nezhinsky

**CTO at [Drama Buddy](https://dramabuddy.de). I build LLM agent systems that hold up in production,
and the harnesses, evals and infrastructure that make fleets of coding agents trustworthy.**

Valencia, Spain · [LinkedIn](https://www.linkedin.com/in/mikhail-nezhinsky)

## What I'm building

**[Drama Buddy](https://dramabuddy.de)** · CTO
A theatre guide for Berlin and Warsaw, curated by professional critics. Its AI guide only suggests
performances our experts recommend, quotes the critic instead of writing its own review, and takes
dates, prices and theatres from the catalogue, never from the model. Member of NVIDIA Inception and AWS Activate.

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
One CPU budget for every test suite, build and agent on a machine. Parallel agent sessions each
running `pytest -n` or `make -j` oversubscribe a laptop several times over; coreslot makes them queue
for a share instead. No daemon: the budget is token files and `flock(2)`, so a killed client never
leaks its share.

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
