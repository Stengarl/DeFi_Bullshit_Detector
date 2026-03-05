# Pleasing Gold (PGOLD) — Adversarial Due Diligence Report

**Prepared:** 2026-03-05
**Investigator:** DeFi Adversarial Research Framework
**Methodology:** Guilty until proven innocent. On-chain data and independent sources ranked above official claims.
**Research Scope:** Phase 1-4 full investigation

---

## LEAD WITH CRITICAL ALERTS

**ALERT 1:** $102,918,211 market cap. $192.61 in 24-hour trading volume. 2 transactions in 24 hours. This ratio (~0.000187% vol/mcap) is an extreme anomaly. Either the market cap is fabricated, the token has no genuine liquid market, or activity has entirely collapsed. This is the single most alarming quantitative signal in this investigation.

**ALERT 2:** Zero named team members in any public document. Zero named custodians. Zero named licensing authorities. Zero independent audits. The project makes gold-custody claims with none of the verification infrastructure required to support them.

---

## 1. Executive Summary

**Verdict: EXTREME CAUTION — HIGH RISK**
**Confidence Level: HIGH** (converging signals across multiple independent data points)

Pleasing Gold (PGOLD) is an RWA (Real World Asset) tokenized gold platform launched in October 2025 by a company called "Pleasing International," allegedly headquartered in Hong Kong. The project claims each PGOLD token represents one troy ounce of LBMA-certified physical gold, backed by institutional custody and redeemable in Hong Kong.

The core problem: every single claim that would make this project trustworthy — gold custody, licensing, audits, team identity, reserves — is asserted without any independently verifiable evidence. Meanwhile, the on-chain data tells a deeply concerning story: near-zero trading activity against a $100M+ market cap, a Kryll X-Ray security rating of 2.9/10 with 28 flagged vulnerabilities, and an upgradeable proxy contract with role-gated mint/burn functions that give an unnamed admin unilateral power over the token supply.

The Chainlink Data Streams integration, confirmed by Chainlink's official account, is the sole independently verified positive signal. It partially validates that the protocol exists and is functional, but does NOT validate gold reserves, licensing, team identity, or financial safety.

### Top 3 Risks

1. **Ghost market cap:** $102M market cap with $192 daily volume and 2 daily transactions — hallmark of an artificial/inactive market or complete illiquidity trap
2. **Complete team anonymity + unverifiable custody:** No custodian, no license authority, no auditor named anywhere — the gold may not exist
3. **Upgradeable contract with admin mint/burn:** Admin can change code or mint unlimited tokens with no public timelock disclosed

### Top 3 Positive Signals

1. **Chainlink officially confirmed** Data Streams integration on their own X account (independently verifiable)
2. **Listed on CoinGecko (#269)** and multiple exchanges (MEXC, LBank, Uniswap V3)
3. **ERC-20 on Arbitrum** with a public contract address — the protocol is at minimum real and deployed

---

## 2. Team Assessment

### 2.1 Identity — UNVERIFIED / ANONYMOUS

**Finding (CRITICAL): Zero team members are publicly named in any official document.**

Exhaustive search of: official GlobeNewswire press release (Oct 29, 2025), CoinPedia sponsored post, GitBook technical docs, CoinGecko listing, MEXC page, LBank page, X/Twitter profile — none name any individual.

The press release was distributed from **Singapore** (not Hong Kong, where the company claims HQ). Geographic discrepancy is unresolved.

**Official claim (LOW TRUST):** "Pleasing International has been a cornerstone of Asia's physical gold market" — Source: GlobeNewswire PR, self-reported.
**Independent verification:** FAILED. Zero corroborating evidence from non-affiliated sources.

**Official claim (LOW TRUST):** "Since 2023, Pleasing International has built an integrated ecosystem of vaulting, refining, logistics, and distribution"
**Independent verification:** FAILED. No evidence of pre-2025 public footprint for this company found anywhere.

### 2.2 GitHub Activity — NO REPOSITORY FOUND

No public GitHub organization or repository for Pleasing Gold or Pleasing International was found through any search. Source code is NOT open-sourced. All technical documentation is in GitBook, which is team-controlled marketing infrastructure.

**Comparison:** PAXG (Paxos Gold) has a fully public, audited, open-source contract at github.com/paxosglobal/paxos-gold-contract. PGOLD has nothing equivalent.

### 2.3 Social Media Forensics

- **Twitter/X @PleasingGolden:** Account exists. No independent crypto researchers, analysts, or community members found discussing this project organically.
- **Kryll X-Ray Social Score: 8%** — near the absolute floor across all tracked metrics.
- **Reddit:** Zero posts found for "Pleasing Gold" or "PGOLD" in r/CryptoCurrency, r/DeFi, or r/ethfinance. For a $100M+ market cap asset, this is deeply anomalous.

### 2.4 Background Verification

**"Licensed precious-metals enterprise"** — No licensing body named. Hong Kong regulates precious metals dealers under the Anti-Money Laundering and Counter-Terrorist Financing Ordinance (AMLO) via the Customs and Excise Department. No AMLO registration, license number, or regulatory authority cited in any document.

**Company registration search for "Pleasing International" in HK:** ZERO public results. This does not conclusively prove non-existence (HK Companies Registry requires direct database access), but zero public footprint for a claimed "cornerstone of Asia's physical gold market" operating since 2023 is deeply suspicious.

### 2.5 What Could NOT Be Verified

- Any individual team member's identity
- Company's HK registration number or legal entity name
- Any pre-2025 business activity of Pleasing International
- Whether Pleasing International has any physical gold operations

---

## 3. Third-Party Consensus

### 3.1 Independent Analyst Coverage

- **Rekt News:** No coverage found (neutral — covers post-event exploits)
- **The Defiant:** No coverage found
- **DL News:** No coverage found
- **DeFiLlama:** NOT listed as a tracked protocol. No TVL data exists.
- **Independent security researchers:** No commentary from any named researcher found.

All coverage found is either paid sponsored posts (CoinPedia — explicitly labeled "Sponsored") or verbatim press release syndication (GlobeNewswire reprinted by Manila Times, BitcoinEthereumNews, ITNewsOnline).

**ZERO independent analytical coverage from any credible third-party source.**

### 3.2 Audit and Security Assessment

**Finding (CRITICAL): No public smart contract audit has been submitted to Arbiscan.**

**Kryll X-Ray Independent Analysis:**

| Category | Score |
|---|---|
| Overall Risk Level | HIGH RISK |
| Composite X-Ray Score | 2.9 / 10 |
| Security Alerts Flagged | 28 total |
| Website Security Grade | F |
| Security Score | 59% (problematic) |
| OnChain Metrics | 4% (critical deficiency) |
| Social Score | 8% |
| Infrastructure Security | Poor |

GitBook documentation mentions "monthly standard attestations" and "independent audit" but names no auditor and provides no report link. This is an unverified claim from a self-controlled marketing document.

**Compiler Bugs Detected via Arbiscan:**
- LostStorageArrayWriteOnSlotOverflow
- VerbatimInvalidDeduplication
- FullInlinerNonExpressionSplitArgumentEvaluationOrder
- MissingSideEffectsOnSelectorAccess

These are low-severity but confirm the contract was compiled with a version containing known bugs.

**Chainlink Partnership — INDEPENDENTLY VERIFIED (POSITIVE):**
Source: x.com/chainlink/status/1983701290149670927
Chainlink's official X account confirmed: integration of Chainlink Data Streams to power XAU markets on Arbitrum. Confidence: HIGH. This is the ONLY independently verified positive claim in the entire investigation.

**LayerZero Partnership — UNVERIFIED:**
Claimed repeatedly in official documents. No independent confirmation from LayerZero's official channels found.

### 3.3 Community Sentiment (Non-Affiliated)

Reddit: Zero posts found. Crypto Twitter: Only the official account and Chainlink's confirmation tweet. No independent community voice found anywhere.

Absence of community is itself a red flag for a $100M+ asset. PAXG, XAUT, and other legitimate tokenized gold products have active, searchable communities with years of organic discussion.

---

## 4. On-Chain Findings

### 4.1 Contract Details

| Parameter | Value |
|---|---|
| Chain | Arbitrum One |
| Contract Address | 0x3e76bb02286bfeaa89dd35f11253f2cbce634f91 |
| Standard | ERC-20 |
| Contract Type | EIP-1967 Transparent Proxy |
| Implementation Contract | 0xd81ea1e2179c983a45aa95929f189c2bd59788d7 (PGOLDToken) |
| Public Audit on Arbiscan | NONE submitted |
| Compiler Bug Flags | 4 known low-severity bugs |

**EIP-1967 Transparent Proxy — HIGH CONCERN:** This pattern allows the admin to upgrade the contract's logic to a new implementation at any time. Without a timelock with sufficient delay (typically 48-72 hours minimum, ideally 2 weeks), an admin can change the contract to anything — including a version that drains user funds or freezes all transfers. **No timelock duration disclosed in any document.**

**Role-gated mint/burn:** Admin can mint new PGOLD tokens or burn existing ones without on-chain governance or community approval. There is no visible on-chain mechanism that independently verifies 1:1 gold backing at mint time.

### 4.2 Token Distribution and Market Data

| Metric | Value | Assessment |
|---|---|---|
| Market Cap | ~$102,918,211 | UNVALIDATED — likely artificial |
| Circulating Supply | ~20,000 PGOLD | Very thin supply |
| 24h Trading Volume | $192.61 | EXTREME ANOMALY |
| Vol/MCap Ratio | ~0.000187% | Should be 1-10%+ for active assets |
| 24h Transactions | 2 | Near-zero activity |
| Primary Market | Uniswap V3 (Arbitrum One), PGOLD/USDT0 pair | Single illiquid DEX |
| DeFiLlama Listing | NOT LISTED | No TVL tracked |
| Publicly Tracked Holders | 0 (per TheBitTimes system) | Unclear distribution |

**The Vol/MCap anomaly is the most damning quantitative signal in this report.** PAXG typically runs 2-8% vol/mcap ratio. PGOLD is roughly 10,000x below this threshold. The market cap APPEARS real because PGOLD is pegged to gold spot price (~$2,900/oz x 20,000 tokens = ~$58M in gold terms, with token premium on top). But the MARKET for PGOLD tokens is not functioning — no genuine price discovery is occurring.

### 4.3 Suspicious Patterns

1. **Vol/MCap 0.000187%** — orders of magnitude below any comparable legitimate asset
2. **Only 1 trading pair on 1 DEX** — no real market infrastructure for a $100M asset
3. **Role-gated mint/burn with no on-chain reserve verification** at issuance
4. **PUSD synthetic stablecoin with "hybrid reserve" model** echoes UST/Luna deathspiral architecture
5. **Zero DeFiLlama tracking** suggests no genuine protocol TVL or usage activity

---

## 5. Red Flags Register

| # | Red Flag | Severity | Evidence Source | Why It Matters |
|---|---|---|---|---|
| RF-01 | $192 daily volume vs. $102M market cap | CRITICAL | CoinGecko/CoinCarp (independent aggregators) | Ghost market — no real price discovery or exit liquidity |
| RF-02 | 2 on-chain transactions in 24 hours | CRITICAL | TheBitTimes on-chain data | Asset of this size should have thousands of daily txns |
| RF-03 | Complete team anonymity | CRITICAL | All official documents exhaustively checked | People rug. Anonymous teams cannot be held accountable |
| RF-04 | No named custodian for gold reserves | CRITICAL | GlobeNewswire PR, GitBook TaaS page | Gold claims completely unverifiable without custodian identity |
| RF-05 | No licensing authority cited | CRITICAL | All official documents | "Licensed" claim cannot be verified and may be false |
| RF-06 | No public smart contract audit | CRITICAL | Arbiscan, Kryll X-Ray | 28 security alerts; gold RWA demands institutional-grade audit |
| RF-07 | Upgradeable proxy — admin controls all code | HIGH | Arbiscan contract analysis (on-chain) | Admin can deploy malicious code to replace current contract |
| RF-08 | Role-gated admin mint/burn | HIGH | GitBook technical docs (confirmed architectural choice) | Admin can inflate supply or destroy balances unilaterally |
| RF-09 | No public GitHub repository | HIGH | GitHub search — no results | Opaque codebase; no independent code review possible |
| RF-10 | Kryll X-Ray Score: 2.9/10 — HIGH RISK | HIGH | Kryll.io automated audit tool (third-party) | 28 alerts, F website grade, 4% on-chain score |
| RF-11 | Zero Reddit/community presence | HIGH | Reddit search across major crypto subs | $100M+ asset with zero organic community is anomalous |
| RF-12 | All press coverage is paid/sponsored | HIGH | Source labels (CoinPedia "Sponsored", GlobeNewswire paid wire) | Marketing dressed as journalism — zero independent coverage |
| RF-13 | Pre-2025 company footprint not found | HIGH | Web search for "Pleasing International" history | Claims "since 2023" with zero public evidence of this |
| RF-14 | Proof of reserve — no mechanism disclosed | HIGH | GitBook TaaS page | Claims PoR but names no auditor and provides no accessible endpoint |
| RF-15 | LayerZero partnership unconfirmed by LayerZero | MEDIUM | LayerZero official channels not found confirming | Partnership claim may be one-sided or exaggerated |
| RF-16 | PR distributed from Singapore, HQ claimed as Hong Kong | MEDIUM | GlobeNewswire filing location data | Geographic inconsistency between claimed and operational base |
| RF-17 | Not listed on DeFiLlama | MEDIUM | DeFiLlama protocol search | Genuine protocols with real TVL get listed — absence is a signal |
| RF-18 | PUSD synthetic stablecoin echoes UST/Luna architecture | MEDIUM | GitBook description of PGOLD-PUSD loop | Algorithmic deathspiral risk not evaluated; precedent is catastrophic |
| RF-19 | 4 compiler bug flags on deployed contract | LOW | Arbiscan contract analysis | Low-severity bugs in production code — poor hygiene |
| RF-20 | Website security grade: F | LOW | Kryll X-Ray | Poor operational security infrastructure |

---

## 6. Comparative Analysis

### vs. Legitimate Tokenized Gold Competitors

| Feature | PGOLD | PAXG (Paxos Gold) | XAUT (Tether Gold) |
|---|---|---|---|
| Named custodian | NO | YES (Brinks) | YES (named vault) |
| Named team | NO (anonymous) | YES (Paxos exec team) | YES (Tether team) |
| Regulatory license | NO (unspecified) | YES (NYDFS Trust Company) | YES (disclosed) |
| Published smart contract audit | NO | YES (multiple public) | YES (quarterly attestations) |
| Open source code | NO | YES (GitHub) | YES |
| Vol/MCap ratio | 0.000187% | ~2-8% | ~1-5% |
| Organic community | NONE FOUND | Active across platforms | Active |
| DeFiLlama tracking | NOT LISTED | Listed | Listed |

PGOLD fails every institutional legitimacy benchmark set by its direct category peers.

### Pattern Match Against Known Frauds

**Terra/Luna parallel:** PUSD is described as a "synthetic stablecoin" backed by a "hybrid reserve of USDT collateral and tokenized metal exposure" with a PGOLD-PUSD convertibility loop. This architecture mirrors UST-LUNA, which collapsed in May 2022, wiping approximately $40B in value. The gold backing provides more stability than Luna, but the synthetic stablecoin adds an unanalyzed and potentially catastrophic risk layer.

**Ghost liquidity pattern:** Elevated market cap with near-zero trading activity is consistent with exit scam staging — founders establish a high paper valuation, then wait for conditions before liquidating treasury positions into whatever thin liquidity exists.

**Sponsored press pattern:** Legitimate projects with real track records earn organic media coverage. Exclusive reliance on paid wire distribution and sponsored posts indicates a project that cannot earn credibility independently.

---

## 7. Unresolved Questions

Declared openly — NOT filled with assumptions.

1. **Who are the actual humans behind Pleasing International?** Cannot determine. No names exist in any public document.
2. **Does Pleasing International hold any physical gold?** Cannot verify without named custodian or accessible proof of reserve.
3. **What specific license does "licensed precious-metals enterprise" refer to?** Cannot determine — no authority cited.
4. **What is the actual token holder distribution?** Full on-chain holder list not retrieved (Arbiscan returned 403).
5. **Is there a timelock on the admin/proxy upgrade function?** Not disclosed anywhere. If absent, code can change instantly.
6. **Has LayerZero officially confirmed the partnership?** Not found in any independent source.
7. **Why is trading volume essentially zero?** Three possibilities: (a) issuer controls all liquidity and there is no free market; (b) token launched and interest immediately collapsed; (c) hidden market not indexed by public aggregators. None is benign.
8. **Does PUSD have a deathspiral failure mode?** Not fully analyzed in this investigation.
9. **Are the 20,000 PGOLD in circulation actually held externally, or primarily by team wallets?** Cannot determine without full holder list.

### Additional Investigation Needed to Close Gaps

- Direct Arbiscan API query of full token holder distribution
- Metasleuth/Breadcrumbs wallet clustering on deployer address to identify insider wallets
- HK Companies Registry direct database lookup for "Pleasing International"
- HK Customs and Excise Department PMSD license verification
- LayerZero official ecosystem/partner list check
- Smart contract static analysis via Slither/Mythril on verified source code
- PUSD mechanism modeling for depeg scenarios

---

## 8. Sources and Trust Ratings

**TIER 1 — On-Chain (Most Trusted)**
- Arbiscan PGOLD Contract: https://arbiscan.io/token/0x3e76bb02286bfeaa89dd35f11253f2cbce634f91

**TIER 2 — Independent Third-Party Analysis**
- Kryll X-Ray Security Report: https://app.kryll.io/x-ray/pleasing-gold

**TIER 3 — Verified Social (Confirmed by Named Partner)**
- Chainlink Official X Confirmation: https://x.com/chainlink/status/1983701290149670927

**TIER 4 — Independent Market Aggregators**
- CoinGecko PGOLD: https://www.coingecko.com/en/coins/pleasing-gold
- Token Terminal PGOLD: https://tokenterminal.com/explorer/projects/pleasinggold/pgold
- TheBitTimes On-Chain Data: https://thebittimes.com/token-PGOLD-ARB-0x3e76bb02286bfeaa89dd35f11253f2cbce634f91.html
- MEXC Tokenomics Page: https://www.mexc.com/price/pleasing-gold/tokenomics
- KuCoin Coverage: https://www.kucoin.com/news/insight/ARB/6902bcc8008bc300077747d0

**TIER 5 — Official Project Docs (Lowest Trust — Marketing Material)**
- GlobeNewswire Launch PR (Oct 29, 2025): https://www.globenewswire.com/news-release/2025/10/29/3176301/0/en/Pleasing-International-Launches-RWA-Platform-Pleasing-Golden-Introducing-Tokenized-Gold-PGOLD-and-Synthetic-Dollar-PUSD.html
- CoinPedia SPONSORED POST: https://coinpedia.org/sponsored/pleasing-international-launches-rwa-platform-pleasing-golden/
- Pleasing GitBook TaaS Docs: https://pleasing.gitbook.io/docs/solutions/tokenization-as-a-service-taas

---

## 9. Research Limitations

This investigation was conducted using web search and public data sources as of 2026-03-05. The following were NOT performed:

- Direct Arbiscan API call for full holder distribution
- Wallet clustering (Metasleuth, Breadcrumbs) on deployer address
- Smart contract static analysis (Slither/Mythril)
- PUSD mechanism deep-dive and deathspiral scenario modeling
- HK Companies Registry direct database lookup
- Twitter/X deep archive analysis of @PleasingGolden full history

The convergence of signals across independently accessible sources — Kryll X-Ray score, trading volume anomaly, holder data, social data, press source analysis, contract architecture — is sufficient to assign HIGH RISK with HIGH confidence even without these additional steps.

**"No evidence of wrongdoing" does NOT equal "Evidence of good behavior."**
For a gold-custody protocol making $100M+ market cap claims, the complete absence of verifiable identity, custody arrangements, licensing details, and auditing is itself strong evidence of unacceptable risk. The burden of proof for custody of physical assets is on the custodian — it has not been met.

---

*Report generated under the DeFi Adversarial Research Framework. Not financial advice. This report identifies risks; it does not constitute a legal finding of fraud.*
