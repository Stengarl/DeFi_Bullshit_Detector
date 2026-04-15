# Supernova.xyz — Adversarial Due Diligence Report

**Date of Investigation:** April 11, 2026  
**Investigator Stance:** Guilty until proven innocent  
**Confidence Level:** Medium-High (limited by inability to verify on-chain burn claims and multisig configurations)  
**Report Status:** Complete

---

## ⚠️ LEAD FINDING — READ BEFORE PROCEEDING

The NOVA token launched February 18–19, 2026. It hit an ATH of $1.27. As of this investigation it trades at approximately $0.006–$0.01. **That is a -99.2% to -99.5% decline in approximately 7 weeks.** The FDV is ~$572,000. There are 1,551 token holders. Daily trading volume is ~$27,000.

The predecessor project, Blackhole DEX ($BLACK on Avalanche), was launched by the same team in July 2025 and similarly collapsed from an ATH of $1.53 to ~$0.016 — a -96.2% decline. Same team. Identical pattern. No credible public explanation for either collapse has been published.

---

## 1. Executive Summary

**Verdict:** Supernova.xyz is a technically real, audited DEX on Ethereum with publicly identified founders. It is not an anonymous shell project, and no evidence of a contract exploit or liquidity drain was found. However, it exhibits a pattern of behavior that has destroyed retail value in two consecutive projects:

1. A high-profile influencer launch with aggressive community hype
2. A rapid token price pump driven by the founders' combined 3M+ social media following
3. A near-total token price collapse (96–99%) with no public accountability

The founders have documented histories of promoting tokens that subsequently collapsed, and one is connected to a multi-influencer paid-promotion investigation. The protocol's tokenomics include unverified burn claims and a team-controlled swap pause mechanism. The project's TVL ($4.8M) and token liquidity ($27K/day) are negligible for an Ethereum DEX, indicating the market has already passed judgment.

**Confidence Level:** Medium-High  
**Top 3 Risks:**
1. Team history strongly suggests a pattern of influencer-driven token distribution followed by collapse
2. Team retains unilateral power to pause all swap functions (audit-confirmed)
3. Token burn and team allocation claims have not been independently verified on-chain

**Top 3 Positive Signals:**
1. Both founders are publicly doxxed — no anonymous team
2. One legitimate security audit completed (Paladin, Feb 2026) with all High/Medium findings resolved
3. Built on battle-tested Solidly/Thena codebase with prior Code4rena audit on the Avalanche predecessor

---

## 2. Team Assessment

### 2.1 Elliot Wainman ("EllioTrades")

**Role:** Co-founder of Blackhole DEX (Avalanche, July 2025) and by lineage, Supernova.xyz  
**Twitter/X:** [@elliotrades](https://x.com/elliotrades) — 700K+ followers  
**Background (VERIFIED):** UC Santa Barbara graduate. Crypto YouTuber. Co-founded Neo Tokyo NFT project with Alex Becker. Founded SuperFarm, later rebranded to SuperVerse ($SUPER).

**Prior Projects — Red Flags:**

**SuperFarm → SuperVerse ($SUPER)**
- [VERIFIED] $SUPER token launched early 2021, reached ATH of ~$4.73, collapsed ~98% to ~$0.10 as of this investigation — nearly five years later.
- [VERIFIED] The project was rebranded from SuperFarm to SuperVerse. Independent critics note the rebrand followed community criticism and failed roadmap items including a P2E game ("Impostors") that raised ~$60M selling 10,000 NFTs and remained in indefinite beta.
- [PARTIALLY VERIFIED] Wainman's name appears in a leaked document naming 200+ influencers involved in undisclosed paid cryptocurrency promotion. Source: [Blocmates influencer leak](https://www.blocmates.com/news-posts/200-influencers-named-in-paid-crypto-promotion-leak-few-disclosed-ads). His specific payments were not confirmed.
- [PARTIALLY VERIFIED] Leaked screenshots allegedly connected EllioTrades to a coordinated promotional campaign around $SUPER that involved MrBeast receiving 1M tokens and selling them within 24 hours for ~1,900 ETH. Source: [Benzinga](https://www.benzinga.com/content/41638540/investigation-connects-mrbeast-with-50-crypto-wallets-tied-to-insider-trading-allegations), [IBTimes](https://www.ibtimes.com/mrbeast-linked-wallet-involved-pump-dump-crypto-token-projects-3746725). **Whether EllioTrades personally held and sold $SUPER during promotional activity was NOT independently verified in this investigation.**

**What Could NOT Be Verified:**
- His GitHub contribution history for Supernova/Blackhole repos (no public GitHub profile linking to these projects surfaced)
- Whether he is a hands-on developer vs. a marketing/community co-founder
- Specific wallet addresses associated with him for on-chain transaction analysis

---

### 2.2 Alex Becker ("ZssBecker")

**Role:** Co-founder of Blackhole DEX and by lineage, Supernova.xyz  
**Twitter/X:** [@ZssBecker](https://x.com/ZssBecker) — 2.6M+ followers  
**Background (VERIFIED):** Entrepreneur. Founded Hyros (ad tracking SaaS), acquired for ~$110M. Co-founded Neo Tokyo NFT with EllioTrades. Active crypto/meme coin streamer on PumpFun.

**Prior Projects — Red Flags:**

- [VERIFIED] Publicly promoted Peanut the Squirrel ($PNUT) meme coin. Token subsequently crashed ~90%. Whether Becker held and sold during promotion: **UNVERIFIED**.
- [VERIFIED] Becker launched STRSZN token on PumpFun in 2025. It reached a $17M+ market cap within 10 minutes and generated $304,000 in creator fees. Long-term price performance: not tracked in this investigation but consistent with PumpFun's median outcome.
- [VERIFIED via multiple independent sources] Multiple consumer watchdog sites and independent crypto analysts document a consistent pattern: Becker promotes projects to his audience; projects subsequently decline; Becker faces refund complaints and fraud allegations. Sources: [FinanceScam dossier](https://www.financescam.com/dossier/alex-becker/), [Bitkan analysis](https://bitkan.com/learn/how-much-is-alex-becker-s-net-worth-is-alex-becker-a-scam-artist-or-fraud-12964).
- [VERIFIED — Becker's own tweet] On February 16, 2024 Becker tweeted: *"crypto is PvP and at some time in the future we will all try to dump savagely on each other n book it for the exit. Leaving only 5-10% of people with profit n everyone else rekted."* Source: [@ZssBecker/1759688968621211833](https://x.com/ZssBecker/status/1759688968621211833). This is his stated worldview.
- [VERIFIED] No formal SEC charges, criminal proceedings, or regulatory enforcement actions documented as of this investigation.

**What Could NOT Be Verified:**
- Specific developer contributions to Blackhole or Supernova code
- Whether Becker held NOVA or BLACK tokens at launch and their subsequent disposal

---

### 2.3 Team Structure Overall

- **Doxxed:** Yes — both principals are publicly identified. This is a positive signal vs. anonymous teams.
- **Developer capacity:** Both founders appear primarily to be influencer-marketers, not protocol engineers. The actual engineering team is not publicly named in any documentation reviewed. This is a governance opacity concern.
- **Track record pattern:** SuperVerse ($SUPER, -98%), Blackhole ($BLACK, -96.2%), Supernova ($NOVA, -99.2%). Three consecutive influencer-promoted tokens with catastrophic declines. The sample size is now sufficient to constitute a pattern.

---

## 3. Third-Party Intelligence

### 3.1 Independent Analyst Coverage

- **The Defiant:** No coverage of supernova.xyz found.
- **DL News:** No coverage of supernova.xyz found.
- **Rekt.news:** No entry found. (Not an exploit; not yet a writeup.)
- **Token Metrics:** Published a [Blackhole deep dive](https://research.tokenmetrics.com/p/deep-dive-blackhole-avalanche-s-gravity-defying-dex-469b) — this is a paid research service, not adversarial coverage.
- **Cookout Club (Cryptomancer, Substack):** Published a [pre-launch analysis](https://cookoutclub.substack.com/p/supernova-blackholes-ethereum-expansion) noting BLACK "is down significantly from its July highs" and flagging execution risk and competition. Most substantive independent piece found.

**Assessment:** The absence of coverage from adversarial DeFi media (Rekt, The Defiant, DL News) is not exculpatory — it reflects that the project is too small and too dead to attract their attention. The near-zero token liquidity means there is little left to investigate.

### 3.2 Audit and Security Assessment

**Audit: Paladin Blockchain Security**
- Date: February 14, 2026
- Scope: 24 smart contracts
- Report: [Public PDF](https://resources.supernova.xyz/Paladin_Supernova_Final_Report.pdf)
- Project page: [paladinsec.co/projects/supernova](https://paladinsec.co/projects/supernova/)

| Severity | Found | Resolved | Partially Resolved | Acknowledged Only |
|---|---|---|---|---|
| Governance | 3 | 0 | 0 | **3** |
| High | 3 | **3** | 0 | 0 |
| Medium | 3 | **3** | 0 | 0 |
| Low | 24 | 16 | 1 | 7 |
| Informational | 35 | 13 | 7 | 15 |
| **TOTAL** | **68** | **35** | **8** | **25** |

**Key Audit Findings:**
1. **CENTRALIZATION RISK (Acknowledged, Not Resolved):** *"The swap functions can be blocked or paused by the SuperNova team."* Any contract or protocol building on top of Supernova must account for this unilateral team power.
2. **Circulating Supply Manipulation (Low/Acknowledged):** `MinterUpgradeable.circulating_supply()` can be gamed via a 1-second stake duration, allowing misrepresentation of supply metrics.
3. **Governance Issues (3x Acknowledged, Not Resolved):** Three governance-classified findings were acknowledged without modification. The specific nature of these findings was not obtainable from public sources; the PDF audit is binary-encoded.

**Audit Assessment:**
- Positive: All 3 High and all 3 Medium findings were resolved before launch.
- Concern: Only a single audit firm engaged. Three governance findings left unresolved.
- Concern: The audit was completed Feb 14, 2026 — four days before mainnet launch. Very compressed timeline.
- Concern: The team's claimed Blackhole audits (Avalanche chain) included Code4rena ([github.com/code-423n4/2025-05-blackhole](https://github.com/code-423n4/2025-05-blackhole)), but this audit history has NOT been formally cross-referenced to the Supernova Ethereum deployment.

**CertiK Skynet:** Supernova appears on CertiK's monitoring platform but no formal audit score was surfaced in search results.

### 3.3 Community Sentiment

- **Reddit:** Zero relevant threads found on r/CryptoCurrency, r/DeFi, or r/ethfinance about supernova.xyz. This is not exculpatory — the community did not materially engage with this project.
- **Twitter/X:** Discussion is dominated by the founders' own promotional posts and community members holding veNFTs. No independent critical analysis surfaced.
- **DeFi Forum coverage:** None found on governance forums of adjacent protocols (Aave, Compound, Morpho).
- **Competitor commentary:** Aerodrome and Velodrome (main ve(3,3) competitors) are merging into a new Ethereum-native DEX ("Aero") in Q2 2026, directly competing with Supernova's positioning. No competitor commentary specifically about Supernova surfaced.

---

## 4. On-Chain Findings

### 4.1 Contract Risk Assessment

**NOVA Token Contract**
- Address: `0x00Da8466B296E382E5Da2Bf20962D0cB87200c78`
- Chain: Ethereum mainnet
- Verified: Yes (Etherscan, Source Code Verified)
- Compiler: Solidity v0.8.13
- Standard: ERC-20, no upgrade proxy detected
- Decimals: 18
- **Minter Role Present:** The contract contains a minter role for token creation. Who controls this role is not publicly documented. This is an unresolved centralization risk.

**GaugeManager Contract**
- Address: `0x19a410046afc4203aece5fbfc7a6ac1a4f517ae2`
- Whether this is protected by a multisig or timelock is not publicly documented. Requires direct Etherscan verification.

**MinterUpgradeable**
- Address not publicly disclosed in documentation reviewed.
- This is an upgradeable contract (Paladin audit confirmed its existence). Whether upgrade authority is protected by a multisig or timelock is unknown.

**⚠️ SCAM TOKEN WARNING**
A separate contract at `0x67fc91510dbb31a3dd72f3f0c8b2581c8c39fda2` is flagged by [LSR Finance](https://desk.lsr.finance/asset/nova-supernova/) as a NOVA impersonator/phishing contract. It contains an airdrop function that transfers ETH to arbitrary addresses. **This is NOT the legitimate Supernova token.** Any user who received unsolicited "NOVA" tokens should verify the contract address before interacting.

**Codebase Lineage (Fork Chain):**
```
Solidly (Andre Cronje, Fantom) 
  → Thena v2 (BNB Chain) 
    → Blackhole DEX (Avalanche, July 2025) 
      → Supernova (Ethereum, February 2026)
```
This is a material fact: the protocol is not novel DeFi infrastructure. It is a fork of a fork of a fork of Solidly. The original Solidly failed catastrophically after Andre Cronje left the space.

### 4.2 Token Distribution Analysis

**CLAIMED (from official docs — not independently verified on-chain):**
- Total minted: 500,000,000 NOVA
- Burned at launch: 450,000,000 NOVA (90%)
- Circulating at launch: 50,000,000 NOVA
  - 10M → Initial liquidity pool
  - 40M → Voter incentives
- Community airdrop via Supermassive veNFTs: 132M burned to create airdrop veNFTs
  - 8M (Cosmic Ignition program)
  - 20M (Warp Speed participants)
  - 104M (veBLACK holders from Avalanche)
- Team/Foundation allocation: Supermassive veNFTs only (claim: no sellable NOVA)

**ADVERSARIAL FLAGS:**
1. The claim that 450M+ tokens were permanently burned has NOT been independently verified against burn address transactions in this investigation. Users should verify burn transactions on Etherscan before trusting stated circulating supply figures.
2. The "Supermassive veNFTs are permanently locked" claim relies on the smart contract enforcing this. If the MinterUpgradeable or governance contracts have upgradeable admin authority, this guarantee could theoretically be reversed.
3. On-chain supply (Etherscan): 54,880,215 NOVA — different from the stated 50M circulating at launch, indicating emissions have already occurred or the initial figures were approximate.

### 4.3 Suspicious Patterns Identified

**Token Price Pattern — Most Alarming Finding:**

| Metric | BLACK (Blackhole, Avalanche) | NOVA (Supernova, Ethereum) |
|---|---|---|
| Launch | July 2025 | February 18, 2026 |
| ATH | $1.53 (July 18, 2025) | $1.27 (February 19, 2026) |
| ATH timing | ~1-2 days after launch | ~1 day after launch |
| Current price | ~$0.016 | ~$0.006–$0.01 |
| Decline from ATH | **-96.2%** | **-99.2% to -99.5%** |
| Current TVL | Unknown (from $255M peak) | $4.8M |
| FDV now | Negligible | ~$572K |

Both tokens peaked within 24–48 hours of launch and have declined near-totally. This pattern is consistent with:
- (a) organic speculation and subsequent unwinding as early adopters exit, OR
- (b) structured distribution to retail at peak, OR
- (c) a combination of both

**No independent on-chain analysis of team/founder wallet behavior was conducted in this investigation.** This is the highest-priority remaining research gap.

**TVL Context:**
- Supernova current TVL: $4.8M
- Aerodrome (Base, ve(3,3) competitor): ~$476M
- The TVL gap to the leading ve(3,3) protocol is 99x. Supernova's $4.8M TVL on Ethereum mainnet is a rounding error in the DeFi ecosystem.

---

## 5. Red Flags Register

| # | Flag | Evidence | Source | Severity |
|---|---|---|---|---|
| 1 | NOVA token -99.2–99.5% from ATH in ~7 weeks | Price data from CryptoRank, DEXTools | [CryptoRank](https://cryptorank.io/price/supernova-dex) | **CRITICAL** |
| 2 | BLACK token -96.2% from ATH — same team, same pattern | Price data from CoinGecko | [CoinGecko](https://www.coingecko.com/en/coins/blackhole) | **CRITICAL** |
| 3 | Phishing/scam impersonator NOVA token at 0x67fc91... exists | LSR Finance scam flag | [LSR Finance](https://desk.lsr.finance/asset/nova-supernova/) | **CRITICAL** (user risk) |
| 4 | Team can pause/block all swap functions unilaterally | Paladin audit finding, "Acknowledged" | [Paladin Report](https://resources.supernova.xyz/Paladin_Supernova_Final_Report.pdf) | **HIGH** |
| 5 | EllioTrades connected to SuperFarm $SUPER (-98%) and influencer paid-promotion investigation | Benzinga, Blocmates, IBTimes | Multiple | **HIGH** |
| 6 | Alex Becker documented history of promoting tokens that crash; admits PvP worldview | Multiple independent sources + his own tweets | [FinanceScam](https://www.financescam.com/dossier/alex-becker/) | **HIGH** |
| 7 | NOVA minter role: who controls mint authority is undisclosed | Etherscan contract analysis | Etherscan | **HIGH** |
| 8 | MinterUpgradeable admin/multisig configuration unknown | Paladin audit + docs | Audit report | **MEDIUM-HIGH** |
| 9 | 450M+ NOVA burn claims not independently verified on-chain | Official docs only | Self-reported | **MEDIUM** |
| 10 | 3 Governance audit findings "Acknowledged" but not resolved | Paladin audit | [Paladin](https://paladinsec.co/projects/supernova/) | **MEDIUM** |
| 11 | Circulating supply metric can be gamed via 1-second stake (Paladin finding) | Audit report | Paladin | **MEDIUM** |
| 12 | TVL $4.8M on Ethereum mainnet — 99x below closest ve(3,3) competitor | DeFiLlama | [DeFiLlama](https://defillama.com/protocol/supernova) | **MEDIUM** |
| 13 | Only 1,551 NOVA holders — near-zero organic user base | Etherscan | Etherscan | **MEDIUM** |
| 14 | Zero independent media coverage (The Defiant, DL News, Rekt) | Search research | Multiple searches | **MEDIUM** |
| 15 | Zero grassroots Reddit/community discussion found | Search research | Reddit searches | **MEDIUM** |
| 16 | No institutional VC backing for Supernova specifically | Search research | Multiple searches | **MEDIUM** |
| 17 | Single auditor (Paladin only) — no multi-firm review | Security docs | [Docs](https://docs.supernova.xyz/security) | **MEDIUM** |
| 18 | Audit completed 4 days before mainnet launch — compressed timeline | Audit date vs. launch date | Paladin + Paragraph | **MEDIUM** |
| 19 | Third-generation fork (Solidly → Thena → Blackhole → Supernova) | Protocol docs | Self-reported | **LOW-MEDIUM** |
| 20 | SuperVerse ($SUPER) -98% decline — EllioTrades' prior flagship token | CoinMarketCap data | CMC | **MEDIUM** (context) |

---

## 6. Unresolved Questions

The following could NOT be determined and represent material gaps in this investigation:

1. **Team/founder wallet addresses on Ethereum.** Were NOVA tokens accumulated before launch via airdrop or private means, and were they sold during the ATH? This is the single most important unanswered question. Requires independent on-chain forensics.

2. **Identity and configuration of NOVA minter role.** Who holds mint authority? Is it an EOA, multisig, or timelock-protected? Requires Etherscan contract read.

3. **MinterUpgradeable admin key structure.** Who can upgrade the minter? Single key, multisig? What timelock, if any?

4. **GaugeManager admin configuration.** Address `0x19a410046afc4203aece5fbfc7a6ac1a4f517ae2` — admin key holder(s) not publicly disclosed.

5. **Verification of 450M+ token burns.** Are these documented on-chain against a verifiable dead address? Requires direct Etherscan block explorer check.

6. **Specific content of the 3 Governance audit findings.** These were acknowledged without resolution. Their severity and nature could not be extracted from the binary-encoded PDF.

7. **What caused the NOVA ATH collapse.** No post-mortem or public explanation from the team has been found. Was it organic sell pressure, coordinated exit, MEV, or something else?

8. **Blackhole $BLACK current TVL.** The predecessor peaked at $255M; current TVL is unknown. This context matters for evaluating whether Supernova is a genuine second act or a repeat pattern.

9. **Engineering team identity.** Who actually built the smart contracts? The two named founders are primarily known as influencer-marketers. The actual developers are unnamed in all documentation reviewed.

10. **Whether veBLACK/veNOVA holders from the Avalanche airdrop sold their NOVA.** 104M NOVA was airdropped to veBLACK holders. Their on-chain behavior around the ATH is untracked in this investigation.

---

## 7. Comparative Analysis

**Patterns Shared With Known Failed Projects:**

| Pattern | Wonderland | Terra/Luna | Supernova |
|---|---|---|---|
| Influencer-driven hype | Partial | No | **Yes** |
| Token peaks within 24h then collapses | No | No | **Yes** |
| Team anonymity | Daniele was known | Do Kwon known | Team known |
| Multiple consecutive collapses | No (1 project) | No | **Yes (BLACK then NOVA)** |
| Audited but centralized admin | Yes | N/A | **Yes** |
| Low holder count relative to hype | Partial | No | **Yes (1,551)** |

**ve(3,3) Fork Graveyard Context:**
The Solidly architecture has a well-documented collapse pattern on every chain where it launched (Fantom, Optimism, various EVM chains). Velodrome (Optimism) and Aerodrome (Base) are the exceptions that sustained TVL through institutional backing and chain-level integration. Supernova's $4.8M TVL against Aerodrome's $476M TVL illustrates that the Supernova team has not replicated the success formula — only the launch playbook.

---

## 8. Sources Index

| Source | URL | Trust Level |
|---|---|---|
| Supernova Docs | https://docs.supernova.xyz/ | Low (marketing) |
| Supernova Security Docs | https://docs.supernova.xyz/security | Low (marketing) |
| Supernova Tokenomics | https://docs.supernova.xyz/tokenomics | Low (marketing) |
| Paladin Audit Report | https://resources.supernova.xyz/Paladin_Supernova_Final_Report.pdf | High (independent auditor) |
| Paladin Project Page | https://paladinsec.co/projects/supernova/ | High |
| DeFiLlama — Supernova | https://defillama.com/protocol/supernova | High (on-chain aggregated) |
| DeFiLlama — Blackhole | https://defillama.com/protocol/blackhole | High |
| CoinGecko — BLACK | https://www.coingecko.com/en/coins/blackhole | Medium-High |
| CryptoRank — NOVA | https://cryptorank.io/price/supernova-dex | Medium-High |
| DEX Screener — NOVA | https://dexscreener.com/ethereum/supernova | Medium-High (on-chain) |
| Etherscan — NOVA Contract | https://etherscan.io/token/0x00Da8466B296E382E5Da2Bf20962D0cB87200c78 | High (on-chain) |
| Code4rena — Blackhole Audit | https://github.com/code-423n4/2025-05-blackhole | High |
| LSR Finance — Scam NOVA Alert | https://desk.lsr.finance/asset/nova-supernova/ | Medium-High |
| Announcing Supernova Mainnet | https://paragraph.com/@supernovadex/announcing-supernova-mainnet | Low (official) |
| Cookout Club — Supernova Analysis | https://cookoutclub.substack.com/p/supernova-blackholes-ethereum-expansion | Medium |
| BlockNews — Blackhole by Becker/EllioTrades | https://blocknews.com/blackhole-dex-by-alex-becker-and-elliotrades-the-future-liquidity-hub-for-defi-gamefi-and-ai-explained/ | Medium |
| FinanceScam — Becker Dossier | https://www.financescam.com/dossier/alex-becker/ | Medium (consumer watchdog) |
| Benzinga — MrBeast/SUPER Investigation | https://www.benzinga.com/content/41638540/investigation-connects-mrbeast-with-50-crypto-wallets-tied-to-insider-trading-allegations | Medium |
| Blocmates — Influencer Promotion Leak | https://www.blocmates.com/news-posts/200-influencers-named-in-paid-crypto-promotion-leak-few-disclosed-ads | Medium |
| IQ.wiki — EllioTrades Profile | https://iq.wiki/wiki/elliotrades | Medium |
| NFTgators — Blackhole $250M TVL | https://nftgators.com/blackhole-hits-250m-tvl-to-become-largest-dex-on-avalanche/ | Medium |
| The Defiant — Aero Merger | https://thedefiant.io/news/defi/dromos-labs-merges-aerodrome-and-velodrome-into-new-dex-aero | High |
| ZssBecker Tweet (PvP worldview) | https://x.com/ZssBecker/status/1759688968621211833 | High (primary source) |
| RootData — Blackhole Team | https://www.rootdata.com/Projects/detail/%20Blackhole?k=MTc3NjY%3D | Medium |

---

*Report generated: April 11, 2026. All price data as of approximately April 10–11, 2026. On-chain verification of burn addresses, multisig configurations, and team wallet behavior remains outstanding.*
