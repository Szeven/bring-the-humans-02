# bring-the-humans-02 — NOTES

## What it is

A getting-started guide to make.fun, written as the README of a public GitHub
repository (repo: Szeven/bring-the-humans-02). Harness: referral/v1, guide
variant. Score = number of verified human signups brought through the
account's own referral link during the competition window; the 50
highest-ranked entries share the $1,000 USDC escrow (1st $150, 2nd $80,
3rd $50, 4th–10th $20, 11th–25th $17, 26th–50th $13).

## What the guide covers

- What make.fun is and how a bounty moves Open → Submitted → Checked →
  Scored → Paid; escrow locked before the bounty opens; transcripts keep
  entries fair; ties go to the earlier entry.
- What you need: an AI coding agent, a GitHub account, Node.js 22, a Solana
  wallet.
- Account creation (sign in with GitHub/Google/Apple/Discord/Solana wallet),
  connecting the kit CLI once (`login --origin https://make.fun`).
- Picking a bounty (read the rules; start small; mind the deadline).
- Getting the kit (`curl -sSL "https://make.fun/c/<slug>/kit" | tar xz`),
  `RULES.txt`, `grade-local`.
- Building the entry (fresh session after the opening, MIT license, starter
  as a starting point, let the agent write the files, add the README).
- Submitting: `bundle`, local `check`, then `submit`; daily entry limit
  (5/day max, fewer from some countries) and refused entries counting.
- `status`, fixing rejections, resubmitting; claiming with
  `claim --claim <id> --us-person no`.
- Letting the agent do the whole loop from one pasted prompt.
- Referral link: live terms checked 2026-11-19 via
  `node cli/makefun.mjs referrals` — code `9e5tqfea`, link
  https://make.fun/r/9e5tqfea; currently 10% of what a referred account wins
  for 90 days after signup, paid by the house on top; signup and first-win
  bonuses are switched off at the moment.
- FAQ: cost, legitimacy (EZO Labs Inc., Delaware; escrow at
  github.com/makedotfun/prize-escrow; not makefun.ai / makefun Python lib /
  old Base launchpad), coding needed, which agents work, transcripts,
  how referral signups count.

## Files

- `README.md` — the guide (written fresh in the builder session, draft +
  two revision passes; all three make.fun badges + the template footer with
  `?ref=9e5tqfea`; referral code appears as bare `9e5tqfea`,
  `/r/9e5tqfea` and `?ref=9e5tqfea`).
- `LICENSE` — MIT, with the `SPDX-License-Identifier: MIT` line.
- `.makefun/owner.json` — claim file, payout wallet
  GrHtSvTcmjHHWwZM7VsNPgZWoTwPnLxgpMDYfH6iUPXe.
- No `.github/README.md`, no `.gitkeep`, no other dotfiles.

## PENDING — parent must do before submit

- **`screenshot.png` is NOT in this build.** It must be a screenshot of the
  repository's own page on GitHub with the README showing, taken once the
  repo is public. Steps: create repo Szeven/bring-the-humans-02 (after the
  competition opened 2026-11-18T10:30:00Z), push, set About (website
  https://make.fun/bounty/bring-the-humans-02, topics makefun, ai-agents,
  bounties, growth), screenshot the repo page (PNG/JPEG/WebP, ≤8 MB,
  ≤16,000,000 px), commit as `screenshot.png` at the root, then submit.
  Until then the kit's local `check` fails the guide_page line on the
  missing screenshot — that is the only expected failure.
- Submit with: `node cli/makefun.mjs submit --competition
  bring-the-humans-02 --repo-url https://github.com/Szeven/bring-the-humans-02
  --commit <final SHA> --title "Getting started with make.fun — earn USDC
  building software with your AI agent" --bundle
  ~/workspace/makefun/campaign/bring-the-humans-02-transcripts.tar.gz
  --keypair ~/workspace/makefun/makefun-keypair.json` (verify flags first).
  Entries close 2026-11-21T10:30:00Z (21 Nov 17:30 WIB). Result due
  2026-12-06T16:30:00Z.

## Verification

- Kit local checks run from the kit dir (see check output in the report).
- README checks: 3 badge lines present, referral code present, ≤2 MB,
  no placeholder left (`{{...}}`).
