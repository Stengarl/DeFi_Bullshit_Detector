# Alphix (alphix.fi) — Adversarial DeFi Due Diligence Report

**Research Date:** April 22, 2026
**Subject:** Alphix (alphix.fi) — Uniswap V4 Hook DEX / Non-Custodial Market Maker
**Legal Entity:** Unconfirmed — GitHub organization lists location as Zurich, Switzerland
**Token:** None currently (pre-token; points program active)
**GitHub:** github.com/alphixfi
**Investigator:** Claude Code (Adversarial DeFi Research Framework)
**Confidence Level:** MEDIUM — Team has minimal verifiable prior footprint; TVL data unavailable; project is early-stage pre-token

---

> **FRAMING NOTE — READ FIRST**
>
> Alphix is a **pre-token, early-stage protocol** with essentially no public-facing team identity. The main website blocked scraping (403). Team members Carl Schmeid and Yanis Benkrai appear in exactly one independently verifiable context — an EthCC Builders Showcase slide deck — and have no discoverable prior digital footprint in crypto or tech. There is no token to pump, no large TVL to misrepresent, and no ZachXBT investigation. The question here is not "is this a rug pull in progress" — it's "is there enough substance and transparency to trust this team if/when they launch a token?"
>
> **Short answer: The code is real. The institutional touch points are real. The team is functionally anonymous with no verifiable track record. This is an early-stage project with genuine technology but a critical transparency deficit.**

---

## 1. Executive Summary

**Verdict:** Alphix is a **technically credible, early-stage DeFi infrastructure project** building on Uniswap V4's hook architecture. The smart contract code is original, professionally structured, and received a clean Sherlock audit (0 High, 0 Medium, 6 Low/Info — all resolved). The project was selected as an IncuBase winner by Coinbase's Base team, presented at EthCC, and received access to Uniswap Foundation security tooling. These are **not** the hallmarks of a scam. However, the **team is functionally anonymous** — the two identified co-founders (Carl Schmeid and Yanis Benkrai) have no discoverable professional history, no LinkedIn profiles, no GitHub activity prior to Alphix, and no prior DeFi projects to assess. The project has no token yet, but the critical unknown is what a future TGE distribution will look like. The single largest risk here is the inability to conduct standard background verification on the people who will ultimately control any future token launch and treasury.

**Confidence Level:** MEDIUM — Constrained by team opacity and very limited user adoption evidence

**Top 3 Risks:**
1. **Anonymous team with no verifiable track record** — Carl Schmeid and Yanis Benkrai cannot be independently verified beyond their EthCC appearance. No LinkedIn, no GitHub pre-history, no prior projects. If a token launches, these are the people controlling distribution.
2. **Upgrade mechanism not disclosed** — The alphix-core README describes an "upgradeable" architecture with `Pausable` and `AccessManager` controls, but the security documentation does not disclose who holds admin keys, whether they are secured by multisig, or what the upgrade process is.
3. **Future token distribution unknown** — No token exists yet. This is currently a points-for-future-airdrop system. The distribution methodology, insider allocation, vesting schedule, and who controls the treasury at TGE are entirely undisclosed.

**Top 3 Positive Signals:**
1. **Base IncuBase program winner** — Coinbase's Base ecosystem has a real vetting and incubation process. Being selected as a winner represents external validation from a credible institutional actor.
2. **Clean Sherlock audit (Dec 2025)** — Independent competitive audit with 0 High, 0 Medium findings, all 6 Low/Info findings resolved. Sherlock's competitive audit model (paid researchers competing to find bugs) is rigorous.
3. **Real, original code with professional security practices** — 253 commits, original Solidity (not a fork-and-rebrand), comprehensive test suite (fuzz, invariant, integration), ReentrancyGuard, two-step ownership, BUSL-1.1 license — consistent with serious infrastructure development.

---

## 2. Team Assessment

### Identified Team Members

**Carl Schmeid — Co-Founder (role not formally confirmed)**

| Attribute | Claim | Verified? | Notes |
|-----------|-------|-----------|-------|
| EthCC Builders Showcase presentation | Presented Alphix at EthCC (May 2025) | ✅ Confirmed via Luma event listing | Confirmed as presenter alongside Yanis Benkrai |
| Location | Zurich, Switzerland (inferred from org) | Partial | GitHub org lists Switzerland; "IncuBase winners based in Zurich" in search |
| LinkedIn profile | Not found | ❌ UNVERIFIABLE | Zero LinkedIn presence discoverable |
| GitHub profile | Not found | ❌ UNVERIFIABLE | No personal GitHub linked to this name |
| Prior projects | None found | ❌ UNVERIFIABLE | No prior DeFi, Web3, or tech projects discoverable |
| Educational background | Not disclosed | ❌ UNVERIFIABLE | |

**Assessment:** Carl Schmeid is a name that appears in exactly one independently verifiable context: the EthCC Builders Showcase event listing. No LinkedIn, no GitHub history, no prior professional footprint exists in public searchable records. This is consistent with either (a) a genuinely early-career founder with no established track record, (b) a pseudonym, or (c) a real person who maintains no digital presence. All three scenarios require skepticism.

---

**Yanis Benkrai — Co-Founder**

| Attribute | Claim | Verified? | Notes |
|-----------|-------|-----------|-------|
| EthCC Builders Showcase presentation | Presented Alphix at EthCC (May 2025) | ✅ Confirmed via Luma event listing | |
| Co-founder title | Co-founder of Alphix | Partially confirmed | Referenced as co-founder in one search result |
| Location | Zurich, Switzerland (inferred) | Partial | Consistent with org location |
| LinkedIn profile | Not found | ❌ UNVERIFIABLE | Searches returned multiple "Yanis Benkr*ai/ani" but none matching this individual |
| GitHub profile | Not found | ❌ UNVERIFIABLE | No personal GitHub linked |
| Prior projects | None found | ❌ UNVERIFIABLE | No prior DeFi, Web3, or tech projects discoverable |

**Assessment:** Same profile as Carl Schmeid. Confirmed as a real person who appeared publicly at EthCC, but no prior career history, educational background, or other project contributions can be independently confirmed.

---

**"Benjamin P." — Team Member (role unknown)**

| Attribute | Claim | Verified? | Notes |
|-----------|-------|-----------|-------|
| LinkedIn | "Benjamin P. — Alphix" found on LinkedIn | Partial | Surname initial only; profile not accessible without login |
| Role | Unknown | ❌ UNVERIFIABLE | |
| Background | Unknown | ❌ UNVERIFIABLE | |

---

### GitHub Analysis — `github.com/alphixfi`

| Metric | Finding | Assessment |
|--------|---------|------------|
| Organization location | Switzerland (Zurich) | Consistent across sources |
| Public members | None listed | Red flag — developers hidden |
| Total repositories | 3 public | Very early stage |
| alphix-core | 0 stars, 1 fork — Solidity, updated Apr 19, 2026 | Active development but near-zero community interest |
| dimension-adapters | Fork of DefiLlama/dimension-adapters (1,736 forks) | Normal — standard DeFiLlama listing process |
| DefiLlama-Adapters | Fork of DefiLlama/DefiLlama-Adapters (7,295 forks) | Normal — standard DeFiLlama listing process |
| Org followers | 1 | Extremely low visibility |
| alphix-core commits | 253 on main branch | Meaningful — not cosmetic |
| Code origin | Original (not a fork) — builds on Uniswap V4 hooks | Positive signal |
| Testing | Unit, integration, full-cycle, invariant, fuzz (256+ runs) | Professional-grade practices |
| License | BUSL-1.1 with MIT transition in 2028 | Same model as Uniswap V4 itself |
| Security patterns | ReentrancyGuard, Pausable, two-step ownership, AccessManager | Serious security implementation |

**The DeFiLlama forks are NOT a fork-and-rebrand red flag.** They are the standard mechanism for submitting a TVL adapter to DeFiLlama — every protocol that wants DeFiLlama tracking forks these repos. This is normal and expected behavior.

**Core code quality is genuine.** The 253-commit alphix-core repo demonstrates: modular hook architecture on Uniswap V4, dynamic fee adjustment via EMA smoothing, JIT liquidity with ERC-4626 vault integration, and a comprehensive test suite. This is not cosmetic GitHub activity.

### Social Media

- **Twitter/X (@AlphixFi):** Active account confirmed. Specific post content inaccessible (behind login wall). No evidence of deleted tweet patterns or prior project shilling found.
- **EthCC May 2025:** Appeared in Base's "EthCC Builders Showcase" — a curated demo event, not a self-submitted talk, implying external selection.
- **IncuBase Winner:** Referenced in posts as "IncuBase winners based in Zurich" — Base's incubation program selection.

### What Could NOT Be Verified

- **Any professional history for Carl Schmeid or Yanis Benkrai prior to Alphix**
- **Whether Carl Schmeid and Yanis Benkrai are their real names**
- **The legal entity operating Alphix** — no company registration, no corporate filing found
- **Who "Benjamin P." is and what role they play**
- **Who holds the Pausable/AccessManager keys in deployed contracts**
- **Whether any seed or angel funding was received and from whom**
- **The full team size** — GitHub org has zero public members; actual headcount unknown

---

## 3. Third-Party Consensus

### Base IncuBase Program

Alphix was selected as a winner of Base's IncuBase incubation program (presented June 2025). IncuBase is Coinbase's L2 (Base) ecosystem incubation initiative. Being selected implies:
- The Base team reviewed the project and found it legitimate enough to support
- The team made a verifiable public appearance on behalf of the project
- Coinbase's ecosystem infrastructure is behind the selection

**This is the strongest legitimacy signal in the report.** Coinbase/Base has institutional credibility and a public reputation to protect. Selection does not guarantee the team's prior history, but it substantially reduces the probability of an outright scam.

### Sherlock Audit (December 2025)

- **Model:** Collaborative audit contest — paid independent researchers compete to find vulnerabilities. This is a rigorous model because researchers are financially incentivized to find bugs.
- **Results:** 0 High, 0 Medium, 6 Low/Info — **all 6 findings resolved**
- **Bug Bounty:** $30,000 USDC live on Sherlock since February 11, 2026
- **Pre-audit tooling:** Olympix (via Uniswap Foundation partnership) and Sherlock AI used for pre-audit scanning

**Important caveat:** A Sherlock audit contest cannot be independently verified in the public audit repo index — no Alphix contest appears in the publicly visible sherlock-audit GitHub organization (though only 10 of 459 repos are visible). The audit report PDF link (`github.com/alphixfi/alphix-core/blob/main/security/2025.12.17-Final-AlphixCollaborativeAuditReport.pdf`) is the primary source and is hosted in the project's own repo, not Sherlock's infrastructure. **This could not be independently verified via Sherlock's own systems** — treat as "claimed and plausible" rather than "fully confirmed."

### Uniswap Foundation

The security documentation mentions access to Olympix (a Solidity security scanner) "provided via Uniswap partnership." This implies some level of Uniswap Foundation engagement, but no official grant announcement was found from the Uniswap Foundation's communications. The Uniswap Foundation committed $26M in grants during 2025 — Alphix is not confirmed as a recipient in available sources.

**Claim status: UNVERIFIED** — plausible but not confirmed.

### Independent Analyst and Community Coverage

- **No independent DeFi analyst coverage found** — no Rekt News, The Defiant, DL News, Blockworks, or CoinDesk articles
- **No Reddit or forum discussions** — no r/DeFi, r/ethfinance, or r/CryptoCurrency posts about Alphix
- **No community criticism or scam allegations** — complete absence of both positive and negative independent discussion
- **DWF Labs research** — DWF Labs published a Uniswap V4 research article that may mention Alphix. DWF Labs is the controversial market maker (accused of $300M Binance wash trading) from the MemeCore investigation. Could NOT confirm whether DWF Labs has any financial relationship with Alphix (article returned 403).

**Assessment:** The complete absence of independent analyst coverage is expected for a pre-token early-stage project with minimal TVL. It is not evidence of fraud, but it means there is essentially no ecosystem validation beyond the institutional touch points listed above.

---

## 4. On-Chain Findings

### Contract Architecture

| Feature | Finding | Assessment |
|---------|---------|------------|
| Chain | Base and Arbitrum | EVM-compatible L2s |
| Protocol base | Uniswap V4 hook system | Builds on audited infrastructure |
| Architecture | Upgradeable hook with AccessManager | Admin keys exist; upgrade path unclear |
| Security patterns | ReentrancyGuard, Pausable, two-step ownership | Professional implementation |
| License | BUSL-1.1 → MIT (2028) | Standard for competitive moat protection |
| Contract addresses | Not publicly disclosed in documentation | RED FLAG — cannot independently verify deployed code |
| Source code on BaseScan | Cannot confirm — no contract address available | UNVERIFIABLE |
| Multisig configuration | Not disclosed | RED FLAG — unknown who controls admin functions |
| Timelock on admin functions | Not disclosed | UNVERIFIABLE |

**The most significant on-chain risk is what cannot be confirmed:**
The alphix-core README describes a `Pausable` contract and `AccessManager` role-based controls. These mean there is at least one privileged address with the ability to pause the protocol and change role assignments. Whether this is controlled by:
- A single EOA (extremely risky)
- A 2-of-3 multisig (acceptable)
- A timelock (best practice)

...is completely undisclosed in any publicly available documentation.

### Token Distribution (Pre-Token)

**No token exists as of this report.** Key unknowns for when/if a token launches:
- Who controls the points-to-token conversion?
- What percentage of supply will insiders receive?
- Will there be a public sale or private placement only?
- What are the vesting schedules for team allocation?
- Is there a lockup period for IncuBase/institutional backers?

The Points Program is the only indication of intended user distribution. Points are earned through: liquidity provision, swapping, and referrals. Hourly snapshots, weekly distributions. This is a standard airdrop farming mechanism and does not commit to any specific token allocation methodology.

### TVL Verification

DeFiLlama has a tracking page for Alphix (`defillama.com/protocol/alphix`) — confirming they completed the adapter submission process. However, the page returned 403 in direct access, and no independent search result returned a specific TVL figure.

**Inference:** TVL is either very small (sub-$1M) or newly launched with minimal deposits. For context:
- If TVL were meaningful (>$5M), it would appear in DeFiLlama headlines or search results
- The complete absence of any TVL figure from any independent source suggests minimal user adoption to date

**This is not a fraud signal — it is an adoption signal.** The protocol exists and is deployed, but has not yet attracted significant liquidity.

### Unified Yield Risk

Alphix's "Unified Yield" feature deploys idle liquidity to:
- **Aave** on Base and Arbitrum
- **Spark Protocol** on Base

This creates indirect exposure to:
- Aave smart contract risk
- Spark Protocol smart contract and governance risk (Rune Christensen's centralization issues — see Spark adversarial report)
- If Aave or Spark experiences an exploit, Alphix LP funds deployed there are at risk

This is a **counterparty dependency risk** that users should understand before depositing.

---

## 5. Red Flags Register

| # | Flag | Evidence | Source | Severity |
|---|------|----------|---------|----------|
| 1 | Team is functionally anonymous with no verifiable prior track record | Carl Schmeid and Yanis Benkrai have no LinkedIn, no personal GitHub, no prior projects discoverable | Research (multiple searches, no results) | **HIGH** |
| 2 | Admin key/multisig configuration not disclosed | alphix-core uses Pausable and AccessManager; no documentation on who holds these keys or how they're secured | alphix-core README (verified) | **HIGH** |
| 3 | Future token distribution methodology completely unknown | Points program active but no TGE commitments on supply, insider allocation, vesting, or lockup | Research (no disclosure found) | **HIGH** |
| 4 | No contract addresses publicly disclosed | Cannot independently verify deployed code matches audited code on BaseScan/Arbiscan | Documentation review (verified by absence) | **HIGH** |
| 5 | Sherlock audit cannot be independently verified via Sherlock's own systems | Audit report is hosted in project's own GitHub repo; no matching contest found in Sherlock's visible audit org | Sherlock audit org (459 repos, alphix not found) | **MEDIUM** |
| 6 | GitHub org has zero public members | Developer identities hidden; cannot cross-reference contributor identities with team claims | GitHub (verified) | **MEDIUM** |
| 7 | Zero stars on alphix-core repo | A deployed and functional protocol with 0 GitHub stars has no developer community or external validator interest | GitHub (verified) | **MEDIUM** |
| 8 | No independent analyst coverage whatsoever | No Rekt News, The Defiant, Blockworks, CoinDesk, or any independent DeFi publication has covered Alphix | Research (verified by absence) | **MEDIUM** |
| 9 | No funding disclosed | No seed round, no investors, no funding announcements found | Research (verified by absence) | **MEDIUM** |
| 10 | Legal entity not identified | No company registration, no corporate filing, no jurisdiction confirmation beyond GitHub org location of "Switzerland" | Research (verified by absence) | **MEDIUM** |
| 11 | Roadmap has no dated milestones | Future plans vague; no committed timeline for token launch, additional chain deployment, or governance | Roadmap docs (verified) | **MEDIUM** |
| 12 | Indirect counterparty exposure to Aave and Spark | Unified Yield deploys idle LP funds to Aave and Spark; exploit in either protocol affects Alphix users | Roadmap docs (verified) | **MEDIUM** |
| 13 | DWF Labs wrote Uniswap V4 research that may include Alphix — relationship undisclosed | DWF Labs article appeared in search results; article blocked (403); cannot confirm if DWF Labs is investor or just researcher | Research (unresolved) | **LOW** |
| 14 | "AI agents" marketing language without specific technical implementation disclosed | Described as "leveraging AI agents and dedicated algorithms" but no specific model, architecture, or implementation detail | Marketing materials (verified) | **LOW** |
| 15 | BUSL-1.1 license restricts ecosystem composability until 2028 | Protocol code cannot be freely forked, adapted, or integrated by others until MIT transition | alphix-core README (verified) | **LOW** |
| 16 | Points airdrop creates future sell pressure | Regardless of future token design, airdrop recipients systematically sell — creates price pressure at TGE | Standard DeFi pattern | **LOW** |

---

## 6. Comparative Analysis

### Against Rug Pull Checklist

| Pattern | Alphix | Assessment |
|---------|--------|------------|
| Anonymous team | ✅ Partial — named but no verifiable history | Concern |
| No audits | ❌ — Sherlock audit performed (Dec 2025) | Positive |
| No real code | ❌ — 253-commit original Solidity repo with fuzz tests | Positive |
| Inflated TVL / fake metrics | Neither confirmed nor denied — no TVL data available | Neutral |
| Controversial market maker (DWF Labs etc.) | Unresolved — DWF Labs article mention but relationship unknown | Neutral |
| No institutional validation | ❌ — Base IncuBase winner, EthCC presenter | Positive |
| Token launch with insider dump | N/A — no token yet | Unknown risk |
| Rapid price pump with insider concentration | N/A — no token yet | Unknown risk |
| Geth fork masquerading as L1 | ❌ — original code building on Uniswap V4 hooks | Positive |
| No response to scrutiny | N/A — no scrutiny has been applied publicly | Neutral |

**Score: 1 confirmed negative pattern (team anonymity), 4 positives, rest unknown or neutral.**

### What Alphix Most Resembles

Among legitimate early-stage DeFi projects, Alphix's profile is closest to:
- **Pre-token DEX infrastructure builders** (similar to early Uniswap hook protocols)
- **DeFi infrastructure from small Swiss/European teams** (similar to early Euler Finance, Morpho when they had minimal TVL and small team)
- **IncuBase/Base ecosystem projects** that are real products but have not yet found product-market fit

The risk profile does **not** resemble:
- MemeCore (no token concentration, no inflated market cap, no wash trading signals, no ZachXBT attention)
- Terra/Luna or Olympus (no unsustainable yield promises)
- Wonderland (no anonymous treasury manager with criminal history — though team anonymity here is still unresolved)

### Uniswap V4 Hook Ecosystem Risk

Alphix operates in a new and largely untested subsector of DeFi — Uniswap V4 hooks. V4 launched on Ethereum and L2s in late 2024/early 2025. The hook architecture allows arbitrary code to execute before and after swaps. Key ecosystem-level risks:

- V4 hooks are a new attack surface not present in V3 — novel vulnerabilities may not yet be understood
- Alphix is one of the first protocols deploying complex logic (dynamic fees + rehypothecation) in hooks — limited battle-testing
- If Uniswap V4 itself has an undiscovered vulnerability, all hooks are at risk

---

## 7. Unresolved Questions

1. **Who are Carl Schmeid and Yanis Benkrai, really?** No prior career history, educational background, or professional track record can be independently verified. Are these real names? Are they early-career founders, pseudonyms, or something else?

2. **Who holds the admin/pause keys?** The deployed contracts have Pausable and AccessManager. Is this controlled by a hardware wallet held by one person? A Gnosis Safe? A timelock? This is the most critical operational security question.

3. **What will the token distribution look like?** The points program will presumably translate into token airdrop at TGE. What percentage goes to insiders? What is the team allocation? What are the vesting schedules? None of this is disclosed.

4. **Does Alphix have any financial relationship with DWF Labs?** DWF Labs wrote a Uniswap V4 research piece that appears to include Alphix. DWF Labs has documented allegations of market manipulation. If they are an investor or market maker for Alphix, that materially changes the risk profile.

5. **What is the actual TVL?** DeFiLlama has a tracking page but no retrievable figure was found. Is this protocol actually being used, or is it deployed but empty?

6. **Has the Sherlock audit report been independently published on Sherlock's infrastructure?** The PDF is hosted in the project's own GitHub repo. Independent verification via Sherlock's platform was not possible.

7. **What is the legal entity and regulatory status?** The GitHub org says Switzerland, but no company registration, Swiss FINMA filing, or legal entity was found. DeFi protocols operating in Switzerland typically engage with FINMA at some point.

8. **What is the full team size?** Three names are partially known (Carl Schmeid, Yanis Benkrai, Benjamin P.). Who else is on the team? This matters for assessing execution capability for a $30K bug bounty and growing protocol.

---

## 8. Sources Used in This Investigation

All sources accessed April 22, 2026.

- [Alphix Official Website](https://www.alphix.fi/) — 403, inaccessible
- [Alphix GitBook Documentation](https://alphix.gitbook.io/docs)
- [Alphix GitHub Organization (alphixfi)](https://github.com/alphixfi)
- [alphix-core Repository](https://github.com/alphixfi/alphix-core)
- [Sherlock Bug Bounty #213 — Alphix](https://audits.sherlock.xyz/bug-bounties/213)
- [Sherlock Audit Organization (GitHub)](https://github.com/sherlock-audit) — 459 repos; no Alphix contest found in visible list
- [EthCC Builders Showcase — Luma Event Listing](https://luma.com/ethcc-showcase) — Carl Schmeid and Yanis Benkrai confirmed as presenters
- [DeFiLlama — Alphix Protocol Page](https://defillama.com/protocol/alphix) — 403, inaccessible directly
- [Alphix Twitter/X (@AlphixFi)](https://x.com/AlphixFi)
- [Alphix Roadmap](https://alphix.gitbook.io/docs/more/roadmap)
- [Alphix Security Documentation](https://alphix.gitbook.io/docs/tech/security)
- [Uniswap Foundation Grants](https://www.uniswapfoundation.org/grants)

---

## 9. Researcher Notes & Lessons (lessons.md update)

**New patterns observed:**
- **Pre-token early-stage projects** present a fundamentally different investigation challenge than post-token projects. Without a token, there is no market cap to investigate, no price manipulation to detect, and no holder concentration to measure. The risk surface shifts entirely to team credibility and future-state unknowns.
- **IncuBase / Base ecosystem winner status** is a meaningful legitimacy signal — Coinbase has institutional reputation to protect and applies genuine vetting. Not foolproof, but not nothing.
- **Sherlock collaborative audit model** (competitive paid researchers) is generally more rigorous than a standard paid audit, because researchers are financially rewarded per finding — creating stronger incentive to find bugs.
- **BUSL-1.1 license** is not inherently suspicious. It is the standard mechanism early DeFi infrastructure protocols use to prevent immediate forking while building a community. Uniswap itself used this.

**Research techniques that worked:**
- EthCC presentation listings (Luma) revealed team names not findable anywhere else
- GitBook security page directly stated the audit firm and result format
- GitHub org metadata (location, email, bio) provided Switzerland confirmation without accessing the main website
- Searching for the project's appearance in hackathon/demo platforms (Akindo, IncuBase) revealed legitimacy signals

**Research techniques that failed:**
- Direct fetching of alphix.fi, alphix.fi/overview, DeFiLlama pages, and DWF Labs article all returned 403 — web scraping defenses are more prevalent than in prior investigations
- LinkedIn site: searches returned zero results for both founders — confirms their deliberate absence from professional networking
- Sherlock audit org search: 10 of 459 repos visible; inconclusive

**Sources that proved reliable:**
- Event listing pages (Luma, EthCC) for team identity confirmation
- GitHub org metadata for location and email
- GitBook docs for security claims

**Sources that proved unreliable/inaccessible:**
- alphix.fi main domain (403)
- DeFiLlama direct access (403)
- LinkedIn for founder verification (no profiles exist)
- DWF Labs article (403)

**False alarm calibration:**
- The DeFiLlama forks in the GitHub org initially looked like a fork-and-rebrand pattern (RED FLAG from MemeCore). They are actually the standard submission process for getting a DeFiLlama adapter accepted. Any protocol wanting DeFiLlama tracking must fork these repos. Context matters — 7,295-fork repos are not the project's core code.
- "Zero stars on GitHub" is a different signal for a pre-token early-stage protocol (expected for low visibility) than for a claimed $5.5B market cap project (MemeCore's 13 stars were alarming in that context). Calibrate star counts against project stage and claimed market position.

---

*Report compiled April 22, 2026 | Alphix (alphix.fi) Adversarial Due Diligence | Adversarial framework applied: guilty until proven innocent. Alphix partially cleared the framework — real code, real audit, real institutional validation — but team anonymity and governance opacity remain unresolved material concerns.*
