# Enosys Loans — Adversarial Due Diligence Report

**Report Date:** 2026-03-26
**Protocol:** Enosys Loans (CDP stablecoin)
**Chain:** Flare Network (also Songbird Canary Network)
**Category:** Liquity V2 Fork / CDP / Decentralized Stablecoin
**Researcher Stance:** Guilty until proven innocent

---

## 1. EXECUTIVE SUMMARY

**Verdict:** MEDIUM-HIGH RISK — Proceed with significant caution and limited position sizing.

**Confidence Level:** Medium (limited on-chain tool access; DeFiLlama and Flare Explorer blocked multiple queries)

Enosys Loans is a Liquity V2 fork deployed on Flare Network, launched December 11, 2025, enabling XRP holders to mint an overcollateralized stablecoin (CDP) using FXRP and wFLR as collateral. The project has genuine longevity — it predates this product as FLR Finance (2021) — and two audits were conducted. However, several structural concerns elevate risk above what the marketing narrative implies: the team is fully anonymous with no verifiable individual identities, the audit that's been most publicized (Coinspect) is NOT publicly available in Coinspect's publications repository, the contracts were made upgradeable in a deliberate departure from Liquity V2's core security design, and the Flare ecosystem is immature with at least one comparable protocol (MoreMarkets) having already shut down.

### Top 3 Risks
1. **Fully anonymous, unverifiable team** — No individual founder names are publicly disclosed. The organization holds no accountability anchors (no institutional backing, no Nasdaq-listed affiliates, no prior acquisition history).
2. **Upgradeable contracts with mutable admin parameters** — Enosys deliberately broke from Liquity V2's immutable architecture. The protocol admin can change core parameters at runtime. Multisig configuration and timelock duration are NOT publicly disclosed.
3. **Coinspect audit not publicly available** — Despite being the first and presumably most comprehensive audit, the Coinspect report for Enosys Loans does not appear in Coinspect's public publications GitHub repository. The actual security posture of the initial codebase cannot be independently verified.

### Top 3 Positive Signals
1. **Long operational history** — FLR Finance / Enosys has been building on Flare since 2021. They survived the bear market and a full rebrand; serial opportunists rarely maintain 5+ year commitments.
2. **Dedaub audit publicly available and findings were addressed** — All 4 HIGH and 3 MEDIUM severity issues from Dedaub's October 2025 audit were resolved. Dedaub is a credible, independent audit firm.
3. **Liquity V2 as base code** — Forking from one of the most rigorously audited and battle-tested CDP protocols in DeFi provides a strong security foundation, even with modifications.

---

## 2. TEAM ASSESSMENT

### Identity Status: ANONYMOUS — No verifiable individual founders

**Official Claim (UNVERIFIED):**
Enosys describes itself as built by "an independent team of globally based developers." The organization's Twitter profile describes them as "from the creators of @FlareScan and @DeFiOracles."

From a 2021 post, the team explicitly stated: *"We will remain anonymous through this pursuit, but at any point in time, a team member is free to reveal themselves."* — Source: FLR Finance Medium (2021)

**What This Means:**
As of March 2026, no core team members are publicly identified by name. The anonymity policy appears intentional and has persisted for 5+ years.

---

### Named Individuals — FFLabs Research Affiliate (Unverified as core team)

In 2021, FLR Finance introduced "FFLabs," a research arm. The following individuals were associated with FFLabs — **these are research lab contributors, not confirmed operators of the protocol:**

| Name | Claimed Background | Verifiability |
|---|---|---|
| Dr. Dionysis Zindros | Postdoctoral researcher at Stanford University, blockchain researcher | **PARTIALLY VERIFIABLE** — Academic blockchain researcher by this name exists in academic literature |
| Stavros | CS developer, Thessaloniki; worked on Silent Phone (Phil Zimmermann) and DFINITY Internet Computer | **PARTIALLY VERIFIABLE** — Silent Phone and DFINITY are real projects; independent employment verification not possible |
| Themis Papameletiou | Software engineer, Athens; Google and ESA internships | **UNVERIFIABLE** — Cannot independently confirm internships |

**Critical Gap:** These individuals were introduced in 2021 as research contributors. Their current role in Enosys Loans (if any) is not documented. The core protocol team building and deploying Enosys Loans remains unnamed.

---

### GitHub Analysis

**Organization:** [github.com/flrfinance](https://github.com/flrfinance)

- Organization has **0 publicly listed members** — "You must be a member to see who's a part of this organization"
- Public repositories include: `smart-contracts`, `flare-loans`, `bridge-contracts`, `bold` (fork of Liquity), `price-feed-ftso-connector`
- `bold` repo is a fork of the Liquity V2 monorepo — confirms the Liquity V2 fork basis
- `flare-loans` has only 4 stars and 1 fork — minimal external developer engagement
- Some repositories appear to be forks of unrelated projects (artblocks-contracts, safe-apps-sdk) — unclear relevance, possible cosmetic padding
- **No commit history quality analysis possible** — member anonymity prevents attribution of commits to verifiable individuals
- **Red flag:** Commit activity graphs returned load errors during research — freshness unknown

**What Could NOT Be Verified:**
- Who actually writes the code
- Whether the same individuals have contributed to known failed or fraudulent projects
- Code quality and patterns in the loans-specific contracts

---

### FlareScan Claim — PARTIALLY MISLEADING

**Official Claim:** Enosys Twitter bio states "from the creators of @FlareScan."

**Finding:** There are TWO distinct FlareScan products:
1. An early testnet block explorer built by FLR Finance for the Coston Test Network (~2020–2021) — the Enosys team's claim is valid for this early product.
2. The current, official flarescan.com — built by **Avascan/Routescan**, launched October 2023, in partnership with Flare Network. Key person: Giacomo Barbieri (Operations Lead at Avascan). **This is an entirely different team with no connection to Enosys.**

**Assessment:** The "creators of FlareScan" claim is a **half-truth used as a credibility signal**. The current flarescan.com — the product most users would recognize — was not built by Enosys. The original early-testnet explorer was, but it no longer exists as an active product.

---

### Historical Project Track Record (FLR Finance / Enosys)

**2021:** FLR Finance launches on Songbird with EXFI token.
**Key incidents:**
- Airdrop "misfire" — Flare Foundation's inclusion in snapshot increased the circulating SGB pool from 9.5B to 15.7B, meaning the Flare Foundation received ~16M EXFI. Community uproar. Team issued post-mortem but characterized the originally announced ratio as "an estimate."
- Repeated roadmap delays and missed delivery milestones — documented frustration in community.
- Promised audits from Halborn, TrailOfBits, and CertiK for the 2022 Flare mainnet launch — current status of these reports not verifiable.

**2023:** Rebranded to Ēnosys.
**December 2025:** Enosys Loans launched.

**Assessment:** The team has a real multi-year operational history, which is a positive signal compared to anonymous teams with no prior digital footprint. However, the history includes a significant airdrop controversy and delayed deliverables — consistent with an earnest but sometimes over-promising early DeFi team rather than calculated malicious actors.

---

## 3. THIRD-PARTY CONSENSUS

### Independent Analyst Coverage

**Coverage depth: LOW**

- No coverage found from The Defiant, Rekt News, or DL News specifically analyzing Enosys Loans' risk profile.
- Coverage is dominated by press-release style articles from Coinpedia, CoinCentral, EconoTimes, FinanceMagnates — these aggregate project claims without independent analysis.
- Markets Gone Wild (September 2025) published a structural analysis of the Liquity V2 fork design — the most substantive independent piece found, but still pre-launch and not adversarial.
- No LlamaRisk assessment found.
- No Code4rena or Sherlock competitive audit found.

**Janus Honest Answers (Substack)** — an independent Flare ecosystem analyst — published a broader analysis of Flare DeFi risk that directly mentions: *"Protocols you use today might not exist tomorrow. That's not FUD — that's reality."* This includes noting that **MoreMarkets.xyz, a lending protocol on Flare, shut down in December 2025** — the same month Enosys Loans launched.

### Audit Assessment

#### Dedaub Audit (October 2025) — PUBLICLY AVAILABLE ✓
Source: [dedaub.com/audits/flare-finance/enosys-october-20-2025](https://dedaub.com/audits/flare-finance/enosys-october-20-2025/)

This was a **diff audit** — focused only on changes from the Liquity V2 upstream codebase.

| Severity | Count | Status |
|---|---|---|
| Critical | 0 | N/A |
| High | 4 | All Resolved |
| Medium | 3 | All Resolved |
| Low | 7 | Mix |
| Advisory | 8 | Mix |

**Selected HIGH findings:**
- **H1 (Stake Scaling Math Error):** `_updateStakeAndTotalStakes` subtracts `oldStake` at wrong scale, corrupting total stakes — potential system instability.
- **H3 (WETH Approval Rotation Risk):** Since core contract addresses are now mutable, cached approval grants become stale — creates refund failures. **(Root cause: upgradeability)**
- **H4 (SortedTroves Registry Drift):** Core functions reject legitimate callers after address rotation, freezing list maintenance. **(Root cause: upgradeability)**

**Dedaub's Structural Warning (verbatim):**
> *"Enosys makes significant changes to the LiquityV2 architecture: main protocol contracts are now upgradeable, and many previously constant protocol parameters are modifiable at runtime by the protocol admin. While these changes introduce centralization to allow adaptation on a relatively young network, they also introduced problematic behavior not previously possible in LiquityV2."*
>
> *"We strongly recommend a follow-up review to reassess the protocol's security."*
>
> *"We recommend re-evaluating the necessity of each deviation from upstream and minimizing changes where possible."*

#### Coinspect Audit (Pre-launch, date unconfirmed) — NOT PUBLICLY AVAILABLE ⚠️
- Enosys claims a completed Coinspect audit, referenced in multiple official sources.
- **Coinspect's public publications repository (github.com/coinspect/publications) contains NO Enosys report.**
- No PDF link for the Coinspect Enosys audit was found anywhere in public search.
- Coinspect's published Flare-ecosystem work consists of: the FAssets Core Vault audit (for Flare Network itself, April 2025) — not for Enosys.
- **This audit cannot be independently verified or read by the public.**

Note: Enosys's website states "both audits and the code are publicly available" — this claim appears to be false for the Coinspect audit as of the research date.

### Community Sentiment

**Assessment: EXTREMELY LOW VOLUME — Cannot determine genuine sentiment**

- No Reddit threads found on r/FlareNetworks, r/DeFi, r/CryptoCurrency
- No site:reddit.com results returned for "Enosys" or "FLR Finance"
- Twitter/X activity exists (@enosys_global) but no adversarial commentary found from non-affiliated accounts
- Flare DeFi community appears very small — ecosystem described as "early stage" by independent analysts
- No Discord commentary from competing projects found
- **Absence of criticism is NOT evidence of safety** — it reflects an extremely small user base with limited external analyst interest

---

## 4. ON-CHAIN FINDINGS

### Identified Contract Addresses (Flare Network)

| Contract | Address | Verified? |
|---|---|---|
| CDP Token (Enosys Loans) | `0x6cd3a5ba46fa254d4d2e3c2b37350ae337e94a0f` | Not confirmed — Flare Explorer returned JS-only pages |
| eUSDT Stablecoin | `0x96b41289d90444b8add57e6f265db5ae8651df29` | Not confirmed |
| APS Governance Token | `0xfF56Eb5b1a7FAa972291117E5E9565dA29bc808d` | Not confirmed |
| DEX Liquidity Contract | `0x28b70f6Ed97429E40FE9a9CD3EB8E86BCBA11dd4` | Not confirmed (403 error) |

**Limitation:** Flare Explorer and Flarescan both failed to return readable contract data during this research session (JS-rendered pages, 403 errors). On-chain verification is incomplete.

### Upgradeability Risk (CONFIRMED — HIGH)

Confirmed by Dedaub audit: Enosys deliberately introduced **upgradeable contract architecture**, diverging from Liquity V2's core immutability principle.

What this enables:
- Admin can change core protocol parameters after deployment without timelock (if no timelock is enforced)
- Admin can upgrade contract logic entirely
- WETH approval patterns can become stale after address rotation
- SortedTroves auth pointers can drift from registry after rotation

**What is NOT publicly disclosed:**
- Who controls the admin/owner role on deployed contracts
- Whether a multisig is used and the signing threshold (e.g., 3-of-5)
- Whether a timelock controller is deployed and its delay period
- The specific wallet addresses of protocol administrators

**Verdict:** Centralization risk is REAL and has been documented by Dedaub. The degree of risk depends entirely on the admin governance structure — which is opaque.

### Token Distribution Analysis (HLN Governance Token)

| Allocation | % | TGE Unlock | Vesting |
|---|---|---|---|
| Community Airdrop | 20% | 27.5% | 12 months |
| APY Cloud | 31.93% | 0% | 36 months |
| Foundation | 17% | 0% | 120 months |
| Investors | 15% | 0% | 36 months |
| Operating Expenses | 15% | 20% | 12 months |
| DFLR Early Airdrop | 0.67% | 100% | Immediate |
| EXFI Stakers | 0.40% | 100% | Immediate |

**Assessment:**
- Foundation has 10-year (120 month) vesting — this is unusually long and could be read as either a genuine commitment or a mechanism to lock tokens out of circulating supply indefinitely.
- Operating expenses: 15% with 20% at TGE creates a sell pressure vector from day 1.
- No independent verification that vesting schedules are enforced on-chain via smart contracts (vs. discretionary).
- FDV ~$9.95M (as of research date) — extremely small, suggesting limited market interest in the governance token.

### TVL Assessment

- **Enosys Loans at launch (December 2025):** ~$3.5M, approximately at the mint cap ($4M FXRP / $1M wFLR).
- **Enosys overall suite:** ~$330K annual revenue reported on DeFiLlama.
- **Current TVL:** Unable to confirm — DeFiLlama returned 403. Initial mint caps suggest the protocol rapidly hit its ceiling.
- **Ecosystem context:** Flare Network has ~$236M TVL total (per Bitget News, citing Flare). Enosys Loans represents a small but meaningful slice.

### Oracle Risk

- Enosys Loans uses Flare's native FTSO (Flare Time Series Oracle) for collateral pricing.
- FTSO aggregates from independent signal providers — described as decentralized and manipulation-resistant.
- The oracle infrastructure is Flare's responsibility, not Enosys's — this is a positive design choice that offloads a major attack surface.
- **Risk note:** Dedaub identified **M2 (Price Feed False Positives)** — `lastGoodPrice` fallback returning 0 causes false-positive liquidation signals. While marked as resolved, this was a non-trivial pricing feed bug.

---

## 5. RED FLAGS REGISTER

| # | Flag | Severity | Evidence | Why It Matters |
|---|---|---|---|---|
| 1 | **Fully anonymous team, no verifiable individuals** | HIGH | No names, no LinkedIn, no public GitHub members, 5-year anonymity policy | Cannot assess founder incentives, prior history with failed/fraudulent projects, or personal accountability. People rug, not protocols. |
| 2 | **Coinspect audit not publicly available** | HIGH | Searched coinspect/publications (GitHub) — no Enosys report. No PDF link found anywhere. Official claim that "both audits are publicly available" appears false. | Claimed first audit cannot be independently verified. Users cannot assess what security issues existed in pre-launch code. |
| 3 | **Upgradeable contracts departing from Liquity V2 immutability** | HIGH | Dedaub audit (confirmed): "main protocol contracts are now upgradeable... many previously constant parameters are modifiable at runtime by the protocol admin" | Admin can arbitrarily change protocol behavior. If admin key is compromised or acts maliciously, funds at risk. This is the single biggest structural departure from the security model Enosys is marketing. |
| 4 | **Admin governance structure not publicly disclosed** | HIGH | No documentation found for multisig configuration, timelock duration, or admin wallet addresses | Cannot assess who controls the upgrade mechanism. A single EOA with upgrade rights is a catastrophic centralization risk. |
| 5 | **FlareScan claim is misleading** | MEDIUM | Official flarescan.com built by Avascan (2023), not Enosys. Enosys built an early testnet explorer in 2020-2021. | This credential is used as a trust signal. Using it to imply credit for the widely known current product is deceptive marketing. |
| 6 | **Ecosystem immaturity — MoreMarkets shut down in Dec 2025** | MEDIUM | Janus Honest Answers Substack (independent analyst): "protocols you use today might not exist tomorrow" — cited MoreMarkets shutdown | Flare DeFi is small. Comparable protocol shut down the same month Enosys Loans launched. Economic sustainability for Flare DeFi protocols is unproven. |
| 7 | **Historical airdrop misfire and community controversy** | MEDIUM | FLR Finance Medium (2021): Flare Foundation received ~16M EXFI due to expanded snapshot. Team characterized pre-announced ratio as "an estimate." | Pattern of overpromising and post-hoc reframing when things go wrong. |
| 8 | **No independent analytical coverage** | MEDIUM | No LlamaRisk, Rekt, The Defiant, or DL News analysis found | Absence of scrutiny could mask undiscovered risks. It also indicates small, insular user base — liquidity risk in crisis scenarios. |
| 9 | **GitHub has zero public members** | MEDIUM | github.com/flrfinance: "This organization has no public members." | Cannot attribute commits, verify code authorship, or assess individual contributor backgrounds. |
| 10 | **Dedaub recommended follow-up review that has not been confirmed** | MEDIUM | Dedaub verbatim: "strongly recommend a follow-up review to reassess the protocol's security." No third audit announced or confirmed publicly. | Critical open recommendation from auditors not resolved as of research date. |
| 11 | **Mint caps create artificial early TVL signal** | LOW | Initial caps: $4M FXRP, $1M wFLR. TVL reached $3.5M "overnight." | The $3.5M TVL is close to the hard mint cap — TVL growth was capacity-constrained, not demand-driven. The headline figure is not a free-market signal. |
| 12 | **HLN token low FDV ($9.95M)** | LOW | CoinGecko/CryptoRank data | Suggests limited external investor conviction in the governance token despite years of operation. |
| 13 | **Promises of expanded collateral (stXRP, FBTC) remain undelivered roadmap items** | LOW | Official communications: "plans to expand" — no confirmed delivery dates | Consistent with historical pattern of forward-looking commitments without firm delivery. |

---

## 6. UNRESOLVED QUESTIONS

The following could NOT be determined and represent critical gaps in this assessment:

1. **Who controls the admin/upgrade keys?**
   The most important unanswered question. Is it a multisig? How many signers? Who are they? Is there a timelock? This directly determines the real-world severity of the upgradeability risk.

2. **Where is the Coinspect audit?**
   The first audit was done pre-launch by Coinspect. It is not in Coinspect's publications repository. Either it was never published, was shared privately, or the claim is fabricated. None of these scenarios are reassuring.

3. **Has Dedaub's recommended follow-up audit been commissioned?**
   Dedaub explicitly and strongly recommended a third review focused on the upgradeability changes. No announcement of this was found.

4. **What is the current TVL post-mint-cap expansion?**
   DeFiLlama's Enosys Loans page was inaccessible (403). The protocol launched with tight mint caps — whether caps have been raised and whether TVL has grown organically is unknown.

5. **What happened to the original Halborn/TrailOfBits/CertiK audits claimed for the 2022 launch?**
   Three major audit firms were named in 2021-2022 announcements. None of these reports are publicly findable. Their findings and remediation status are unknown.

6. **Are the vesting schedules enforced on-chain?**
   HLN tokenomics describe multi-year vesting for investors and foundation allocations. Whether these are enforced via smart contracts (immutable) or are discretionary agreements is unknown.

7. **What is the actual on-chain composition of TVL?**
   Due to block explorer access issues, the actual breakdown of collateral types and whale concentration in the stability pool could not be verified.

---

## APPENDIX: SOURCES

### Primary Research Sources
- Dedaub Audit Report: https://dedaub.com/audits/flare-finance/enosys-october-20-2025/
- Enosys Medium (Official): https://enosys.medium.com/introducing-enosys-loans-8f7dfeff3056
- Flare Network Announcement: https://flare.network/news/enosys-loans-xrp-backed-stablecoin-flare
- Markets Gone Wild (Pre-launch analysis): https://marketsgonewild.com/crypto-news/2025/09/19/exploring-the-new-wave-enosis-xrp-backed-stablecoin-flare-a-look-into-liquity-v2-fork/
- DeFiLlama Enosys: https://defillama.com/protocol/enosys
- Coinspect Publications (GitHub): https://github.com/coinspect/publications
- FLR Finance GitHub Org: https://github.com/flrfinance
- Flare Builders (Giacomo Barbieri, FlareScan): https://www.flare.builders/blog/giacomo-barbieri-flarescan
- Janus Honest Answers (Substack, independent): https://janusthewatcher.substack.com/p/janus-honest-answers-how-to-put-flr

### Official Claims Treated as Marketing Material
- Enosys Global Website: https://enosys.global/
- Enosys Tokenomics (Medium): https://enosys.medium.com/introduction-2bee6d0b14cb
- FLR Finance rebrand announcement: https://enosys.medium.com/flr-finance-enosys-abd2324445bb

---

*Research conducted under adversarial methodology. Every factual claim marked by its source rank (on-chain > third-party > community > digital footprint > official communications). Unverified claims are explicitly labeled. Absence of evidence is not treated as evidence of absence.*
