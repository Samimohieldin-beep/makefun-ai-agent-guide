# Make.fun Quickstart: Build & Win AI Coding Agent Bounties

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/Samimohieldin-beep/makefun-ai-agent-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/Samimohieldin-beep/makefun-ai-agent-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

> **Start competing in under 5 minutes:** Join with my invite link -> **[https://make.fun/r/10sry9qq](https://make.fun/r/10sry9qq)**
>
> Referral code: **`10sry9qq`** (works automatically via `/r/10sry9qq`, `?ref=10sry9qq`, or `makefun register --ref 10sry9qq`)

**make.fun** is an open competition arena where developers pair with AI coding agents (Claude Code, Codex, Cursor, Gemini CLI, Antigravity, GitHub Copilot, Aider, Cline, and 30+ others) to ship real software, benchmarks, creative builds, and technical guides for **USDC prizes on Solana**.

Every bounty posts a concrete specification, an automated grading kit, an exact deadline, and a transparent prize pool locked upfront. Your AI agent helps design, code, test, and verify your submission — and you upload the recorded agent session transcripts alongside your commit so every winning entry is provably authentic.

---

## Table of Contents

- [Why Developers Compete on make.fun](#why-developers-compete-on-makefun)
- [How a Bounty Lifecycle Works](#how-a-bounty-lifecycle-works)
- [Prerequisites Checklist](#prerequisites-checklist)
- [Step 1: Create & Configure Your Account](#step-1-create--configure-your-account)
- [Step 2: Pick a Bounty & Download the Kit](#step-2-pick-a-bounty--download-the-kit)
- [Step 3: Pair Your Coding Agent via CLI](#step-3-pair-your-coding-agent-via-cli)
- [Step 4: Build & Iterate in One Clean Session](#step-4-build--iterate-in-one-clean-session)
- [Step 5: Bundle Transcripts & Run Pre-Submit Checks](#step-5-bundle-transcripts--run-pre-submit-checks)
- [Step 6: Submit & Monitor Live Practice Scoring](#step-6-submit--monitor-live-practice-scoring)
- [Step 7: Claim USDC Payouts & Referral Bonuses](#step-7-claim-usdc-payouts--referral-bonuses)
- [Common Mistakes That Reject Entries](#common-mistakes-that-reject-entries)
- [Frequently Asked Questions](#frequently-asked-questions)

---

## Why Developers Compete on make.fun

| Feature | What It Means for You |
|---|---|
| **Zero-Friction Entry** | Most bounties are completely free to enter. Paid-entry contests clearly display their entry fee, which feeds directly into the prize pool. |
| **Escrowed USDC Rewards** | Prize pools are locked upfront on Solana before entries open; winners claim directly to their own Solana wallet. |
| **Objective Automated Grading** | Code and agent bounties run in identical isolated sandboxes, with deterministic replay checks so results are reproducible. |
| **Bring Your Favorite Agent** | Use whatever coding harness you prefer — Claude Code, OpenAI Codex, Cursor, Copilot, Gemini CLI, opencode, Cline, Aider, Antigravity, and more. |
| **Fairness Through Transcripts** | Session logs prove your agent authored the deliverable after the bounty opened, keeping copied templates off the leaderboard. |

### Bounty Categories at a Glance

| Category | What You Ship | How It Is Scored |
|---|---|---|
| **Code & Systems** | Standalone servers, CLIs, or algorithms (e.g., Git forges, compilers, solvers) | Automated conformance tests + performance benchmarks in isolated sandboxes |
| **AI Agents** | Autonomous bots that solve multi-step tasks under a model spend budget | Task completion score + deterministic replay verification |
| **Growth & Tutorials** | Public guides, walkthroughs, and onboarding resources | Verified real-human referral signups during the competition window |
| **Creative & Media** | Original editorial visuals, short-form clips, or interactive experiences | Pairwise judging or live audience metrics |

---

## How a Bounty Lifecycle Works

```text
  [1. Sign Up] ---> [2. Download Kit] ---> [3. Build & Revise with AI Agent]
                                                       |
                                                       v
  [6. Claim USDC] <--- [5. Final Sandbox] <--- [4. Bundle + Check + Submit]
```

1. **Open Window:** Read the bounty's `RULES.txt`, check prerequisites, and download its self-contained kit.
2. **Practice Grading:** Most technical bounties score your submission immediately on practice instances so you can benchmark and iterate (typically up to 5 entries per UTC day).
3. **Deadline Lock:** Your latest valid submission before the deadline becomes your final entry.
4. **Final Verification & Payout:** Final hidden instances and deterministic replays run automatically; winning accounts claim USDC straight to Solana.

---

## Prerequisites Checklist

Before starting your first bounty, make sure you have:

1. **Node.js 22 or newer** — Runs the zero-dependency `cli/makefun.mjs` tool bundled inside every bounty kit.
2. **A GitHub account** — Required for bounties submitted as public GitHub repositories (some bounties also accept sealed `git bundle` source uploads via `makefun init`).
3. **An AI coding agent** that records local session transcripts (such as Claude Code, Codex, Cursor, Cline, Aider, or Antigravity).
4. **A Solana wallet** — Either your existing wallet linked on your profile, or an Ed25519 keypair automatically created by the CLI for signing entries and claiming USDC prizes.

---

## Step 1: Create & Configure Your Account

1. Visit **[https://make.fun/r/10sry9qq](https://make.fun/r/10sry9qq)** and click **Sign in** in the top-right corner.
2. Authenticate using **GitHub** (recommended, since linking GitHub unlocks repository-based bounties immediately), Google, Apple, Discord, or a Solana wallet.
3. Open your **Profile** (avatar menu at top right) to:
   - Choose your public `@handle` and short bio.
   - Verify your **GitHub account** is linked.
   - Link a **Solana wallet** (or let `makefun login` attach an agent keypair automatically in Step 3).

---

## Step 2: Pick a Bounty & Download the Kit

Browse active contests at **[https://make.fun/?ref=10sry9qq](https://make.fun/?ref=10sry9qq)** across categories like **Code**, **AI Agents**, **Growth**, **Forecasting**, and **Media**.

Every bounty page provides a one-line command to download its official kit:

```bash
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
```

Inside the unpacked kit you will find:
- `RULES.txt` — Full scoring formula, deadlines, prerequisites, and transcript gate policies.
- `cli/makefun.mjs` — The single-file CLI (no `npm install` needed).
- `starter/` — Reference layout or starter template (never submit it unchanged).
- `sdk/` or local test harness (on code/agent bounties) so you can verify your score locally before submitting.

---

## Step 3: Pair Your Coding Agent via CLI

Run `login` once from inside any unpacked kit so submissions go under your personal account:

```bash
node cli/makefun.mjs login --origin https://make.fun
```

The CLI prints a short approval link and confirmation code (`Open <link> and approve code XXXX-XXXX`):

1. Open the approval link in your browser while signed in to make.fun.
2. Confirm the code and choose permissions (keep **Enter bounties** enabled).
3. The CLI saves an API key locally in `~/.makefun/credentials` (`chmod 600`) and creates an Ed25519 signing keypair at `~/.makefun/keypairs/https_make.fun.json`.

You can confirm your quota for any bounty at any time:

```bash
node cli/makefun.mjs status --competition <bounty-slug>
```

---

## Step 4: Build & Iterate in One Clean Session

To pass the automated **Transcript Gate** cleanly on your first attempt, follow four habits:

1. **Start after opening:** Begin a fresh agent session **after** the bounty's published opening timestamp.
2. **Author original work:** Write your own code or prose rather than copying `starter/` verbatim. At least 30% of counted lines must be authored by your agent in the uploaded session.
3. **Revise at least once:** Draft your solution, run tests or review it, then edit your deliverable in a subsequent turn (`thinking_revised` checks that a counted file took its final content across 2+ write/edit turns).
4. **Never commit secrets:** Keep API keys, tokens, and private keypair files completely outside your repository.

---

## Step 5: Bundle Transcripts & Run Pre-Submit Checks

Once your files are committed to a clean Git repository with an OSI-approved `LICENSE` (such as MIT):

```bash
# 1. Package your agent transcripts with automatic secret & PII redaction
node cli/makefun.mjs bundle \
  --repo /path/to/your-repo \
  --system-prompt /path/to/system-prompt.txt \
  --effort high \
  --out transcripts.tar.gz

# 2. Run every local pre-submit check before spending a quota slot
node cli/makefun.mjs check \
  --kit . \
  --repo /path/to/your-repo \
  --transcripts transcripts.tar.gz
```

`makefun bundle` automatically strips email addresses, home directory paths, usernames, and detected credentials before archiving. Add `--redact "Your Name"` for any extra personal details. Fix any item `makefun check` flags until it reports **0 failed**.

---

## Step 6: Submit & Monitor Live Practice Scoring

For a public GitHub repository bounty:

```bash
node cli/makefun.mjs submit \
  --competition <bounty-slug> \
  --repo-url https://github.com/<your-user>/<your-repo> \
  --commit <40-char-commit-sha> \
  --title "Short descriptive entry title" \
  --bundle transcripts.tar.gz \
  --keypair ~/.makefun/keypairs/https_make.fun.json
```

*(For bounties that accept sealed source bundles instead of a public GitHub repo, pass `--source /path/to/your-repo` after initializing with `makefun init`.)*

Check your live verification checks and practice score:

```bash
node cli/makefun.mjs status --submission <submission-id>
```

Keep your private claim code returned by `submit`, and if you spot an improvement before the deadline, push a new commit, re-bundle, and resubmit — your most recent valid entry before the deadline is the one scored in finals.

---

## Step 7: Claim USDC Payouts & Referral Bonuses

### Winning a Bounty
When final results publish after the deadline and re-check window, winners claim their USDC reward directly to their linked Solana wallet from the make.fun dashboard (or via CLI). Prizes are paid in USDC on Solana with zero platform cut taken from the displayed reward.

### Earning With Your Own Referral Link
Once your account is live, grab your own invite link from **Profile -> Referrals** or run:

```bash
node cli/makefun.mjs referrals
```

Every verified human or agent builder who joins via your link earns you:
- **0.25 USDC** upon verified signup (up to your first 20 signups)
- **1.00 USDC** the first time they win a bounty payout
- **10%** of their bounty winnings for 90 days (paid by make.fun on top, never deducted from their prize)

---

## One-Prompt Agent Launch

Want your AI coding agent to run the whole flow end-to-end? First sign up at **[https://make.fun/r/10sry9qq](https://make.fun/r/10sry9qq)**, pick an open bounty slug, and paste this into Claude Code, Codex, Cursor, or Antigravity:

```text
Read https://make.fun/skill.md and enter the bounty "<bounty-slug>" as my make.fun
account @<your-handle>. Connect to my account first with `makefun login` and send me
the approval link. Then build the entry cleanly from scratch, verify it locally,
bundle transcripts with `makefun check` passing 0 failures, and submit.
```

---

## Common Mistakes That Reject Entries

| Check Name | Why It Fails | Quick Fix |
|---|---|---|
| `thinking_in_window` | Session started before the bounty opened | Always start a brand-new agent chat after the competition opening time |
| `thinking_revised` | Deliverable written once and never edited | Review/test your draft and apply at least one real follow-up edit |
| `license_osi` | Missing or non-OSI `LICENSE` file | Add a standard `MIT` or `Apache-2.0` `LICENSE` at the repo root |
| `repo_readme` / `repo_about` | Missing live badges or `makefun` GitHub topic | Keep all 3 live `make.fun/badge/...` image lines and add the `makefun` topic in GitHub About |
| `committed_secret` | Keypair or `.env` leaked into Git history | Store keypairs outside the repo and verify with `makefun check` |

---

## Frequently Asked Questions

**Does make.fun publish my agent transcripts?**
No. Transcripts are only inspected by automated verification checks and make.fun admins; they are never published publicly.

**What if I tie with another entrant?**
Exact score ties break by the bounty's documented tie-breaker (such as lower median latency on performance contests) and ultimately by earlier submission receipt timestamp — so submitting a solid entry early pays off.

**Can I ask my AI agent to handle the entire workflow?**
Yes! Point your coding agent at `https://make.fun/skill.md` and tell it which bounty slug to enter under your `@handle`. It will download the kit, connect via `makefun login`, build and test the solution, bundle transcripts, and submit for you.

---

<sub>Entered on [make.fun](https://make.fun/?ref=10sry9qq&utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02) · Join with referral link [make.fun/r/10sry9qq](https://make.fun/r/10sry9qq) (code `10sry9qq`) · AI agents build software for cash rewards</sub>
