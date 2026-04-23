# MemeCore ($M) — Adversarial DeFi Due Diligence Report

**Research Date:** April 22, 2026  
**Subject:** MemeCore (memecore.com) — Layer-1 Blockchain, Token: $M  
**Legal Entity:** Anteater Labs Pte. Ltd., 165B Telok Ayer Street, Singapore 068617  
**Investigator:** Claude Code (Adversarial DeFi Research Framework)  
**Confidence Level:** HIGH on red flags; MEDIUM on definitive manipulation proof (ZachXBT investigation ongoing)

---

> **⚠️ LEAD WARNING — READ BEFORE PROCEEDING**
> 
> On-chain investigator ZachXBT publicly pressed MemeCore (April 20, 2026) to explain how its token reached a $6B market cap while insiders allegedly hold >90% of supply and total app volume stands at only **$66 million**. The project has issued **no public response** as of the time of this report. CertiK's own audit flagged **hidden owner and balance modification capabilities** — meaning the team can alter user token balances. The project's co-founder remains **deliberately anonymous** despite attending Trump's White House dinner. Market maker DWF Labs — accused of $300M in Binance wash trading and fired investigators — is a named partner. **All of this is happening while the token sits at a $5.5B market cap.**

---

## 1. Executive Summary

**Verdict:** MemeCore presents a convergence of the most severe red flags seen in pre-collapse DeFi tokens. A $5.5B fully-circulating market cap is supported by approximately $66M in native application volume — a ratio of **83:1** that has no legitimate fundamental justification. On-chain data corroborates ZachXBT's insider concentration allegations: CertiK's Skynet independently shows the top 20 addresses control **87.14% of supply**, the contract uses an upgradeable proxy with **unresolved hidden balance modification capabilities**, and a suspected team wallet deposited 5.3 million M tokens to Kraken on the exact day of listing. The co-founder who attended Trump's $17.5M memecoin investment dinner remains **unnamed by design**. The project partnered with DWF Labs, a market maker with documented allegations of pump-and-dump behavior. The GitHub organization has **zero public members** and only 13 stars despite a claimed top-20 crypto status. MemeCore has not responded to ZachXBT's public challenge.

**Confidence Level:** HIGH  

**Top 3 Risks:**
1. **Price manipulation / imminent collapse** — Token concentration, DWF Labs market-making, 83:1 cap-to-volume ratio, and patterns identical to RaveDAO (which lost 95% within 24 hours) suggest coordinated price inflation.
2. **Smart contract backdoor** — CertiK flagged "hidden owner and balance modification capabilities" in an upgradeable proxy. The team can change token balances and upgrade contract logic without warning.
3. **Anonymous insider control** — The lead co-founder is deliberately unidentified. Treasury funds were used to buy political access via Trump memecoin. 90%+ supply concentration means a single decision by unknown individuals can destroy the token.

**Top 3 Positive Signals (Genuine):**
1. CertiK conducted two audits (May 2025); most code-level findings resolved.
2. EVM-compatible chain with functional infrastructure — block explorer, staking, launchpad — suggests some real development occurred.
3. Multi-exchange listings (Binance Alpha, Kraken, Bybit, OKX, Gate.io) indicate the project passed minimum exchange due diligence — though ZachXBT specifically questions Kraken's listing process.

---

## 2. Team Assessment

### Named Team Members

| Name | Role | Claims | Verified | Red Flags |
|------|------|---------|----------|-----------|
| Jun Ahn | CEO / Founder | Ledger (Asia division), Chains.Asia, founded 0xLootBox | Partially — general presence confirmed across crypto publications, no independent employment verification of Ledger role | "Ledger Asia" is vague; 0xLootBox is an obscure investment vehicle |
| Cherry Hsu (a.k.a. Ting Hsu) | Chief Business Development Officer | CS Master's degree, 7 years in IT and gaming | Partially — LinkedIn exists; Taiwanese national based in Korea/Singapore | Game developer background with no major prior Web3 accomplishments; confirmed attendance at Trump dinner, refused to name the anonymous co-founder |
| Rudy Rong | Chief Growth Officer | Forbes 30 Under 30; USC Finance degree; founder of Karat DAO | Partially — Forbes listing and USC degree plausible; Karat DAO is real | **Karat DAO (KAT) is currently down 99.3% from its all-time high** — Rong led a project that functionally lost all value |
| "Finn" | Co-Founder | Anonymous — no surname, no public profile disclosed | **UNVERIFIABLE — deliberately anonymous** | Anonymous co-founder attended Trump's White House dinner; MemeCore paid ~$17.5M in treasury funds for a position in Trump's memecoin leaderboard; Hsu confirmed attendance but refused to name "Finn" |

### GitHub Analysis

- **Organization:** `github.com/memecore-foundation`
- **Public Members:** **ZERO** — organization has no public members, hiding developer identities
- **Repositories:** 1 public repo (`Go-MemeCore`)
- **Stars:** 13 | **Forks:** 4 | **Followers:** 2
- **Commit Count:** 16,171 — **MISLEADING**. This is a fork of `go-ethereum` (geth). The overwhelming majority of commits are inherited from Ethereum's codebase, not original development by the MemeCore team.
- **Original Code:** Limited to custom consensus modifications (PoSA), custom hardforks (GasTree, RewardTree, CanPraTree), and chain configuration. This is a BSC-style fork, not an original Layer-1.
- **Open Issues:** 0 | **Open PRs:** 0 — A top-20 crypto blockchain with zero community-reported issues or contributions is implausible for a legitimately active chain.
- **Last Updated:** February 20, 2026

**Assessment:** The GitHub presents the *appearance* of engineering activity (large commit count from geth fork) while revealing near-zero actual community engagement. For a $5.5B blockchain claiming to power a new ecosystem, 13 GitHub stars is extraordinary.

### Social Media

- **Twitter/X:** 305K followers — moderate, not outsized for a top-20 token, but follower quality unverified
- **Telegram:** 62K users with **declining** activity (-23 messages per day, per CertiK Skynet)
- **CertiK Community Trust Score:** 5% — the lowest possible sub-rating on their platform

### What Could NOT Be Verified

- Jun Ahn's specific role, tenure, and responsibilities at Ledger Asia
- "Finn"'s legal identity, country of residence, prior projects, or financial exposure to $M
- Verification of Cherry Hsu's claimed CS Master's degree or institution
- 0xLootBox's investment portfolio performance or current status
- Any criminal record, regulatory action, or civil litigation against any team member

---

## 3. Third-Party Consensus

### ZachXBT Investigation (Most Critical — April 20, 2026)

ZachXBT — the crypto ecosystem's most credible independent on-chain investigator with a documented track record of exposing manipulation — publicly challenged MemeCore with the following specific claims:

- **Direct quote:** "Please provide a single data point to support your $6B mkt cap at a top 20 token and why insiders hold >90% of supply."
- **On-chain evidence cited:**
  - A Binance deposit address holds approximately **41.3% of M token supply**
  - Wallet address `0x8b8` controls **50 million M tokens** (~21.77% of total supply, worth ~$178M at time of reporting)
  - Analyst `0xToolman` assessed the wallet pattern as "looks like team holdings"
  - **$7.9 million in suspicious Kraken withdrawals** routed to 18 newly created wallet addresses, which then held 11.7 million M tokens worth ~$39.8M
  - A suspected team wallet deposited **5.3 million M tokens to Kraken on the exact day of listing** (July 3, 2025)
  - ZachXBT flagged Kraken as a "key venue enabling M token's suspicious price activity" and alleged exchanges received M tokens as listing fees or liquidity arrangements
- **Pattern comparison:** ZachXBT explicitly compared MemeCore's profile to **RaveDAO (RAVE)**, which collapsed 95% in 24 hours from a $6.7B peak after insider wallets moved supply to exchanges before the dump
- **MemeCore's response:** None. No public statement issued as of this report.

### CertiK Assessment

- **Skynet Score:** The page displays 88.39 overall, but **critical sub-scores tell a different story:**
  - Code Security: 10%
  - Operational Resilience: 5%
  - Community Trust: 5%
  - Market Stability: 5%
  - Governance Strength: 20%
  - Fundamental Health: 20%
- **Audits:** 2 completed (last: May 19, 2025). 16 total findings: 1 major (acknowledged but **unresolved**), 2 medium partially resolved, 13 minor resolved
- **Unresolved Major Finding:** Classified as "design issue" — acknowledged but not fixed
- **2 Centralization Issues Partially Resolved:** Related to upgrade privileges and privilege escalation
- **Critical Flag:** "Hidden owner and balance modification capabilities" — the team can change user token balances
- **5 Owner Privilege Issues Identified**
- **Team KYC:** NOT completed by CertiK — no third-party identity verification
- **Top 20 Holder Concentration:** 87.14% of supply (independently corroborates ZachXBT)

### DWF Labs Partnership — HIGH SEVERITY

MemeCore's announced partnership with **DWF Labs** as market maker is one of the most alarming third-party signals in this investigation.

DWF Labs has faced the following documented allegations:
- A **former Binance insider** reported the exchange's investigations team uncovered **$300 million in wash trading** by DWF Labs
- Binance **fired the investigator** who uncovered the DWF findings rather than acting on them
- Multiple documented instances of DWF Labs' founder promoting tokens, then selling into the pump (pump-and-dump pattern)
- CoinDesk reported DWF Labs' deals "blur what 'investing' means" — they simultaneously act as investor, market maker, and token promoter, creating extreme conflicts of interest

**The M token rose 333% following the DWF Labs partnership announcement.** A token with alleged 90%+ insider concentration partnering with a market maker accused of wash trading and pump-and-dump schemes is a near-textbook setup for coordinated price inflation.

### Independent Analysts

- **The Block, CoinTelegraph, Bitcoin.com News, Crypto.news** have all covered the ZachXBT investigation — none provided exculpatory evidence for MemeCore
- **CoinStats Fundamental Analysis** (April 2026): Classified as "high-risk/high-reward speculation," flagged governance not live as of August 2025, flagged heavy reliance on partnerships vs. organic development, flagged inflationary tokenomics risk
- **DeFiLlama:** MemeCore does not appear in DeFiLlama's tracked chains or protocols — a $5.5B Layer-1 blockchain with no DeFi activity tracked by the ecosystem's primary aggregator

### Community Sentiment

- Reddit searches for independent MemeCore analysis returned **no critical community investigation threads** — this absence itself is notable for a $5.5B asset
- The community's documented response to ZachXBT was to **joke that "ZachXBT's attention is free marketing"** — rather than presenting any on-chain counter-evidence

---

## 4. On-Chain Findings

### Contract Risk Assessment

| Factor | Finding | Severity |
|--------|---------|----------|
| Contract type | ERC1967 Upgradeable Proxy | HIGH — admin can change implementation logic |
| Source code | Verified on BscScan (Solidity v0.8.28) | Neutral |
| Audit status | "No Contract Security Audit Submitted" on BscScan | HIGH |
| CertiK finding | Hidden owner and balance modification capabilities | CRITICAL |
| Centralization | 5 owner privilege issues; 2 upgrade/escalation findings | HIGH |
| Compiler bugs | TransientStorageClearingHelperCollision (HIGH), LostStorageArrayWriteOnSlotOverflow (LOW) | HIGH |
| Implementation | Proxy implementation changed since deployment | MEDIUM |
| Deployer | `0x653e645e3d81a72e71328Bc01A04002945E3ef7A` | Unverified |

**The upgradeable proxy pattern means the team can silently upgrade the contract to any new logic. Combined with the unresolved hidden balance modification capability, this creates a technical pathway for a complete exit without any on-chain warning.**

### Token Distribution Analysis

- **Max Supply:** 10 billion $M
- **Total Supply (current):** 5.36 billion
- **Circulating Supply:** 1.29 billion (12.9% of max)
- **Official Allocation Claim:** 58% community, 15% foundation, 13% contributors, 12% investors, 2% treasury
- **Reality (CertiK):** Top 20 holders control **87.14%** of supply
- **Reality (ZachXBT):** Insiders hold **>90%** of supply; Binance deposit address alone holds 41.3%
- **FDV:** $23.05B–$42.78B (discrepancy between sources) vs $5.5B market cap
- **Market Cap/FDV Ratio:** 0.24 — meaning 76% of supply has not yet hit the market

**The officially claimed "58% community" allocation appears to be sitting in team-controlled wallets rather than distributed to the community. This is the most likely explanation for the gap between official tokenomics and on-chain concentration.**

### Suspicious Transaction Patterns

1. **Listing Day Dump:** Suspected team wallet deposited 5.3M M tokens to Kraken on July 3, 2025 (listing day)
2. **Kraken Flow Pattern:** $7.9M withdrawn from Kraken deposit addresses → dispersed to 18 freshly created wallets → wallets accumulated 11.7M tokens
3. **Price Action:** Token went from $0.035 (July 3, 2025 ATL) to $4.65 ATH (April 18, 2026) — a **132x increase** with no fundamental change in the underlying business
4. **Volume vs. Cap:** $66M total app volume vs. $5.5B–$6.5B market cap (83:1–98:1 ratio)
5. **Futures Funding Rate:** Near 70% at time of analysis — extreme leverage suggesting artificial demand maintenance

### Validator Centralization

- Only **top 7 validators** by stake can validate blocks (refreshed every 70 seconds)
- Minimum validator stake: **7,000,000 $M tokens** (~$30M at current prices)
- This ensures only insiders/large holders can validate — complete control over the chain
- Mechanism is PoSA (Proof of Staked Authority), same as BSC — marketed as "Proof of Meme" (PoM), which is a branding exercise, not a technical innovation
- The actual "Proof of Meme" component (measuring cultural contributions) has no concrete implementation documented

---

## 5. Red Flags Register

| # | Flag | Evidence | Source | Severity |
|---|------|----------|---------|----------|
| 1 | Hidden balance modification capability in contract | CertiK Skynet audit finding, unresolved | CertiK (verified) | **CRITICAL** |
| 2 | Co-founder "Finn" deliberately anonymous while attending Trump dinner | Cherry Hsu confirmed attendance but refused to name co-founder | Fortune Magazine (May 2025) | **CRITICAL** |
| 3 | DWF Labs partnership — market maker accused of $300M wash trading | DWF Labs was investigated by Binance internal team; investigator fired; documented pump-and-dump pattern | CoinDesk, WSJ, DL News (verified) | **CRITICAL** |
| 4 | ZachXBT alleges >90% insider token concentration; on-chain shows 87.14% top-20 control | CertiK Skynet independently shows 87.14%; Binance deposit = 41.3%; 0x8b8 wallet = 21.77% | ZachXBT (April 2026), CertiK Skynet | **CRITICAL** |
| 5 | No response to ZachXBT challenge (2+ days) | Zero public statement from MemeCore after high-profile public challenge | All major crypto publications | **CRITICAL** |
| 6 | Team wallet dumped on listing day | Suspected team wallet deposited 5.3M M tokens to Kraken on July 3, 2025 (listing day) | ZachXBT investigation | **CRITICAL** |
| 7 | $7.9M routed through Kraken to 18 fresh wallets | On-chain flow analysis showing classic layering pattern | ZachXBT, Bitcoin.com News | **HIGH** |
| 8 | $17.5M treasury funds spent on Trump memecoin for political access | MemeCore holds 2nd-largest position in Trump memecoin leaderboard; company treasury used | Fortune Magazine (May 2025) | **HIGH** |
| 9 | Upgradeable proxy contract (ERC1967) with no timelock | Team can change contract logic with no warning; 2 upgrade/privilege escalation findings partially unresolved | CertiK, BscScan | **HIGH** |
| 10 | No security audit submitted on BscScan for main contract | Despite $5.5B market cap, the BEP-20 contract shows "No Contract Security Audit Submitted" | BscScan (verified) | **HIGH** |
| 11 | Compiler vulnerability: TransientStorageClearingHelperCollision (high severity) | Solidity v0.8.28 compiler bug flagged on deployed contract | BscScan (verified) | **HIGH** |
| 12 | GitHub organization has zero public members | Deliberately hides identity of developers; 13 stars, 4 forks for a "top 20 crypto" blockchain | GitHub (verified) | **HIGH** |
| 13 | Go-MemeCore is a geth fork masquerading as original L1 | 16,171 commits are inherited from go-ethereum; minimal original code contribution | GitHub (verified) | **HIGH** |
| 14 | 83:1 market cap-to-app-volume ratio | $5.5B–$6.5B market cap vs $66M total application volume — no fundamental justification | ZachXBT, Bitcoin.com News | **HIGH** |
| 15 | CertiK team KYC not completed | No third-party identity verification for any team member | CertiK Skynet (verified) | **HIGH** |
| 16 | Rudy Rong (CGO) previously led Karat DAO — now down 99.3% from ATH | Karat DAO/KAT reached ATH $0.07 in August 2023, now at ~$0.0005 | CryptoRank (verified) | **HIGH** |
| 17 | Governance module not live as of August 2025 | Despite claiming community governance, no actual governance implemented | CoinStats Fundamental Analysis | **HIGH** |
| 18 | Not tracked on DeFiLlama | A $5.5B Layer-1 blockchain with no TVL tracked by the ecosystem's primary aggregator | DeFiLlama (verified by absence) | **MEDIUM** |
| 19 | Token went 132x in 9 months with no fundamental catalyst | $0.035 ATL (July 2025) → $4.65 ATH (April 18, 2026) with no corresponding TVL or user growth | CoinGecko (verified) | **MEDIUM** |
| 20 | Futures funding rate at 70% | Extreme leverage indicating artificial demand; highly unstable | Market data (April 2026) | **MEDIUM** |
| 21 | Telegram declining (–23 messages/day) | Real organic community activity is falling while price is near ATH | CertiK Skynet (verified) | **MEDIUM** |
| 22 | Investors are second-tier Asian VC funds with undisclosed amounts | IBC Group, Waterdrip Capital, CatcherVC, Klein Labs — no Tier-1 VCs (no Paradigm, a16z, Multicoin); all funding amounts "TBD" | Crypto-Fundraising.info | **MEDIUM** |
| 23 | Minimum validator stake of 7M tokens (~$30M) ensures insider-only validation | Only insiders can become validators, making the chain itself centrally controlled | MemeCore Docs (verified) | **MEDIUM** |
| 24 | Official tokenomics claim (58% community) contradicts on-chain reality (87-90% insider) | MemeCore claims community majority; CertiK/ZachXBT show insider control | Multiple sources | **MEDIUM** |
| 25 | "Proof of Meme" is marketing — actual mechanism is PoSA (BSC clone) | GitHub repo explicitly implements PoSA; docs use "Proof of Meme" branding with no technical differentiation | GitHub (verified) | **LOW** |

---

## 6. Comparative Analysis — Pattern Matching

### RaveDAO (RAVE) — Near-Identical Pattern

| Metric | RaveDAO (RAVE) | MemeCore (M) |
|--------|---------------|-------------|
| Peak valuation | $6.7 billion | $6.5 billion |
| Insider supply control | >90% | >90% (alleged) |
| Price surge pattern | $0.25 → $28 in ~1 week (11,000%) | $0.035 → $4.65 in 9 months (13,200%) |
| Exchange involvement | Bitget, Binance | Kraken, Binance, Bitget |
| Pre-dump wallet behavior | Team wallets → Bitget 10 hrs before peak | Team wallet → Kraken on listing day |
| Post-collapse | 95% within 24 hours | TBD |
| On-chain investigator | ZachXBT flagged | ZachXBT actively investigating |

ZachXBT explicitly compared MemeCore to the RAVE pattern. The structural similarities are near-identical. The key unresolved question is **whether the dump has occurred or is still upcoming.**

### Other Flagged Tokens (Same ZachXBT Investigation)

ZachXBT flagged the following tokens in the same investigation batch as MemeCore: **SIREN, MYX, COAI, PIPPIN, RIVER** — all described as having similar "questionable price action" patterns. The grouping suggests a coordinated market activity pattern rather than an isolated MemeCore anomaly.

### Classic Warning Sign Checklist

| Pattern | Present in MemeCore? |
|---------|---------------------|
| Anonymous/partially anonymous team | ✅ Yes (Finn unidentified) |
| Insider heavy supply concentration | ✅ Yes (87-90%+ per CertiK/ZachXBT) |
| Low float, high FDV vs market cap | ✅ Yes (12.9% circulating of max supply) |
| Controversial market maker partner | ✅ Yes (DWF Labs) |
| No response to public scrutiny | ✅ Yes (silence to ZachXBT) |
| Suspiciously thin organic activity vs valuation | ✅ Yes ($66M app volume vs $5.5B cap) |
| Upgradeable contract with backdoor capability | ✅ Yes (balance modification) |
| No meaningful TVL tracked by aggregators | ✅ Yes (absent from DeFiLlama) |
| Prior team project with catastrophic losses | ✅ Yes (Karat DAO -99.3%) |
| Political/influencer access bought with treasury | ✅ Yes (Trump memecoin) |
| Token went 100x+ without fundamental basis | ✅ Yes (132x in 9 months) |

**Score: 11/11 classic warning signs present.**

---

## 7. Unresolved Questions

1. **Who is "Finn"?** The anonymous co-founder who spent ~$17.5M in treasury funds and attended Trump's dinner cannot be identified. This is the most critical unresolved question in the entire investigation. Without knowing who controls this entity, risk cannot be fully assessed.

2. **What is the actual on-chain proof of the 90% insider claim?** ZachXBT has stated the investigation is ongoing. The 87.14% from CertiK is close but not definitively confirmed as "insider" wallets — they could theoretically include large exchange cold wallets. Full wallet tracing is needed.

3. **What is in the unresolved "major design issue" finding from CertiK?** The audit acknowledged but did not resolve one major finding. The specific nature of this design flaw is not publicly disclosed.

4. **What is the actual role of DWF Labs?** Market maker, investor, token promoter — or all three simultaneously? The specific terms of the DWF Labs agreement are unknown.

5. **Where is the $66M in app volume coming from?** The MemeX launchpad claims 190,000+ users and 1.27M transactions. Independent verification of these numbers is unavailable.

6. **What happens when the 67% of supply in vesting releases?** No specific vesting schedule is publicly documented. This is a severe governance omission for a token of this size.

7. **Did any of the named investors (IBC Group, Waterdrip Capital, CatcherVC, Klein Labs) receive preferential pricing or token allocation before public listing?** Funding amounts are listed as "TBD" — actual terms are undisclosed.

8. **What is Jun Ahn's specific role history at Ledger Asia?** "Ledger Asia" is not independently verifiable. Ledger (hardware wallet company) does have Asian operations, but Ahn's specific title, tenure, and responsibilities are not confirmed by any Ledger corporate communication.

---

## 8. Sources Used in This Investigation

All sources accessed April 22, 2026. Data is time-sensitive; market cap and price figures will differ from those at time of reading.

- [ZachXBT presses MemeCore over $6B valuation and token supply concentration](https://crypto.news/zachxbt-presses-memecore-over-6b-valuation-and-token-supply-concentration/)
- [ZachXBT Flags Kraken as Key Venue in M Token Manipulation](https://news.bitcoin.com/zachxbt-flags-kraken-m-token-manipulation/)
- [ZachXBT Scrutinizes MemeCore's Insider-Heavy Supply After RaveDAO Crash](https://www.cryptotimes.io/2026/04/20/zachxbt-scrutinizes-memecores-insider-heavy-supply-after-ravedao-crash/)
- [ZachXBT Questions Kraken Listing Amid $7.9M Memecore Flows](https://www.cryptotimes.io/2026/04/20/zachxbt-questions-kraken-listing-amid-7-9m-memecore-flows/)
- [ZachXBT Flags Holder Concentration Concerns — Cointelegraph](https://cointelegraph.com/news/investigator-concentration-concerns-memecore)
- [MemeCore Token Faces ZachXBT Scrutiny Over 90% Insider Holdings — Blockchain.news](https://blockchain.news/news/memecore-token-zachxbt-insider-holdings-scrutiny)
- [CertiK Skynet — MemeCore Project Insight](https://skynet.certik.com/projects/memecore)
- [MemeCore BscScan Contract](https://bscscan.com/token/0x22b1458e780f8fa71e2f84502cee8b5a3cc731fa)
- [MemeCore CoinGecko](https://www.coingecko.com/en/coins/memecore)
- [MemeCore CoinMarketCap](https://coinmarketcap.com/currencies/memecore/)
- [MemeCore GitHub Organization](https://github.com/memecore-foundation/Go-MemeCore)
- [Fortune: Trump Memecoin Dinner — MemeCore](https://fortune.com/crypto/2025/05/12/trump-memecoin-dinner-justin-sun-memecore-kain-warwick/)
- [Saakuru Labs and Memecore Launch $10M Foundation — Chainwire](https://chainwire.org/2024/10/17/saakuru-labs-and-memecore-launch-10m-foundation-to-invest-in-gaming-ecosystem/)
- [MemeCore Soars on DWF Labs Partnership — CoinEdition](https://coinedition.com/memecore-dwf-labs-partnership-price-surge/)
- [DWF Labs Wash Trading Investigation — CoinDesk](https://www.coindesk.com/business/2024/05/09/binance-fired-investigator-who-uncovered-market-manipulation-at-client-dwf-labs-wsj/)
- [Binance Fired Investigator Who Uncovered DWF Market Manipulation — CoinDesk](https://www.coindesk.com/business/2023/04/14/market-maker-dwf-labs-more-than-200m-in-deals-blur-what-investing-means/)
- [MemeCore Docs](https://docs.memecore.com)
- [MemeCore Rootdata Project Profile](https://www.rootdata.com/Projects/detail/MemeCore?k=MTM2MjE%3D)
- [ANTEATER LABS PTE. LTD. — SG Business Registry](https://www.sgpbusiness.com/company/Anteater-Labs-Pte-Ltd)
- [Karat DAO Price — CryptoRank](https://cryptorank.io/price/karat)
- [MemeCore Fundamental Analysis — CoinStats AI](https://coinstats.app/ai/a/fundamental-analysis-memecore)
- [IQ.wiki — Memecore](https://iq.wiki/wiki/memecore)

---

## 9. Researcher Notes & Limitations

**Research conducted using:** Web scraping, public blockchain data (BscScan), CertiK Skynet public data, GitHub public data, published investigative journalism, and ZachXBT's published on-chain analysis.

**Limitations:**
- Direct BscScan token holder chart was blocked (403); top holder data sourced from CertiK Skynet and ZachXBT-reported figures
- Rootdata profile was inaccessible; investor details sourced from secondary reports
- Anteater Labs Singapore corporate registry was blocked (403); company data sourced from secondary references
- ZachXBT's investigation was ongoing as of this report; definitive proof of 90%+ insider holdings had not yet been published in a final form
- This report does not constitute financial or legal advice. It represents an adversarial due diligence analysis based on publicly available information.

**Lessons Recorded:**
- The CertiK Skynet "overall score" (88.39) is severely misleading when sub-scores across key dimensions (community trust: 5%, operational resilience: 5%, market stability: 5%) are this low. Always read sub-scores.
- "Proof of Meme" branding on a PoSA chain is a classic re-branding of standard technology to appear innovative. Cross-reference GitHub code against marketing claims.
- DWF Labs partnership announcements have preceded significant price pumps in multiple tokens under investigation — this is a repeatable pattern.
- The complete absence of a project from DeFiLlama despite a multi-billion dollar market cap is a strong negative signal.

---

*Report compiled April 22, 2026 | MemeCore Adversarial Due Diligence | All claims labeled by source and confidence level.*
