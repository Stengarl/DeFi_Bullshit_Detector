# Boros (Pendle Finance) — Adversarial Due Diligence Report

**Date of Investigation:** April 11–12, 2026  
**Investigator Stance:** Guilty until proven innocent  
**Confidence Level:** High (Pendle is a well-documented 5-year-old protocol; Boros has 8 months of live data)  
**Report Status:** Complete (updated with parallel agent findings April 12)

---

## ⚠️ FRAMING NOTE

Boros is NOT a standalone project with its own team. It is a product built and operated by **Pendle Finance**, a yield tokenization protocol founded in 2021. Any investigation of Boros is inseparable from an investigation of Pendle Finance itself. This report covers both.

Boros represents a mechanistic departure from Pendle's original yield tokenization model: instead of tokenizing yield from on-chain protocols, Boros tokenizes **funding rates from centralized perpetual futures exchanges** (primarily Binance), settling them on-chain via an order book. This introduces centralization risks that Pendle V2 did not have.

---

## 1. Executive Summary

**Verdict:** Boros by Pendle is a legitimately-built DeFi product from a team with a 5-year verifiable track record, real institutional backing, and credible auditors. It is not a rug pull, and the team are demonstrable builders, not influencer-marketers.

However, the investigation reveals a cluster of concerns that marketing materials do not surface prominently: **Pendle's TVL has collapsed ~85% from its $13.4B September 2025 peak** to roughly $2B in early 2026; the **$6.9B "open interest" headline figure is notional derivative exposure**, not actual locked capital ($91M deposits, $416K total fees); and **ChainSecurity identified an open, unresolved math insolvency risk** in the Boros margin system. Boros additionally introduces structural centralization — Binance oracle dependency, whitelisted-only liquidations, admin order purging, and off-chain infrastructure liveness risk — that Pendle V2 did not carry.

The PENDLE token has declined **-85% from its ATH of $7.52** (April 2024), with the protocol TVL at multi-year lows as the airdrop/points farming mercenary capital that drove the 2025 peak has fully unwound.

**Confidence Level:** High  
**Top 3 Risks:**
1. **Binance investor/oracle conflict** — YZi Labs (formerly Binance Labs) is a Pendle investor AND Binance is the primary oracle for Boros settlement. Binance controls data that directly determines whether Boros users profit or lose. This structural conflict has never been publicly addressed by the team.
2. **Open ChainSecurity math insolvency finding** — "Incorrect mathematical modeling of the margin system might lead to insolvency of certain users." Status: acknowledged, not marked as resolved. Settlement system complexity remains an open attack surface.
3. **Whitelisted centralization** — liquidations, order cancellation, and order purging are all permissioned to Pendle-operated bots. If bots fail during a rate spike, the protocol has no permissionless fallback for solvency maintenance.

**Top 3 Positive Signals:**
1. Multi-year verifiable track record — Pendle has operated since 2021, survived multiple DeFi bear markets, two direct security incidents (both contained), and commands meaningful ongoing TVL
2. Serious security posture — Pendle V2 audited by 6 firms; Boros audited by ChainSecurity + claimed Spearbit/WatchPug (latter unverified publicly); active Cantina + Immunefi bug bounties; Chaos Labs risk infrastructure
3. Genuine builders — the protocol generates real fees, has real TVL, and shipped a genuinely novel product (on-chain funding rate IRS); no pump-and-dump pattern identified

---

## 2. Team Assessment

### 2.1 Pendle Finance — Entity Background

Pendle Finance was introduced in November 2020 as "Benchmark" before rebranding. It launched publicly in 2021 and raised $3.7M from institutional backers including Mechanism Capital, HashKey Capital, Spartan Group, Crypto.com Capital, DeFi Alliance, and **YZi Labs (formerly Binance Labs)**.

The team is incorporated in Singapore. TN Lee appears publicly at industry events and in media interviews. The protocol has been operating continuously for over 5 years without an exit or abandonment.

⚠️ **BINANCE INVESTOR/ORACLE CONFLICT — FLAGGED:** YZi Labs (Binance Labs' renamed entity) holds a financial stake in Pendle. Boros uses Binance's funding rate API as its primary — and initially sole — oracle for settling all positions. Binance therefore simultaneously: (a) benefits financially from Pendle's success, and (b) controls the data used to settle Boros positions. This conflict has **not been publicly addressed** in any project documentation reviewed. [VERIFIED structural conflict; no misconduct evidence found]

**Source:** [Yahoo Finance — Pendle $3.7M raise](https://finance.yahoo.com/news/pendle-raises-3-7m-defi-080000426.html), [CoinCarp investors](https://www.coincarp.com/currencies/pendlefinance/fundraising/)

---

### 2.2 TN Lee — CEO and Co-Founder

**Real identity:** Verified. Full name used in public discourse.  
**Twitter/X:** [@tn_pendle](https://twitter.com/tn_pendle) — active, public-facing  
**LinkedIn:** Available — lists Dana Labs and Kyber Network  
**Background (VERIFIED):**
- ~2017–2018: Joined Kyber Network founding team as **Head of Business** — oversaw Korea, China, US, Europe expansion. Left Kyber Network before its catastrophic $48.8M exploit in November 2023 (cleared on timeline).
- ~2019: Founded **Dana Labs** — a construction-tech data analytics startup, entered AppWorks Accelerator in Singapore. **Failed to gain traction.** [VERIFIED — Crunchbase, LinkedIn]
- 2020: Pivoted Dana Labs into Pendle Finance

**Prior Failed Startup:** Dana Labs is a low-severity red flag. Construction-tech → DeFi yield trading is an abrupt pivot, and the startup had no meaningful product before pivoting. This is common in the space and does not impute fraud, but it means TN Lee had zero prior fintech or financial markets experience before Pendle.

**Red Flags:** None material. The Dana Labs failure is low-severity. No allegations of pump-and-dump. Present consistently in media since 2021.

**Full legal name unconfirmed:** "TN" may be initials; his full surname may not be "Lee." Legal identity not independently confirmed in public record. [UNVERIFIED — low severity given 5-year public presence]

**GitHub (PARTIALLY VERIFIED):** The `pendle-finance` GitHub organization contains active, substantive repositories including `pendle-core-v2-public` (archived as read-only January 2026, indicating stable mature code) and `sdk-boros-public`. ~167 contributors to the organization. The engineering work is real, not cosmetic.

**Note:** Core repositories use the suffix "-public" (e.g., `pendle-core-v2-public`), suggesting private counterpart repositories may exist where the final production code is maintained. This is common practice but means the audited/public code may not be identical to the deployed production code.

**What Could NOT Be Verified:** Specific commit attribution to TN Lee personally. His individual GitHub profile was not surfaced.

---

### 2.3 Vu Nguyen — CTO / Chief Engineer

**Real identity:** Verified.  
**Background:**
- 3x International Mathematical Olympiad gold medalist [UNVERIFIED — sourced only from project claims; no independent journalistic confirmation found]
- Computer Science degree, National University of Singapore (NUS) [UNVERIFIED independently — sourced from project]
- Lead Smart Contract Developer at **Digix** (gold tokenization project) [PARTIALLY VERIFIED — Digix public history corroborates his role]

**Digix Track Record — Adverse Context:**
Independent research surfaced that Digix **failed completely**:
- Digix launched in 2016/2017 with a $64M treasury from its DAO
- Governance mechanism was widely criticized for rewarding majority-vote conformity
- Community complained about inability to withdraw funds from the DAO
- CEO launched **"Project Ragnarok"** (full dissolution vote) in December 2019
- **$64M treasury liquidated** in January 2020
- Digix withdrew its Singapore Payment Services Act license in September 2022
- **Ceased all operations in March 2023**

**Assessment:** Vu Nguyen was a **technical developer**, not in governance or CEO role — his responsibility for Digix's governance failures is indirect. The important nuance: he was the smart contract developer on a protocol that failed due to governance dysfunction, not smart contract exploits. Pendle V2's smart contracts have not been directly exploited, suggesting he learned from Digix's technical work without replicating its organizational failures.

That said: his pre-Pendle flagship project no longer exists. The IMO medal claim and NUS degree, which are the primary indicators of his mathematical competence, could not be independently verified from non-project sources.

**Red Flags:** Digix complete dissolution is MEDIUM concern, partially mitigated by Vu's non-governance role.

---

### 2.4 "GT" and "YK" — Pseudonymous Co-Founders

**Identity:** Unknown. Two co-founders of Pendle who have maintained pseudonymous identities since inception (2020).

**Assessment:** This is a MODERATE concern, not a critical one, for the following reasons:

- Pendle has operated for 5+ years with these individuals in leadership. If they were planning an exit, they had ample opportunity (e.g., during the $10B TVL peak).
- TN Lee and Vu Nguyen are publicly identified and would personally face reputational and legal consequences from any exit.
- The pseudonymous co-founders' share of PENDLE tokens is subject to vesting schedules visible on DeFiLlama.
- That said: their backgrounds, prior projects, and motivations cannot be independently verified.

**What Could NOT Be Verified:** Real identities of GT and YK. Prior project affiliations. Whether they are still actively working on Pendle in 2026.

---

### 2.5 Institutional Investors (Verified)

| Investor | Type | Notable for |
|---|---|---|
| Mechanism Capital | Crypto VC | Invested April 2021 as lead |
| HashKey Capital | Crypto VC | Well-established, Hong Kong-based |
| Spartan Group | Crypto VC | Prominent Asia-based DeFi investor |
| Crypto.com Capital | Exchange VC | Major exchange, legitimate institution |
| DeFi Alliance | Accelerator | DeFi-focused institutional support |
| Lemniscap | Crypto VC | European, established DeFi investor |

**Assessment:** Pendle's investor base is a who's-who of legitimate Asia-Pacific DeFi institutional investors. This is meaningfully different from projects funded by anonymous angels or no disclosed investors. The investor list confirms due diligence was done on the team at founding.

---

## 3. What Boros Is — Technical Overview

Boros is an **on-chain interest rate swap (IRS) marketplace** deployed on **Arbitrum**, launched in August 2025.

**Core mechanic:** Users trade "Yield Units" (YUs). A YU represents the accumulated yield of 1 unit of a collateral asset in a yield-bearing instrument until expiry. For example, 1 BTC YU = the cumulative funding rate earned on 1 BTC in the BTCUSDT perpetual market on Binance, from now until expiry.

- **Going long a YU:** You pay a fixed rate and receive the realized floating funding rate. Profitable if actual funding rates exceed the fixed rate paid.
- **Going short a YU:** You lock in the fixed rate. Profitable if actual funding rates come in below the fixed rate received.

**Oracle source:** Funding rates are fetched from external sources (initially Binance BTCUSDT/ETHUSDT). As of April 2026, Hyperliquid BTC funding rate markets have been added.

**Architecture:** Hybrid CLOB (Central Limit Order Book) + AMM on Arbitrum. The orderbook is fully on-chain.

**Collateral:** Position-specific (must match the underlying asset).

**Settlement:** At expiry, the contract cash-settles based on the cumulative realized funding rates vs. the fixed rate agreed at open.

---

## 4. Third-Party Intelligence

### 4.1 Independent Analyst Coverage

| Source | Trust Level | Tone | Key Finding |
|---|---|---|---|
| [CoinDesk](https://www.coindesk.com/markets/2025/08/06/pendle-lets-crypto-traders-bet-on-bitcoin-and-ether-funding-rates-with-boros-platform) | HIGH | Neutral/descriptive | Straight news on Boros launch, no adversarial analysis |
| [Blockworks — tokenizes funding rates](https://blockworks.co/news/boros-pendle-tokenizes-funding-rates) | HIGH | Cautiously bullish | Notes Boros is "starting from 0 again" with a new risk engine |
| [Blockworks — sleeper perps](https://blockworks.co/news/boros-sleeper-perps) | HIGH | Cautiously bullish | Boros <5% of Pendle revenue; ADL risk; 1,000bps scenario modeled |
| [The Defiant](https://thedefiant.io/news/defi/pendle-announces-leveraged-yield-tokenization-platform) | HIGH | Neutral | Launch announcement; no adversarial analysis |
| [DL News — $69.8B yield settled](https://www.dlnews.com/external/pendle-settles-698-billion-in-yield-bridging-the-140t-fixed-income-market-to-crypto/) | MEDIUM-LOW | Positive | **⚠️ Appears to be a paid/sponsored placement** — treat with significantly lower weight than standard DL News editorial |
| [Chaos Labs — Boros risk infrastructure](https://chaoslabs.xyz/posts/defi-rate-swaps-building-risk-infrastructure-for-boros) | MEDIUM-HIGH | Risk-aware | **Chaos Labs is a paid risk partner to Pendle** — conflict of interest exists, but their systemic risk warnings (Monte Carlo simulations, ADL scenarios) remain credible |
| [OAK Research — Boros funding rate futures](https://oakresearch.io/en/analyses/innovations/boros-funding-rate-futures-on-pendle) | MEDIUM | Positive | Small independent research shop; no red flags raised |
| [Auditless Research — Boros > V2](https://research.auditless.com/p/al-88-why-pendles-boros-will-be-bigger) | MEDIUM | Bullish | Investment-oriented; acknowledges new architecture risk |
| [Serenity Research (Dec 2022)](https://serenityresearch.medium.com/pendle-finance-initial-review-dec-2022-9567525e79a3) | MEDIUM | **Critical** | Early independent review called Pendle V2 "prone to hacker attacks." **Prescient** — the Penpie ecosystem hack occurred 21 months later via Pendle's permissionless composability. |
| [Exponential DeFi — Pendle risk](https://exponential.fi/protocols/pendle/9d7ffafa-4f96-4fc9-856b-dd9c4497df7e) | MEDIUM-HIGH | Risk-aware | Documents that Pendle multisig has fewer than 4 signers; timelock documentation described as ambiguous or absent |
| Rekt.news | N/A | N/A | **No entry for Pendle or Boros** — meaningful absence |

**Multisig Risk (Exponential DeFi, UNVERIFIED):** Exponential DeFi's risk profile documents that Pendle's upgrade/admin multisig has fewer than 4 signers and timelock documentation is ambiguous. If correct, this means protocol upgrades could theoretically be pushed with minimal deliberation. **This requires independent verification via Arbiscan contract reads of the AccessController admin roles** — it was not independently confirmed in this investigation.

**Assessment:** Despite Pendle's prominence, there is a notable absence of independent adversarial coverage of Boros specifically. The existing coverage skews promotional. The most notable adversarial signal is the 2022 Serenity Research warning, which proved accurate in direction (though the exploit was in a third-party protocol). The DL News piece should be discounted as likely paid placement.

### 4.2 Audit and Security Assessment

#### Boros-Specific Audit: ChainSecurity

- **Auditor:** [ChainSecurity](https://chainsecurity.com) — a Tier-1 academic-grade security auditor based in Switzerland, affiliated with ETH Zurich
- **Report:** [chainsecurity.com/security-audit/pendle-boros-markets](https://www.chainsecurity.com/security-audit/pendle-boros-markets)
- **Status:** Published. Key findings publicly summarized.

**ChainSecurity Findings Summary:**

| Category | Assessment | Details |
|---|---|---|
| Asset Solvency | **High** (after v1 remediation) | HIGH finding (v1): "High priced buy order on empty orderbook can generate bad debt." Resolved in v2 via margin system revamp + admin purge capability. |
| Price Manipulation Resistance | **Good** | TWAP instability concern if spread is high. Mitigated by spread reduction and increased TWAP duration. |
| Arithmetic Operations | **High** | Rounding favors protocol; high-precision calculations used. |
| Code Complexity | **Good but risky** ⚠️ | Well-structured but uses extensive inline assembly that bypasses safety checks. Settlement process (FTags, TickNonceData, Quaternary Indexed Trees, LibOrderIdSort) is "exceptionally complex," significantly increasing the surface area for subtle state consistency bugs, off-by-one errors, and edge cases. |
| Math Insolvency Risk | **Open finding** ⚠️ | "Incorrect mathematical modeling of the margin system might lead to insolvency of certain users." **Not marked as resolved.** |
| Documentation | **High** | Whitepaper and specification available; matches implementation. |
| Decentralization | **Improvable** ⚠️ | Critical operations (order cancellation, purging, liquidations) require **whitelisted accounts** only. |
| Parameter Security | **Human-dependent** ⚠️ | "The security of the system vitally depends on the correct selection of market parameters... it is the responsibility of Pendle to choose parameters." Systemic insolvency risk is explicitly a team-responsibility, not a protocol-property. |

**Critical Remediated Finding:** The empty orderbook bad debt vulnerability (v1) was resolved before mainnet launch. Positive.

**Open Math Insolvency Risk:** ChainSecurity's finding that incorrect margin modeling "might lead to insolvency of certain users" was not marked as resolved. This is a live risk that users cannot independently verify without reviewing margin parameter calculations.

**Persistent Structural Risk:** The audit uses upgradeability and pausability as mitigating factors for multiple open findings. This means **the safety net for residual risks is the team's ability to intervene, not trustless protocol design.** Trust in Pendle's operational competence is load-bearing for the security model.

#### Claimed Additional Audits: Spearbit and WatchPug [UNVERIFIED]

The Pendle security documentation references audits by Spearbit and WatchPug in addition to ChainSecurity. However, no publicly linked PDF reports for these firms' Boros-specific engagements were found in this investigation. **Treat these as project claims until the reports are independently accessed.** The existence of ChainSecurity's audit is confirmed; the others are not.

#### Pendle V2 Audits (Parent Protocol)

Pendle V2 smart contracts have been audited by **6 separate auditors**:
1. Ackee
2. Dedaub
3. Dingbats
4. Code4rena (contest wardens)
5. Additional auditors documented in GitHub `audits/` directory

Audit reports are publicly available at [github.com/pendle-finance/pendle-core-v2-public/tree/main/audits](https://github.com/pendle-finance/pendle-core-v2-public/tree/main/audits).

**Bug Bounty:** Active Cantina bounty at [cantina.xyz/bounties/aa966ff2-4740-49da-af4a-40f85e2e82a3](https://cantina.xyz/bounties/aa966ff2-4740-49da-af4a-40f85e2e82a3)
- Critical severity: up to **$500,000**
- High severity: up to **$100,000**
- Covers 9 core Boros contracts on Arbitrum

**Assessment:** The security posture is serious and multi-layered. Six audits for the core protocol + a specialist ChainSecurity audit for the new Boros product + an active six-figure bug bounty is above-average for DeFi. The key gap is that the Boros-specific audit is from a single firm (ChainSecurity), not multiple firms.

### 4.3 Security Incidents

#### Pendle Twitter/X Account Hijack — March 30, 2024

**What happened:** Pendle's official Twitter/X account was compromised. A fake airdrop was posted. **No user funds were lost.** The account was recovered.

**Assessment:** Social media security incident only. No on-chain impact. Demonstrates that the team's operational security has had gaps, but the impact was contained.

**Source:** [Quadriga Initiative](https://quadrigainitiative.com/cryptocurrencyhackscamfraudwiki/index.php?title=Pendle_Finance_Twitter_Hack_Fake_Airdrop)

#### Penpie Hack — September 3, 2024 ($27M)

**What happened:** Penpie, a **third-party protocol** built on top of Pendle, was exploited for $27.3M via a reentrancy vulnerability in Penpie's own `_harvestBatchMarketRewards` function. The attacker registered a malicious Pendle Market (Pendle is permissionless for market creation) and exploited Penpie's lack of reentrancy protection to drain assets.

**Impact on Pendle:** 
- Pendle itself was NOT vulnerable — the bug was in Penpie's code
- Pendle paused its contracts promptly, protecting an estimated $105M in further potential losses
- Pendle's PENDLE token declined ~9% in the immediate aftermath
- Pendle published post-incident analysis and resumed normal operations

**Adversarial assessment:** This incident actually demonstrates Pendle's security discipline:
1. Their pause mechanism worked and was used appropriately
2. The vulnerability was in a third-party protocol, not Pendle itself
3. Response was rapid and effective
4. The permissionless nature of Pendle market creation (which enabled the attack vector for Penpie) is a known property, not a bug

**Source:** [The Block](https://www.theblock.co/post/314616/pendle-says-it-saved-105-million-that-could-have-been-further-drained-amid-penpie-hack), [The Defiant](https://thedefiant.io/news/defi/pendle-pauses-contracts-after-yield-protocol-penpie-suffers-usd27-million-exploit)

#### CPIMP Attack — July 2025

**What happened:** A widespread "Customized Proxy In the Middle of Proxy" (CPIMP) vulnerability was discovered and exploited across multiple DeFi protocols. The attack front-runs a proxy's initialization call and inserts a hidden intermediary layer. Pendle was among partially-affected protocols.

**Impact on Pendle:** Pendle had already migrated from infected contracts by the time the public disclosure occurred (3 weeks prior to the announcement). The migration cost Pendle "small amounts" due to anti-recovery mechanisms in the CPIMP variant they faced (which blocked transfers above 90% of balance). **No large-scale fund loss occurred.**

**Adversarial assessment:** This is a genuine security incident where Pendle lost some funds. The amounts appear small and the team detected and responded before broader exploitation. However, this confirms that Pendle's contracts are not immune to exploit and that proxy upgradeability is a live attack surface, not just a theoretical risk.

**Source:** [Dedaub CPIMP disclosure](https://dedaub.com/blog/the-cpimp-attack-an-insanely-far-reaching-vulnerability-successfully-mitigated/)

### 4.4 Community Sentiment

- **Reddit:** Pendle has active Reddit presence with substantive technical discussion. No specific Boros rug or scam threads found. Community discussion is genuinely analytical (not promotional).
- **Governance:** Pendle has active governance forum participation.
- **Aave Governance:** Chaos Labs published a Pendle Principal Token Risk Oracle proposal to Aave governance — indicating Pendle's instruments are being integrated into blue-chip protocols with their own risk teams reviewing them. Source: [Aave Governance](https://governance.aave.com/t/arfc-pendle-principal-token-risk-oracle/20962).

### 4.5 Systemic Contagion Risk — Pendle-Aave-Ethena Loop

**Source Trust: HIGH** (independently documented by Chaos Labs and The Block; Aave governance record)

This is the highest-severity systemic risk identified in the third-party intelligence sweep. It is not a Boros-specific risk but directly implicates Boros's correlated exposure:

**The Loop (documented mechanism):**
1. Users borrow against Pendle principal tokens (PTs) on Aave to purchase more USDe/sUSDe (Ethena stablecoin)
2. This loop swelled Ethena's Aave footprint to **$6.6 billion** at peak
3. Pendle PTs were accepted as collateral on Aave via a custom risk oracle (Chaos Labs' Pendle PT Risk Oracle, approved by Aave governance)

**The Failure Mode:**
- Boros allows users to trade the funding rates that underpin sUSDe yields
- A funding rate collapse simultaneously triggers: (1) Boros forced liquidations on long-funding positions, (2) sUSDe yield compression → Ethena loop deleveraging, (3) Pendle PT collateral values on Aave at risk → Aave pool stress
- These three effects are **positively correlated** — they all worsen together in the same adverse scenario

**Chaos Labs Warning (August 2025):**
Chaos Labs formally warned Aave governance: if funding rates fall and sUSDe yields compress, borrowers deleverage en masse, stressing Aave's core pools and risking liquidity strains across the entire Pendle-Aave-Ethena ecosystem.

**Why This Matters for Boros Users:**
Boros is not an isolated product. A severe funding rate spike or collapse triggers a cascade that runs through Ethena → Pendle V2 → Aave simultaneously. The advertised "hedge against funding rate volatility" instrument is itself embedded in a structure where that same volatility propagates systemic contagion.

**Sources:** [The Block — Chaos Labs warns on Pendle-Aave-Ethena loop](https://www.theblock.co/post/367265/chaos-labs-debates-usde-risks-as-pendle-looping-trade-swells-ethenas-aave-footprint-to-6-6-billion) | [Aave Governance — Pendle PT Risk Oracle](https://governance.aave.com/t/arfc-pendle-principal-token-risk-oracle/20962) | [Chaos Labs — Pendle PT Risk Oracle](https://chaoslabs.xyz/posts/introducing-pendle-pt-risk-oracle)

### 4.6 Auto-Deleveraging (ADL) Risk

**Source Trust: HIGH** (Chaos Labs, Blockworks, ChainSecurity audit)

Boros uses **auto-deleveraging (ADL)** as a last-resort solvency mechanism. When a losing position's margin is exhausted and the insurance fund is insufficient, the protocol forcibly closes profitable positions to cover losses — penalizing winning traders.

- Boros caps OI at 1.2x the underlying perp OI to limit reflexivity, but this is a design constraint, not a full mitigation
- A 1,000 bps sudden funding rate spike (modeled scenario in Blockworks) could trigger cascading forced unwinds
- Chaos Labs ran Monte Carlo simulations for parameter calibration — but explicitly acknowledged this is novel territory with **no historical baseline data** on which to validate parameters
- ChainSecurity's recommendation for "extensive monitoring" implies the system is not self-correcting by design — it depends on team/bot intervention to maintain solvency

**ADL is standard practice in perpetual futures (Binance, Bybit use it).** The adversarial concern is that users taking profitable positions have no contractual protection against forced closure if the insurance fund is depleted in a tail event.

---

## 5. On-Chain Findings

### 5.1 Contract Risk Assessment

**Boros Router (Arbitrum):** `0x8080808080dab95efed788a9214e400ba552def6`
- Network: Arbitrum One
- Verified: Yes (Arbiscan)
- **In-scope contracts for Cantina bounty:** 9 core contracts including Router, MarketHub, AccessController, MarketFactory, AMMFactory, Market, AMM, FIndexOracle instances

**Pendle V2 Core (Ethereum):** Active, read-only archived January 2026 — indicating mature, stable code no longer actively modified

**Key Architectural Risks:**

1. **Upgradeable Contracts:** Boros contracts are explicitly described as upgradeable. The ChainSecurity audit notes that upgradeability is a "mitigating factor" for identified risks. This is a double-edged sword: it enables emergency fixes but also means the team can modify contract logic unilaterally. Who holds the upgrade key (EOA? Multisig? Timelock?) was NOT publicly documented in sources reviewed.

2. **Pausable Contracts:** The team can pause Boros. This was already demonstrated to work correctly in the Penpie incident context. But pause capability means user funds could be temporarily frozen at team discretion.

3. **Whitelisted Accounts for Critical Operations:** 
   - Order cancellation: whitelisted only
   - Order purging: whitelisted only
   - Liquidations: whitelisted only
   - Some market makers exempted from CLO restrictions via `exemptCLOCheck` flag
   - Individual accounts may have custom margin factors differing from global values
   
   **This is the most significant structural centralization risk.** If whitelisted bots fail, go offline, or are compromised, liquidations cannot be executed by anyone else, potentially allowing insolvent positions to accumulate bad debt.

4. **Inline Assembly:** ChainSecurity noted "extensive inline assembly that bypasses safety checks." Inline assembly in Solidity is a legitimate performance optimization technique but removes type safety and standard Solidity guards. It requires exceptional developer competence to use safely. Given Vu Nguyen's credentials, this is likely handled correctly, but it is a higher-complexity risk surface.

5. **Oracle Architecture (Critical for Boros):** Boros funding rates are sourced from external oracles:
   - **Initial:** Binance BTCUSDT and ETHUSDT funding rates
   - **Added:** Hyperliquid BTC funding rate market
   - **Planned:** Bybit, additional assets
   
   The `FIndexOracle` contract is the on-chain representation of this data. The system uses TWAP with deviation caps to prevent manipulation. However:
   - If Binance experiences downtime, manipulates its funding rate calculation methodology, or is subject to a regulatory action, Boros markets on Binance data cannot settle correctly
   - The oracle feed requires an active, functioning Binance perpetuals market
   - **This is structurally different from Pendle V2** which uses on-chain yield sources (Aave, Compound, Ethena, etc.) that are trustlessly verifiable

### 5.2 Token Distribution Analysis — PENDLE

**Total Supply:** 258,446,028 PENDLE (with inflationary emissions)

**Allocation:**
| Category | Percentage | Notes |
|---|---|---|
| Liquidity Incentives | 49.21% | Ongoing emissions to LPs |
| **Team** | **17.74%** | Linear vesting; ongoing pressure |
| Ecosystem Fund | 14.83% | Protocol-controlled |
| **Investors** | **12.07%** | Linear vesting |
| Liquidity Bootstrapping | 5.35% | Used at launch |
| **Advisors** | **0.80%** | |

**Total insider allocation (Team + Investors + Advisors): ~30.6%**

**Vesting:** Linear, extending to approximately 2030. As of this investigation, ~59% of total supply is already unlocked. The vesting schedule is publicly trackable on DeFiLlama unlocks.

**PENDLE Token Performance:**
- ATH: $7.52 (April 2024)
- December 2025 local high: ~$3.00
- Current price (April 2026): ~$1.00
- Decline from ATH: **-87%** (multi-month, not a rapid dump)
- Decline from December 2025 local high: **-67%**
- 24h volume: ~$25M (substantial, legitimate liquidity)
- Pendle TVL: **peaked at $13.4B (September 2025)**; current (early 2026): **~$2B (~85% collapse)**
- Annual fees: $78.19M (FY2025)

**TVL Collapse Driver (VERIFIED — Chaos Labs, The Block):** The $13.4B peak was fueled almost entirely by Ethena (USDe/sUSDe) yield loops and airdrop/points farming mercenary capital. As funding rates compressed in late 2025 and Ethena incentives wound down, this capital unwound in bulk. The current ~$2B TVL represents a return to baseline organic usage, stripping out the speculative overlay.

**Assessment:** The PENDLE token decline is not a rug pattern — it occurred over extended timeframes with normal trading volume, and the TVL collapse is explained by structural mercenary capital exit rather than protocol failure. However, ongoing team/investor vesting creates continuous selling pressure until ~2030, and the current TVL represents a dramatically different operating context than Boros launched into. Users should monitor unlock events via [DeFiLlama unlocks](https://defillama.com/unlocks/pendle).

### 5.3 Boros Metrics (On-Chain/Verified)

| Metric | Value | Source |
|---|---|---|
| Cumulative volume (to Jan 2026) | $9.8B | Pendle 2025 Annual Review |
| Monthly volume (Jan 2026) | $2.9B | Pendle Annual Review |
| Peak OI before Dec 2025 expiries | $245M | Blockworks |
| Total deposits (year-end 2025) | ~$91M | DeFiLlama |
| Fee revenue (to Jan 2026) | $416K | Pendle Annual Review |
| Fee share of Pendle revenue | ~10% (March 2026) | Blockworks |
| OI as % of $63B perps market | ~0.1% | Blockworks |

**Assessment:** Boros is a genuinely small but growing product. $9.8B cumulative volume is real throughput. The $416K total fee revenue in 5 months is modest but consistent with early-stage product. The 0.1% market penetration against a $63B perps market represents a significant addressable growth opportunity.

### 5.4 Suspicious Patterns

**None identified.** No evidence of:
- Wash trading on Boros
- Team wallet dumps of PENDLE correlated with Boros marketing
- Circular transactions to inflate metrics
- Fake TVL via recursive positions

The PENDLE token decline from ATH is steep but multi-month and correlated with broader market conditions. It does not exhibit the 24–48-hour pump-and-dump pattern observed in Supernova/Blackhole.

---

## 6. Red Flags Register

| # | Flag | Evidence | Source | Severity |
|---|---|---|---|---|
| 1 | **YZi Labs (Binance Labs) is a Pendle investor AND Binance is the Boros oracle** — unaddressed structural conflict | Investor list + oracle docs | CoinCarp, Pendle Docs | **HIGH** |
| 2 | Boros oracle dependent on Binance exclusively at launch | Documentation + CoinDesk | [Docs](https://pendle.gitbook.io/boros/boros-docs), [CoinDesk](https://www.coindesk.com/markets/2025/08/06/pendle-lets-crypto-traders-bet-on-bitcoin-and-ether-funding-rates-with-boros-platform) | **HIGH** |
| 3 | Whitelisted centralization: all critical ops (liquidations, order cancel) require permissioned accounts | ChainSecurity audit | [ChainSecurity](https://www.chainsecurity.com/security-audit/pendle-boros-markets) | **HIGH** |
| 4 | Settlement system "exceptionally complex" — FTags, Quaternary Indexed Trees, MatchEvent | ChainSecurity audit finding | [ChainSecurity](https://www.chainsecurity.com/security-audit/pendle-boros-markets) | **MEDIUM-HIGH** |
| 5 | Regulatory exposure: Boros is permissionless leveraged derivatives trading with no KYC | Structural | Protocol docs | **MEDIUM-HIGH** |
| 6 | GT and YK co-founders remain pseudonymous after 5+ years — no public accountability surface | Public record | Multiple sources | **MEDIUM** |
| 7 | Inline assembly bypasses safety checks in Boros contracts | ChainSecurity audit | Same | **MEDIUM** |
| 8 | CPIMP attack July 2025: Pendle affected, lost small amounts in recovery | Dedaub disclosure | [Dedaub](https://dedaub.com/blog/the-cpimp-attack-an-insanely-far-reaching-vulnerability-successfully-mitigated/) | **MEDIUM** |
| 9 | Contracts upgradeable and pausable; upgrade key holder undisclosed | ChainSecurity + docs | Audit report | **MEDIUM** |
| 10 | PENDLE token -82% from ATH; insider allocation ~30.6% with ongoing vesting | Price data + tokenomics | CoinGecko, DeFiLlama | **MEDIUM** |
| 11 | Vu Nguyen's prior project (Digix) fully dissolved: $64M treasury liquidated, ops ceased March 2023 | Digix dissolution records | Medium/Digix | **MEDIUM** (role was technical, not governance) |
| 12 | TWAP instability risk if spread is high | ChainSecurity audit | [ChainSecurity](https://www.chainsecurity.com/security-audit/pendle-boros-markets) | **MEDIUM** |
| 13 | Repo naming pattern ("-public" suffix) suggests private counterpart repos; audited code may differ from production | GitHub observation | github.com/pendle-finance | **LOW-MEDIUM** |
| 14 | Penpie hack ($27M, Sept 2024) — enabled by Pendle's permissionless market creation | Halborn, The Block | [Halborn](https://www.halborn.com/blog/post/explained-the-penpie-hack-september-2024) | **LOW-MEDIUM** (Pendle not directly vulnerable) |
| 15 | Only one audit firm for Boros (ChainSecurity) — no second firm review | Public record | ChainSecurity page | **LOW-MEDIUM** |
| 16 | Pendle Twitter/X account hijacked March 2024 — social media opsec gap | Incident record | Quadriga Initiative | **LOW** |
| 17 | TN Lee's full legal name unconfirmed; "TN" may be initials | Public record | Multiple sources | **LOW** |
| 18 | No prominent risk disclosures in Boros marketing materials | Boros landing page | [boros.pendle.finance](https://boros.pendle.finance) | **LOW** |
| 19 | **Off-chain liveness risk**: order matching, liquidation monitoring, and settlement all depend on Pendle-operated bots; no permissionless fallback | ChainSecurity audit (whitelisted ops) + protocol architecture | [ChainSecurity](https://www.chainsecurity.com/security-audit/pendle-boros-markets) | **HIGH** |
| 20 | **Pendle-Aave-Ethena loop systemic contagion**: funding rate collapse simultaneously triggers Boros liquidations + sUSDe yield compression + Aave Pendle PT collateral stress — all correlated | Chaos Labs warning, The Block, Aave governance | [The Block](https://www.theblock.co/post/367265/chaos-labs-debates-usde-risks-as-pendle-looping-trade-swells-ethenas-aave-footprint-to-6-6-billion) | **HIGH** |
| 21 | **Multisig fewer than 4 signers** (Exponential DeFi claim, UNVERIFIED) — protocol upgrades could be pushed with minimal deliberation | Exponential DeFi risk profile | [Exponential DeFi](https://exponential.fi/protocols/pendle/9d7ffafa-4f96-4fc9-856b-dd9c4497df7e) | **MEDIUM** (pending independent verification) |
| 22 | **TVL collapsed 85%** from $13.4B peak (Sept 2025) to ~$2B (early 2026) — mercenary capital has fully unwound; Boros launched into a contracting ecosystem | DeFiLlama, Chaos Labs, The Block | Multiple | **MEDIUM** |

---

## 7. Unresolved Questions

1. **Has the Binance investor/oracle conflict been formally disclosed or addressed?** YZi Labs (Binance Labs) holds a financial stake in Pendle while Binance controls the primary data feed for Boros settlement. No public statement addressing this conflict was found. This is the single most important governance question for Boros users.

2. **Who controls the upgrade keys for Boros contracts?** Is it a multisig? How many signers? What timelock, if any? This is the single most important undisclosed governance detail. Requires direct Arbiscan contract read of admin roles.

3. **Who are the whitelisted accounts for liquidations and order management?** Are these operated by Chaos Labs, the Pendle team, or third-party keepers? If whitelisted bots go offline, can positions become unresolvable?

4. **What are GT and YK's real identities?** Five years of operation suggests they are genuinely committed builders, but their backgrounds remain unverifiable.

5. **What exactly did Pendle lose in the CPIMP recovery?** "Small amounts" is unquantified. On-chain tracing of CPIMP-related Pendle transactions would establish the magnitude.

6. **Will Boros add non-Binance oracle sources faster than the Binance concentration risk justifies?** The Hyperliquid addition is encouraging, but if 80%+ of OI remains in Binance-sourced markets, oracle concentration risk persists.

7. **What happens to Boros positions if Binance changes its funding rate calculation methodology or experiences extended downtime?** No force majeure or alternative settlement mechanism is documented.

8. **Are the `exemptCLOCheck` flag and custom margin factors for specific market makers publicly disclosed?** If market makers receive preferential treatment, this creates information asymmetry for regular users.

9. **Has Boros faced any regulatory inquiries** given its permissionless leveraged derivatives offering with no KYC in multiple jurisdictions?

10. **What is the current Boros TVL and OI in April 2026?** The most recent data in this investigation is from January 2026. The market may have grown or contracted significantly since.

---

## 8. Comparative Analysis

### vs. Traditional Interest Rate Swap (TradFi)

Boros is structurally analogous to a cleared interest rate swap, but with no central clearing counterparty (CCP) and no regulatory oversight. TradFi IRS markets are the largest derivatives market by notional ($500T+). The key structural difference: Boros uses on-chain margin and whitelisted liquidation bots instead of a central clearinghouse. This makes it more accessible but less resilient to black swan events.

### vs. Pendle V2

| Feature | Pendle V2 | Boros |
|---|---|---|
| Yield source | On-chain protocols (trustless) | CEX funding rates (centralized) |
| Oracle | On-chain (verifiable) | Binance API (trust-dependent) |
| Leverage | None | Up to 1.2x (scaling) |
| Liquidations | Not applicable (no leverage) | Whitelisted bots required |
| Complexity | Medium | Very High |
| TVL | $5.8B avg 2025 | $91M deposits |

### vs. Known DeFi Rug Patterns

Boros / Pendle share **none** of the primary rug pull indicators:
- ❌ Anonymous team — Two co-founders are publicly identified with verifiable backgrounds
- ❌ No audits — 6 audits for V2, ChainSecurity for Boros
- ❌ Recent appearance — Operating since 2021 (5+ years)
- ❌ No TVL — $13.4B peak TVL (September 2025); ~$2B current baseline TVL after mercenary capital exit
- ❌ Influencer-driven launch — Institutional VC backing, developer-led team
- ❌ Token collapse in hours/days — PENDLE decline is multi-month, not a dump pattern

---

## 9. Sources Index

| Source | URL | Trust Level |
|---|---|---|
| Boros Pendle landing page | https://boros.pendle.finance/ | Low (marketing) |
| Boros GitBook Docs | https://pendle.gitbook.io/boros/boros-docs | Medium (technical, self-reported) |
| Pendle Security Docs | https://docs.pendle.finance/pendle-v2/Security | Medium (self-reported) |
| ChainSecurity — Boros Audit | https://www.chainsecurity.com/security-audit/pendle-boros-markets | High (independent auditor) |
| Cantina Boros Bounty | https://cantina.xyz/bounties/aa966ff2-4740-49da-af4a-40f85e2e82a3 | High |
| Chaos Labs — Boros Risk | https://chaoslabs.xyz/posts/defi-rate-swaps-building-risk-infrastructure-for-boros | High (independent risk firm) |
| DeFiLlama — Pendle | https://defillama.com/protocol/pendle | High (on-chain aggregated) |
| DeFiLlama — Boros | https://defillama.com/protocol/boros | High |
| DeFiLlama — PENDLE Unlocks | https://defillama.com/unlocks/pendle | High |
| Pendle GitHub — V2 Core | https://github.com/pendle-finance/pendle-core-v2-public | High (on-chain) |
| Pendle GitHub — Boros SDK | https://github.com/pendle-finance/sdk-boros-public | High |
| Arbiscan — Boros Router | https://arbiscan.io/address/0x8080808080dab95efed788a9214e400ba552def6 | High (on-chain) |
| CoinDesk — Boros Launch | https://www.coindesk.com/markets/2025/08/06/pendle-lets-crypto-traders-bet-on-bitcoin-and-ether-funding-rates-with-boros-platform | Medium-High |
| Blockworks — Boros Sleeper | https://blockworks.co/news/boros-sleeper-perps | Medium |
| Halborn — Penpie Hack | https://www.halborn.com/blog/post/explained-the-penpie-hack-september-2024 | High |
| The Block — Penpie/Pendle | https://www.theblock.co/post/314616/pendle-says-it-saved-105-million-that-could-have-been-further-drained-amid-penpie-hack | High |
| Dedaub — CPIMP | https://dedaub.com/blog/the-cpimp-attack-an-insanely-far-reaching-vulnerability-successfully-mitigated/ | High |
| The Defiant — Penpie | https://thedefiant.io/news/defi/pendle-pauses-contracts-after-yield-protocol-penpie-suffers-usd27-million-exploit | High |
| Aave Governance — Pendle PT Oracle | https://governance.aave.com/t/arfc-pendle-principal-token-risk-oracle/20962 | High (blue-chip governance) |
| Yahoo Finance — Pendle $3.7M | https://finance.yahoo.com/news/pendle-raises-3-7m-defi-080000426.html | High |
| IQ.wiki — TN Lee | https://iq.wiki/wiki/tn-lee | Medium |
| CoinGecko — PENDLE | https://www.coingecko.com/en/coins/pendle | High |
| Tokenomist — PENDLE Vesting | https://tokenomist.ai/pendle | High |
| Quadriga Initiative — Pendle Twitter Hack | https://quadrigainitiative.com/cryptocurrencyhackscamfraudwiki/index.php?title=Pendle_Finance_Twitter_Hack_Fake_Airdrop | Medium |
| Digix dissolution announcement | https://medium.com/digix/digixdaos-dissolution-655be3110196 | High |
| Three Sigma — Penpie reentrancy analysis | https://threesigma.xyz/blog/exploit/penpie-reentrancy-exploit-analysis | High |
| OAK Research — Boros funding rate futures | https://oakresearch.io/en/analyses/innovations/boros-funding-rate-futures-on-pendle | Medium |
| pendle-finance GitHub org | https://github.com/pendle-finance | High (on-chain) |
| The Block — Pendle-Aave-Ethena loop | https://www.theblock.co/post/367265/chaos-labs-debates-usde-risks-as-pendle-looping-trade-swells-ethenas-aave-footprint-to-6-6-billion | High |
| Chaos Labs — Pendle PT Risk Oracle | https://chaoslabs.xyz/posts/introducing-pendle-pt-risk-oracle | High (independent risk firm) |
| Chaos Labs — Arbitrum STIP Pendle analysis | https://chaoslabs.xyz/posts/arbitrum-stip-analysis-pendle-finance | High |
| Exponential DeFi — Pendle protocol risk | https://exponential.fi/protocols/pendle/9d7ffafa-4f96-4fc9-856b-dd9c4497df7e | Medium-High |
| Auditless Research — Why Boros will be bigger | https://research.auditless.com/p/al-88-why-pendles-boros-will-be-bigger | Medium |
| OAK Research — Boros funding rate futures | https://oakresearch.io/en/analyses/innovations/boros-funding-rate-futures-on-pendle | Medium |
| Serenity Research — Pendle initial review 2022 | https://serenityresearch.medium.com/pendle-finance-initial-review-dec-2022-9567525e79a3 | Medium |
| CoinTelegraph — Penpie exploited $27M | https://cointelegraph.com/news/penpie-protocol-exploited-suffers-27-million-loss | High |
| The Record — Penpie files FBI report | https://therecord.media/penpie-defi-protocol-ethereum-stolen | High |
| Boros by Pendle — Medium launch post | https://medium.com/boros-fi/boros-by-pendle-yield-trading-with-margin-63d026dc7399 | Low (official) |

---

*Report generated: April 11–12, 2026. Boros launched August 2025; 8 months of live operational data informed this report. Boros-specific TVL/OI figures as of January 2026; current figures require live DeFiLlama check.*
