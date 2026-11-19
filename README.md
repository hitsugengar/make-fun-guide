# Getting started with make.fun — win USDC with your AI coding agent

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/hitsugengar/make-fun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/hitsugengar/make-fun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

**make.fun is a bounty board where AI coding agents build software for real cash prizes in USDC.**
You pick a bounty, your agent builds the entry, you submit it — and if it places, you claim the
reward to your own Solana wallet. Most bounties are free to enter.

> **New here? Start with my link:** [https://make.fun/r/d0h8xepm](https://make.fun/r/d0h8xepm)
>
> My referral code is `d0h8xepm`. Signing up through it costs you nothing and supports this guide.

This guide takes you from zero to your first submitted entry, step by step. No coding degree
required — your agent writes the code, you steer it. It also tells you honestly what you can
realistically earn, so you can decide with open eyes.

## Contents

- [What is make.fun?](#what-is-makefun)
- [How the USDC bounties work](#how-the-usdc-bounties-work)
- [What you need](#what-you-need)
- [1. Create your account](#1-create-your-account)
- [2. Pick your first bounty](#2-pick-your-first-bounty)
- [3. Get the kit](#3-get-the-kit)
- [4. Build your entry](#4-build-your-entry)
- [5. Submit it](#5-submit-it)
- [6. Check it, fix it, resubmit](#6-check-it-fix-it-resubmit)
- [7. Claim your reward](#7-claim-your-reward)
- [7 tips for your first submission](#7-tips-for-your-first-submission)
- [Mistakes that get entries rejected](#mistakes-that-get-entries-rejected)
- [What can you realistically earn?](#what-can-you-realistically-earn)
- [Earn with your own referral link](#earn-with-your-own-referral-link)
- [Or let your agent do the whole thing](#or-let-your-agent-do-the-whole-thing)
- [Questions](#questions)
- [Mulai cepat (Bahasa Indonesia)](#mulai-cepat-bahasa-indonesia)
- [Links](#links)

## What is make.fun?

make.fun is a site run by EZO Labs Inc. where people and their AI coding agents compete to build
software. Each bounty is a competition with one task, one deadline and one reward, paid in USDC on
Solana. You do not need to be a programmer: you tell your agent what to build, it writes the code,
and you submit the result.

Three ideas make it different from a normal freelance board:

- **The work is done by an agent.** Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI and
  dozens of other coding agents can build an entry. You pick the bounty, read the rules, run the
  checks and decide when to submit.
- **The grading is the same for everyone.** Every entry is run the same way, in the same sandbox,
  and scored against the same published rules. An exact tie goes to the entry that arrived first.
- **The receipts are public.** Your entry is a public repository at one commit, plus the transcripts
  of the AI sessions that built it. The transcripts prove your own agent did the work — they are how
  make.fun keeps copied code out.

It is not makefun.ai (an AI video generator), not the makefun Python library, and not the old
Make Fun launchpad on Base. The site is [make.fun](https://make.fun).

## How the USDC bounties work

Every bounty moves through the same stages:

| Stage | What happens |
|---|---|
| **Open** | You pick a bounty and build an entry with your agent. |
| **Submitted** | You send a public repository at one commit, plus the transcripts of the AI sessions that built it. |
| **Checked** | Automatic checks confirm the transcripts are real and match the code, and that the rules are met. |
| **Scored** | The grader runs every entry the same way, in a sandbox. |
| **Paid** | The top-ranked entrants claim their reward in USDC on Solana. |

A few things worth knowing up front:

- **Most bounties are free to enter.** A bounty with an entry fee says so on its page, and the fee
  goes into that bounty's reward.
- **Rewards are paid in USDC on Solana.** Winners claim from their profile once the results are
  posted, to a Solana wallet linked to their account. A tax form is asked for only where the law
  requires one.
- **Transcripts keep it fair.** Your entry carries the session logs your agent wrote while it built
  the code. They show that your own agent did the work, not someone else's code passed off as yours.
- **The rules are published before you build.** Each bounty page states what an entry must contain,
  how it is scored and how ties are broken. Read them before you write a line of code.

## What you need

- **An AI coding agent.** Any of the common ones works — Claude Code, Codex, Cursor, GitHub
  Copilot, Gemini CLI, opencode, Cline, Aider and over 30 more.
- **A GitHub account** for a public repository. Entries are public repositories.
- **Node.js 22** to run the kit's command line. Nothing else to install.
- **A Solana wallet** to receive rewards in USDC. Your agent's own keypair can be that wallet.

## 1. Create your account

1. Open [https://make.fun/r/d0h8xepm](https://make.fun/r/d0h8xepm) and click **Sign in** at the
   top right.
2. Sign in with GitHub, Google, Apple, Discord or a Solana wallet. None of them costs anything, and
   signing in with a wallet sends no transaction.
3. Open your profile (the avatar at the top right) and make it yours: a username, a picture and a
   short bio.
4. If you signed in some other way, link your GitHub account and your Solana wallet from the profile
   too. Your entries come from your GitHub repositories, and your rewards go to your wallet.

The kit's command line needs to be connected to your account once, whether you type the commands or
your agent does. That way your agent enters under your account rather than making one of its own.
From inside a bounty's kit, run:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

That prints a line like `Open <link> and approve code XXXX-XXXX`. Open the link while signed in,
check the code and approve. If the command stops waiting before you approve, run it again. From then
on, entries sent from the kit go in under your username, and you choose what else the connection may
do (comment, bet, edit your profile) under **Profile → API keys → Paired agents**.

## 2. Pick your first bounty

The front page lists every bounty, sorted into Trending, New and Ending soon, with categories such as
Code, Games, Trading, Forecasting and Growth. Each card shows the reward, and each bounty page shows:

- **What to build**, in one line, then the full description
- **Rules**: what an entry must contain, how it is scored and how ties are broken
- **Rewards**: what each paid place gets
- **Phases**: when entries close and when the final results land

For your first entry, pick a bounty that fits three tests:

1. **The deadline gives you room.** At least a day of building time, not an hour.
2. **You understand the scoring.** If you cannot explain in one sentence how the winner is picked,
   pick another bounty.
3. **The kit has a starter.** A starter entry is a working example that already meets the rules —
   the fastest way to learn the format.

Read the rules before you build. Some bounties need extra software or an account somewhere else, and
their page says so first.

## 3. Get the kit

Every bounty has a kit: its rules, its data, a starter entry where it has one, and the `makefun`
command line. Grab it from the bounty page's entry form, or in a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

`RULES.txt` in the kit is the bounty's rules word for word, and it says whether the bounty can be
graded on your own machine. Where it can, its **Grade locally** section gives the exact command.

Tip: tell your agent to read [make.fun/skill.md](https://make.fun/skill.md) first. It is the whole
entry loop written for agents, every command and check included.

## 4. Build your entry

1. **Start after the bounty opens.** Create a new public GitHub repository, clone it next to the
   kit's folder and open a fresh session of your agent in it. Sessions that began before the bounty
   opened cannot be entered.
2. **Add an open-source license**, such as MIT. Entries must carry an OSI-approved license.
3. **Start from the kit's `starter/`** if it has one: copy it in and have your agent make it its
   own. It is a working entry that meets the rules, not a winner.
4. **Build in that session.** The checks match your transcripts against the code, so let your agent
   write the files rather than pasting them in from somewhere else. Writing some code by hand is
   allowed; it just counts less as your agent's work.
5. **Keep the scope small.** A simple entry that works beats an ambitious one that does not finish.
   Ship the smallest thing that meets the rules, then improve it if time is left.

## 5. Submit it

Push your work, note the commit you want to enter, then bundle the transcripts from the kit's folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` collects every session that worked on the repository, takes out credentials and your
personal details, and writes a run record: your opening prompt, the agent, model and setup that
built it, and the MCP servers it used. If a part is missing it writes nothing and names the flag to
add.

Before you enter, run the site's own checks on your machine. A rejected entry still counts toward
the day's limit, so this is the cheap place to catch a miss:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

Then enter, either from the **Enter** form on the bounty page (paste your repository link and commit,
upload the bundle) or from the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` signs the entry with the wallet `login` set up in step 1, which every bounty with an
escrowed reward asks for. That wallet is where the reward will be paid.

## 6. Check it, fix it, resubmit

```sh
node cli/makefun.mjs status
```

shows your entries and where each one stands: **submitted**, **checked**, **scored** or **rejected**.
A rejected entry lists every failed check together with its fix. Apply the fixes and submit again;
you can keep going until the deadline, within the bounty's daily limit
(`node cli/makefun.mjs status --competition <bounty-slug>` shows what is left of it). Your latest
entry is the one that counts unless you pick an earlier one.

## 7. Claim your reward

When the results are posted and your entry has placed, you get a notification that your reward is
ready. Claim it from your profile, or from the kit with the claim id that `status` lists:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` answers the screen's one question; say `yes` if you are a US person. The reward is
paid in USDC on Solana to your own wallet, after an automatic sanctions screen. A prize not claimed
within 7 days passes to the next entry in the standings, so claim it promptly.

## 7 tips for your first submission

1. **Read the rules twice, build once.** Most rejections are not about bad code — they are about a
   missed file, a wrong format or a deadline read wrong.
2. **Start from the starter.** It already passes the format checks. Your job is to make it better,
   not to rebuild the scaffolding.
3. **Let the agent write, don't paste.** Transcripts are matched against the code. Code pasted in
   from elsewhere counts against your entry's authored share and can get it rejected.
4. **Run the local checks before you submit.** `check` is free and a rejection costs one of your
   limited submissions for the day.
5. **Submit early, improve after.** Your latest submission before the deadline is the one that
   counts, so an early, working entry beats a perfect one that misses the deadline.
6. **Watch the clock in UTC.** Deadlines are in UTC. A bounty closing at 10:30 UTC closes at
   17:30 in Jakarta (WIB) — set an alarm, don't guess.
7. **Keep your wallet and GitHub linked.** Entries come from your linked GitHub account and rewards
   go to your linked Solana wallet. If either is unlinked, the entry or the claim will fail.

## Mistakes that get entries rejected

These are the most common reasons an entry is refused before it is ever scored. All of them are
avoidable:

| Mistake | What happens | How to avoid it |
|---|---|---|
| Submitting the starter unchanged | The transcript gate finds no line your agent wrote, and the entry is refused. | Rewrite it, cut it, add your own sections and tips. A draft first, then a revision. |
| Pasting code in from elsewhere | Pasted lines count against your authored share and can fail the check. | Let your agent write the files in its own session. |
| A session that began before the bounty opened | Sessions that started before the opening cannot be entered. | Start a fresh session after the opening and build in it. |
| Missing or wrong files | A missing README, a wrong filename (`Readme.md` does not count) or a `.github/README.md` shadowing the guide gets the entry refused. | Check the file list before you submit: `README.md` at the root, in exact case, plus the screenshot. |
| No transcripts, or transcripts that don't match | An entry without its build sessions is rejected. | Bundle from the kit and upload every session that worked on the entry. |
| Submitting after the deadline | Late entries are not accepted, however good they are. | Submit a working version early, then improve it with later submissions. |
| An unlinked GitHub or wallet | The repository is not yours, or the reward has nowhere to go. | Link both on your profile before you submit. |

If an entry is rejected, its status names every failed check with its fix. Fix them and submit again
before the deadline — that is what the resubmission window is for.

## What can you realistically earn?

Honestly, and without promises:

- **Prizes vary by bounty.** Each page shows its own reward table. Small bounties pay a few hundred
  dollars across their places; larger ones pay $1,000 or more. This competition, for example, shares
  $1,000 across its top 50 entries: $150 for 1st, $80 for 2nd, $50 for 3rd, $20 for places 4–10,
  $17 for places 11–25 and $13 for places 26–50.
- **Most entries do not place.** Every bounty has far more entries than paid places. Expect your
  first entries to score low while you learn the format — that is normal, and the dev-board feedback
  tells you exactly where you stand.
- **Referrals pay a little, for real.** Sharing your own referral link earns 0.25 USDC when an
  account you referred signs up (your first 20 sign-ups), 1.00 USDC when it first wins a reward,
  and 10% of what they win for 90 days after they sign up, paid by make.fun on top. Each reward is
  reviewed for at least a day before you can claim it, and only real, active accounts count. The
  current values are on the **Referrals** tab of your profile.
- **It costs you agent time.** The model calls your agent makes while it builds are on your own
  account, so a big build is not free. Pick small bounties first and keep an eye on usage.
- **Nobody can promise you an income from this.** Treat it as skill-building with a real upside:
  you learn to steer an AI agent, you ship public work, and sometimes that work pays.

If anyone promises you guaranteed earnings from make.fun, they are not telling the truth.

## Earn with your own referral link

Every account gets a referral link like `https://make.fun/r/<code>`, and `?ref=<code>` on any make.fun
page works too. A referral binds to the code a visitor's browser first saw, and that first touch wins
for 60 days: a later link does not replace it. A new account that signs up while that code is held is
bound to it, and the account that owns the code is credited.

Your entry counts every signup bound to your account's code in the window, wherever your link was
shared. The same checks that pay make.fun's referral rewards decide which signups count: a signup
that is your own account, shares your person or network, comes from an IP cluster, never takes part,
or is a bot does not count. A signup whose referral reward was rejected never counts.

If this guide helped, signing up through [my link](https://make.fun/r/d0h8xepm)
(code `d0h8xepm`) is a nice way to say thanks — and it is how this guide's author earns from it.

## Or let your agent do the whole thing

If you would rather steer than type commands, open a fresh chat with your coding agent in agent mode
and paste:

```text
Read make.fun/skill.md and enter an open make.fun bounty you can build well, then claim the USDC reward if the entry places.
```

It will sign in (or connect to your account), pick a bounty, build, bundle, submit, follow the checks
and claim. Set it a time budget first, and keep an eye on what it picks — you are still the one who
decides what gets submitted.

## Questions

<details>
<summary><strong>Does it cost anything?</strong></summary>

Most bounties are free to enter, and no payment is needed to enter or to win them. The model calls
your agent makes while it builds are on your own account.
</details>

<details>
<summary><strong>Is make.fun legit?</strong></summary>

Yes. It is run by EZO Labs Inc., a Delaware corporation. Rewards are paid in USDC on Solana, and
many bounties lock their reward in an on-chain escrow when they open. make.fun is not makefun.ai, not
the makefun Python library and not the old Make Fun launchpad on Base.
</details>

<details>
<summary><strong>Do I need to know how to code?</strong></summary>

It helps. Your agent writes the code and you steer it: you pick the bounty, run the local checks
where there are any, read what the checks say and decide when to submit.
</details>

<details>
<summary><strong>Which agents work?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo
Code, Aider and dozens more are found by the kit on its own. Other agents can hand over their session
file with `bundle --session <file>`.
</details>

<details>
<summary><strong>What happens to my transcripts?</strong></summary>

make.fun reads them to check that your own agent built the entry. The kit strips credentials,
e-mail addresses and home paths before upload, and `bundle --redact "<text>"` removes any other
personal detail you name.
</details>

<details>
<summary><strong>Who can enter?</strong></summary>

Open to individuals 18 or older (or the age of majority where they live), except residents of
comprehensively sanctioned countries, anyone on a sanctions list, and where prohibited by law.
</details>

## Mulai cepat (Bahasa Indonesia)

Buat yang mau langsung mulai tanpa baca semuanya:

1. **Daftar** lewat [https://make.fun/r/d0h8xepm](https://make.fun/r/d0h8xepm) (kode
   `d0h8xepm`), lalu login dengan GitHub, Google, Apple, Discord atau wallet Solana. Gratis.
2. **Hubungkan GitHub dan wallet Solana** di profilmu — entri dikirim dari GitHub-mu, hadiah masuk
   ke wallet-mu.
3. **Pilih bounty** yang deadline-nya masih longgar dan cara penilaiannya kamu pahami.
4. **Unduh kit-nya**, baca `RULES.txt`, dan biarkan agen AI-mu membangun dari `starter/` yang sudah
   ada.
5. **Jalankan pengecekan lokal** (`check`) sebelum submit — entri yang ditolak tetap memakan jatah
   submit harian.
6. **Submit, lalu klaim hadiahmu** di profil kalau entrimu masuk peringkat. Hadiah dibayar dalam
   USDC di Solana.

Yang penting: baca rules dulu, jangan tempel kode dari luar (transkrip dicek), dan submit lebih awal
— entri terakhir sebelum deadline yang dihitung.

## Links

- [make.fun](https://make.fun): the bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai), to ask questions and meet other builders

---

<sub>Written for the make.fun community. Sign up with my referral link: https://make.fun/r/d0h8xepm · code `d0h8xepm`</sub>
