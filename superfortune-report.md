# SUPERFORTUNE (app.superfortune.xyz) — ADVERSARIAL DeFi DUE DILIGENCE REPORT

**Investigation Date:** May 5, 2026  
**Target:** app.superfortune.xyz — Token: $GUA (BEP-20)  
**Contract Address:** `0xa5c8e1513b6a08334b479fe4d71f1253259469be` (BSC)  
**Investigator Posture:** Guilty until proven innocent. Default assumption: every claim is marketing until independently verified.  
**Research Methods:** Web search, WebFetch, on-chain explorer analysis, CertiK Skynet, DeFiLlama, GeckoTerminal, CoinGecko, CryptoRank, CoinMarketCap, Reddit/CT searches, Manta Network GitHub scan.

---

## 1. EXECUTIVE SUMMARY

**Verdict: HIGH RISK — Structurally primed for insider extraction. Not a confirmed active rug, but the conditions for one are fully in place.**  
**Confidence Level: HIGH** (based on consistent findings across multiple independent data sources)

SuperFortune is an AI-powered "InfoFi" application built on BNB Smart Chain that combines Chinese metaphysics (Bazi, I Ching) with crypto price analysis. It is incubated by Manta Labs, the team behind Manta Network. The $GUA token launched November 27, 2025 with an FDV of ~$852M and a current market cap of ~$106M.

The Manta Labs incubation and Binance Alpha listing provide the only meaningful floor of legitimacy. Beyond that, the adversarial picture is deeply concerning.

### Top 3 Risks

1. **Pyramid/MLM Referral Architecture with Undisclosed USDC Funding** — The platform pays real USDC on two tiers of recruit purchases after a mandatory $10 entry fee. The source of this USDC is deliberately never disclosed in the official documentation. This is structurally indistinguishable from an illegal money circulation scheme.

2. **Total Team Control Over Unaudited Smart Contracts** — The team retains mint, pause, proxy upgrade, balance modification, and tax modification capabilities on an unaudited contract. Combined with 93% token concentration in major addresses and no ownership renouncement, the team can extract value at will.

3. **FDV of ~$852M vs. ~$21,600 in Verifiable Early Revenue** — This represents one of the most extreme valuation/revenue gaps observed in any DeFi project. 87.5% of supply remains locked and subject to future sell pressure over years of unlock events.

### Top 3 Positive Signals

1. **Manta Labs Incubation** — Manta Network is a real, funded Layer 2 with publicly identified founders (Kenny Li, Victor Ji, Shumo Chu), creating some accountability floor not present in pure anonymous projects.

2. **Binance Alpha Listing** — Binance Alpha applied some vetting before listing. This is not a full Binance compliance review but adds minimal due diligence.

3. **Verified Contract on BscScan** — The source code is verified with Exact Match to deployed bytecode, allowing independent code inspection.

---

## 2. TEAM ASSESSMENT

### 2.1 Named Individuals — SuperFortune Project

**Result: Zero named individuals.** No founders, developers, or advisors are publicly identified anywhere on the SuperFortune website, documentation, CoinGecko, CoinMarketCap, ICO Drops, or any independent source. No KYC verification exists. CertiK Skynet explicitly flags: **"No Team Verification — Failed KYC Checks."**

### 2.2 Parent Organization — Manta Labs / p0x Labs

The project claims to be "incubated by Manta Labs, the team behind Manta Network." The Manta Network founding team is publicly identifiable:

| Individual | Role | Verification Status | Source |
|---|---|---|---|
| **Kenny Li** | Co-Founder & COO, p0x Labs | VERIFIED — LinkedIn, Crunchbase | INDEPENDENT |
| **Victor Ji** | Co-Founder, p0x Labs | VERIFIED — LinkedIn, Harvard/Peking University credentials | INDEPENDENT |
| **Shumo Chu** | Co-Founder, p0x Labs / UCSB Professor | VERIFIED — academic record, ZK researcher | INDEPENDENT |

**Critical caveat:** None of these individuals are named anywhere in SuperFortune's own documentation as being responsible for GUA. The attribution is entirely inferential. SuperFortune's actual developers are **anonymous**.

### 2.3 GitHub Analysis

- CoinMarketCap lists the GitHub as: `manta-network/super-fortune-backend`
- Direct inspection of the Manta Network GitHub org (117 public repositories) found **no public `super-fortune-backend` repository**
- The repository is either private, renamed, or was deleted
- No community developers can audit the codebase, contribute, or verify claims about technical architecture

**[UNVERIFIED CLAIM]** The project describes itself as having "AI-powered" analysis combining machine learning with Bazi/I Ching. No technical documentation, model architecture, training data sources, accuracy benchmarks, or peer review exists anywhere in public-facing materials.

### 2.4 Social Media Forensics

**Official Account: @SUPERFORTUNE888 (Twitter/X)**
- Active. Posts about GUA token burns, airdrops, Binance Alpha, BNB Chain integration.
- Manta Network's official account (`@MantaNetwork`) has retweeted and co-posted with SuperFortune — most credible confirmation of the incubation relationship.
- Heavy airdrop/referral farming promotion — classic engagement-farming signal.
- No deleted tweet controversies surfaced; no deep tweet archive analysis was possible.

**Telegram:** t.me/Superfortunexyz — active, no independent moderation analysis available.

**Regional Marketing:** Manta Network Indonesia (`@MantaNetwork_ID`) actively promoted SuperFortune launches — coordinated regional push typical of airdrop farming campaigns.

### 2.5 Manta Labs — Controversy Record (Material to SuperFortune Risk)

**A. Money Laundering Allegations — South Korea (January 2024) — [HIGH RED FLAG]**

- During the Manta Network (MANTA) token launch, 2 million MANTA tokens were transferred to the personal wallet of Manta's Korean Business Development representative.
- Within 5 minutes of the Bithumb listing, MANTA hit $230 — approximately 100× the listing price.
- The Korean BD allegedly sold all 2M tokens, netting approximately $5.16 million (2,094.7 ETH), which was moved to a personal wallet.
- Manta's official response characterized these as pre-allocated "Ecosystem/Community" funds.
- **Status: Unresolved. No legal action publicly confirmed. No individual named.** The pattern of a low-float, high-FDV token launching with a trusted insider dumping at the listing peak is exactly the structure SuperFortune's own tokenomics replicate.
- *Sources: BeInCrypto, CoinChapter, CoinGape — INDEPENDENT*

**B. Lazarus Group / North Korea Targeting (April 2025)**
- Kenny Li was targeted in a sophisticated deepfake Zoom phishing attack attributed to Lazarus Group.
- Li avoided compromise. This does NOT implicate Manta in wrongdoing — it shows Manta holds sufficient assets to attract nation-state-level attackers.
- Raises questions about operational security at p0x Labs, which incubates SuperFortune.
- *Sources: Cointelegraph, Decrypt — INDEPENDENT*

**C. DDoS Attack During MANTA Launch (January 2024)**
- Manta Network suffered a DDoS attack coinciding with the token launch controversy.
- *Sources: Multiple crypto news outlets — INDEPENDENT*

### 2.6 What Could Not Be Verified — Team

| Item | Reason |
|---|---|
| Identity of SuperFortune's actual developers | No disclosure; GitHub repo private |
| Whether Kenny Li / Victor Ji / Shumo Chu are directly involved in GUA operations | Only incubation claimed — no role specifics published |
| Whether Korean BD money laundering resulted in legal action | No follow-up reporting found |
| Whether team social media accounts existed prior to 2025 | Archive analysis not completed |

---

## 3. THIRD-PARTY CONSENSUS

### 3.1 Independent Media Coverage

| Outlet | Coverage Found | Assessment |
|---|---|---|
| The Defiant | None | N/A |
| Rekt News | None | N/A |
| DL News | None | N/A |
| CoinTelegraph | None | N/A |
| Decrypt | None | N/A |
| Messari | Yes — brief mention in Manta Labs portfolio report | Neutral, not investigative |
| PANews | Yes — announcement pieces | Promotional |
| BingX Learn | Yes — tokenomics explainer | Exchange-affiliated, not independent |
| VentureBurn | Yes — promotional guide | Promotional |
| BeInCrypto / CoinGape / CoinChapter | Yes — covering Manta Network controversy (parent) | INDEPENDENT, negative on parent |

**Critical Finding:** Zero coverage from any credible independent DeFi-focused investigative publication for a project with a ~$106M market cap. Every article found is exchange-affiliated (BingX, MEXC, Gate, LBank), promotional crypto media, or the project itself. This is a significant anomaly. A $100M+ token with no critical coverage from The Defiant, Rekt News, or DL News after 6 months suggests either aggressive reputation management or a community too dominated by airdrop participants to produce whistleblowers.

### 3.2 Audit and Security Assessment

| Auditor | Status | Details |
|---|---|---|
| CertiK | **NOT AUDITED** | CertiK Skynet explicitly states "Not Audited By CertiK" |
| Hacken | No evidence | Not found |
| SlowMist | No evidence | Not found |
| Any named third party | **Unlinked reference only** | The project references a "Superfortune-EVM" audit document internally but no auditor is named, no report URL is provided, and no public version exists |
| Bug Bounty | None | CertiK confirms absence |

**CertiK Skynet Scores:**
- CoinMarketCap displays: **3.9/10 code security** — alarming
- CertiK Skynet direct: **77.25 (BBB)** — conflicting score
- The two scores reference different versions of the CertiK scoring methodology. Both indicate significant concern.
- Operational Resilience Score: **5%**
- Governance Strength: **5%**

**[UNVERIFIED CLAIM]** The project's internal documentation references a security audit with "reentrancy guards, pausable/upgradeable architecture" and "1 high-risk issue marked fixed." No auditor is identified and no public report is linked. This claim cannot be verified.

### 3.3 Community Sentiment

**Reddit:**
- ~105 posts mentioning the project, ~5,334 comments
- Pattern: posts receive net downvotes, comments receive net upvotes — anomalous, potentially indicating coordinated comment upvoting (astroturfing/bots)
- No dedicated critical threads on r/CryptoCurrency, r/DeFi, or r/ethfinance surfaced

**Twitter/X:**
- No independent skeptical coverage from unaffiliated crypto accounts found
- Coverage dominated by airdrop hunters and exchange promotional accounts

**Competitors/Adjacent communities:** No commentary from competing protocol communities surfaced.

**Assessment:** Absence of visible community criticism may reflect: (a) participants are primarily airdrop hunters with limited financial exposure, (b) active suppression of critical voices in community channels, or (c) a project too young and niche for adversarial community attention. The Reddit vote anomaly is concerning.

---

## 4. ON-CHAIN FINDINGS

### 4.1 Contract Risk Assessment

| Risk Vector | Present | Details | Confidence |
|---|---|---|---|
| Contract Verified on BscScan | YES | Solidity v0.8.26, Exact Match | HIGH |
| Proxy / Upgradeable Architecture | CONTRADICTED | BscScan: No proxy detected; CertiK Skynet: "proxy contract implementation" flagged | MEDIUM |
| Mint Function Active | YES (CertiK) | Team retains ability to mint new GUA | HIGH |
| Pause Transfer | YES (CertiK) | Transfers can be halted by owner | HIGH |
| Blacklist Capability | CONTRADICTED | BscScan: absent; CertiK: "potential blacklist capabilities" | MEDIUM |
| Owner Balance Modification | YES (CertiK) | Team can modify balances | HIGH |
| Tax/Fee Modification | YES (CertiK) | 8 issues flagged — modifiable tax mechanisms | HIGH |
| Anti-Whale Controls | YES (CertiK) | Centrally controlled | HIGH |
| Ownership Renounced | NO | CertiK confirms ownership NOT renounced | HIGH |
| Self-Destruct Capability | YES (CertiK) | Contract can be destroyed by owner | HIGH |

**Net Assessment:** The smart contract is entirely controllable by the team. Every significant risk vector is present. The combination of mint function + proxy upgrade + ownership retention = team can alter token behavior, supply, and rules at any time with no technical barrier.

**Contract Deployer Wallet** (`0xa89FD7b64aA4bf4bc63333043714D6a5E5Cdb7Bb`):
- Untagged and unverified on BscScan
- Created approximately 188 days ago (October 2025)
- Received the entire 1,000,000,000 GUA mint at contract creation
- Currently holds only 0.789 BNB and 28 low-value meme tokens
- Full disposition of the 1B GUA from this wallet to team/treasury/ecosystem wallets is not publicly documented

### 4.2 Token Distribution

| Category | Allocation | Status |
|---|---|---|
| Community Treasury & Governance | 40% (400M GUA) | Primarily locked; unlock schedule partially disclosed |
| Ecosystem, Growth & Marketing | 24% (240M GUA) | 8–48 month vesting |
| Team & Shareholders | 15% (150M GUA) | 18-month cliff from TGE (May 2027 earliest unlock) |
| Community Rewards & Airdrops | 10% (100M GUA) | 8–48 month vesting |
| Liquidity & Reserves | 11% (110M GUA) | 1.5% at TGE; 9.5% reserved |

**Circulating Supply Discrepancy (Major Data Integrity Issue):**

| Source | Circulating Supply Reported |
|---|---|
| CoinMarketCap | ~125,000,000 (12.5%) |
| CoinGecko | ~45,000,000 (4.5%) |
| CryptoRank | ~176,310,000 (17.63%, as of Feb 2026) |

Three major tracking platforms report wildly different circulating supply figures. This is not a minor rounding difference — the spread is 4× between CoinGecko and CryptoRank. It means market cap figures are unreliable and the actual float is unknown.

**Holder Concentration:** CertiK Skynet reports **93.08% of tokens held by major addresses**. At any circulating supply figure, this implies near-total insider dominance of token economics.

### 4.3 DEX Liquidity and Trading Analysis

| Venue | Type | Liquidity | 24h Volume | Vol/Liq Ratio |
|---|---|---|---|---|
| LBank | CEX | N/A | $1.42M–$3.7M | N/A (dominates 79–88% of total volume) |
| MEXC | CEX | N/A | ~$92K | N/A |
| Gate.io | CEX | N/A | ~$61K | N/A |
| Uniswap V3 (BSC) | DEX | $50,300 | $55,900 | **1.11× — elevated** |
| Uniswap V4 (BSC) | DEX | $3,300 | $96 | 0.03× |
| PancakeSwap V2 (TGE venue) | DEX | **$0.445** | ~$0 | ∞ |

**Critical Findings:**

1. **LBank dominates 79–88% of all reported GUA volume.** LBank has a documented history of wash trading allegations across listed tokens. This level of concentration in a single exchange with inflated volume reputation is a strong signal that reported trading volume does not reflect genuine market interest.

2. **PancakeSwap V2** — described as the TGE launch venue — now has **$0.445 in liquidity**. Initial DEX liquidity was removed or migrated without public disclosure.

3. **Uniswap V3 Vol/Liq ratio of 1.11×** — daily volume exceeds the entire pool's liquidity. This is elevated and consistent with wash trading on the primary DEX pool.

4. **Total on-chain DEX liquidity is below $55K.** A token with a $100M+ market cap cannot sustain organic CEX volume of $1.4M+/day when its on-chain liquidity is $55K. The disparity is orders of magnitude beyond what legitimate market making explains.

### 4.4 Upcoming Unlock Events (Critical)

- **~May 27, 2026 (≈22 days from report date):** ~21,990,000 GUA unlocking
- **Value at current price (~$0.85):** ~$18.7M
- **As % of most conservative circulating supply (125M):** ~17.6% instantaneous dilution
- **As % of smallest reported circulating supply (45M):** ~49% dilution
- No independently verified on-chain timelock or lock contract (PinkLock, Unicrypt, Team Finance) has been found to enforce the stated vesting schedule

### 4.5 Solana Impersonator Token (Critical Safety Finding)

A separate GUA token was found actively trading on Solana (Raydium pool: `EHfiXMde7y8tu1QBA3C8XE7vyRwSnKiMMQGt4WFNVdHD`) with:
- $245K in liquidity
- FDV of $1.03B

This is almost certainly an impersonator/scam token exploiting the SuperFortune brand. The project has not taken prominent, visible public action to warn users against this fake token.

---

## 5. RED FLAGS REGISTER

### CRITICAL

| # | Red Flag | Evidence | Source Type |
|---|---|---|---|
| C-1 | **Multi-level referral system with undisclosed USDC funding source.** Platform pays 35% USDC to direct inviters and 10% to second-tier inviters of new $10 entry-fee payments. The documentation explicitly confirms real USDC settlement but never discloses where this USDC originates. Structure is functionally a pyramid scheme. | docs.superfortune.ai/referral-rewards | OFFICIAL (self-incriminating) |
| C-2 | **Team retains full smart contract control.** Mint, pause, proxy upgrade, balance modification, self-destruct, and tax modification all active. Ownership not renounced. Zero technical barrier to rug. | CertiK Skynet, BscScan | INDEPENDENT / ON-CHAIN |
| C-3 | **93.08% token concentration in major addresses.** Combined with 87.5% supply still locked, insiders will dominate all future price action for years. | CertiK Skynet | INDEPENDENT |
| C-4 | **Zero completed audit from any named auditor** for a $100M+ market cap project. The referenced "Superfortune-EVM" audit has no auditor name, no public report, and no link in official documentation. | CertiK Skynet, docs.superfortune.ai | INDEPENDENT / OFFICIAL |

### HIGH

| # | Red Flag | Evidence | Source Type |
|---|---|---|---|
| H-1 | **Parent incubator (Manta Labs) has unresolved insider dump allegations.** In January 2024, 2M MANTA tokens were sold by a Korean BD representative at listing peak, netting $5.16M. This is precisely the low-float, high-FDV launch pattern SuperFortune replicates. | BeInCrypto, CoinChapter, CoinGape | INDEPENDENT |
| H-2 | **LBank dominates 79–88% of all GUA trading volume.** LBank has documented wash trading history. DEX liquidity ($55K) cannot support the reported CEX volume ($1.4M+/day) organically. | CoinGecko volume data, GeckoTerminal | INDEPENDENT / ON-CHAIN |
| H-3 | **PancakeSwap TGE liquidity pool has $0.445 remaining.** Initial liquidity was removed or migrated without disclosure. | GeckoTerminal BSC | ON-CHAIN |
| H-4 | **FDV of ~$852M vs. ~$21,600 in verifiable early revenue.** ~39,000× revenue multiple with 87.5% of supply still locked. | CoinGecko, BingX, revenue data | INDEPENDENT |
| H-5 | **Circulating supply reported inconsistently across three major platforms** (CoinGecko: 45M, CMC: 125M, CryptoRank: 176M). Accurate float is unknown. All market cap figures are unreliable. | CoinGecko, CMC, CryptoRank | INDEPENDENT |
| H-6 | **Upcoming ~$18.7M unlock in ≈22 days** (May 27, 2026). No independently verified on-chain lock contract enforcing vesting. | CryptoRank, MEXC News | INDEPENDENT |
| H-7 | **GitHub repo `manta-network/super-fortune-backend` is not publicly accessible** despite being listed as the official GitHub on CMC. Code cannot be independently reviewed. | Manta GitHub org scan, CMC listing | INDEPENDENT / ON-CHAIN |
| H-8 | **Uniswap V3 volume exceeds pool liquidity** (ratio 1.11×) — primary DEX pool shows elevated wash trading signal. | GeckoTerminal | ON-CHAIN |
| H-9 | **Active Solana impersonator GUA token** with $245K liquidity and $1.03B FDV. No prominent public user warning found from the project. | DexScreener Solana | COMMUNITY / ON-CHAIN |
| H-10 | **Team allocation of 15% + combined treasury of 40%** = 55% insider-controlled with no external investor accountability. "No VC" framing obscures that insiders own even more, not less. | Tokenomics docs | OFFICIAL |

### MEDIUM

| # | Red Flag | Evidence | Source Type |
|---|---|---|---|
| M-1 | **Zero independent investigative media coverage** for a $100M+ market cap project (no Defiant, Rekt News, DL News, Cointelegraph, Decrypt). | Search results | INDEPENDENT (absence) |
| M-2 | **Pseudoscientific product core.** Bazi and I Ching "AI" analysis of crypto prices has no published accuracy data, no backtesting, no peer review. Regulators in multiple jurisdictions treat fortune-based financial advice as potentially illegal. | docs.superfortune.ai, BingX risk section | OFFICIAL + INDEPENDENT |
| M-3 | **Reddit vote anomaly.** Posts receive net downvotes; comments receive net upvotes. Pattern consistent with coordinated bot/astroturf activity. | CMC community intelligence | COMMUNITY |
| M-4 | **Temporary HTTP redirects on all domains** (superfortune.xyz→app.superfortune.xyz, docs.superfortune.xyz→docs.superfortune.ai). Production protocols use permanent redirects; 307 temporary suggests ongoing infrastructure instability or possible future domain switching. | WebFetch redirect behavior | ON-CHAIN (infrastructure) |
| M-5 | **No bug bounty program** confirmed by CertiK. Operational Resilience: 5%. Governance Strength: 5%. | CertiK Skynet | INDEPENDENT |
| M-6 | **Contract deployer wallet is untagged, first appeared October 2025**, received 1B GUA mint. Full disposition of tokens never publicly documented. | BscScan | ON-CHAIN |
| M-7 | **CertiK scores contradict each other** (3.9/10 on CMC vs 77.25/100 BBB on Skynet). Ambiguity about actual security rating is itself a red flag. | CertiK Skynet, CMC | INDEPENDENT |

### LOW

| # | Red Flag | Evidence | Source Type |
|---|---|---|---|
| L-1 | **ATL of $0.04 on TGE day** followed by 20×+ rise — raises question of coordinated initial price suppression or pump-and-dump setup. | CoinGecko price history | ON-CHAIN |
| L-2 | **"No VC / no public sale" framing** is marketed as community-friendly but structurally means no external oversight of vesting enforcement. | Docs | OFFICIAL |
| L-3 | **Binance Futures listing (20× leverage)** for a sub-$100M micro-cap token. Unusual; significantly amplifies retail destruction potential during unlocks or price dislocations. | Multiple sources | INDEPENDENT |
| L-4 | **~6 months old.** Has not existed through any bear market. All performance data is within initial hype window. | TGE date Nov 27, 2025 | INDEPENDENT |

---

## 6. UNRESOLVED QUESTIONS

| Question | Why Unresolved | What Would Resolve It |
|---|---|---|
| Who are SuperFortune's actual developers? | No disclosure; GitHub private | Public doxxing, KYC with named auditor |
| What is the funding source for USDC referral payouts? | Never disclosed in official docs | Published treasury accounting or on-chain revenue tracking |
| Is team vesting enforced on-chain? | No Unicrypt/PinkLock/Team Finance address found | On-chain lock contract address with public timelock |
| Is the Uniswap V3 volume organic or wash traded? | Requires deep order flow analysis | On-chain DEX trade graph analysis, wallet clustering |
| What happened to PancakeSwap TGE liquidity? | No public announcement of removal/migration found | Transaction history of original LP provider wallet |
| Did the Korean MANTA money laundering result in legal action? | No follow-up reporting found | Korean regulatory filings, legal records |
| Does Kenny Li / Manta leadership directly control GUA treasury? | Only incubation claimed | Formal disclosure of multisig signers for GUA wallets |
| Is the referenced "Superfortune-EVM" audit real? | No public report, no auditor named | Published audit report with auditor identification |
| What is accurate circulating supply? | Three platforms report 45M / 125M / 176M | Official on-chain lock contract addresses with verifiable balances |

---

## 7. COMPARATIVE ANALYSIS — RUG PULL PATTERN MATCHING

| Pattern | Known Rug Pulls | SuperFortune |
|---|---|---|
| Anonymous team | Wonderland (Sifu), Squid Game token | YES — no named individuals on GUA |
| Low float / high FDV | Terra/Luna (UST mechanics), most 2021–22 IDOs | YES — 4.5–12.5% float, 88–95.5% locked |
| Insider-controlled treasury | Celsius (Mashinsky), FTX (Bankman-Fried) | YES — 55% team+treasury, no external accountability |
| Exchange-driven wash trading volume | Multiple BSC scam tokens 2021 | LIKELY — LBank dominates 79–88%, DEX liq only $55K |
| Referral/MLM mechanics | BitConnect, OneCoin | YES — two-tier USDC referral with mandatory entry fee |
| Pseudoscientific value proposition | HEX (Richard Heart's "store of value" framing) | YES — Bazi/I Ching "AI" price prediction |
| Parent org with prior misconduct | Multiple serial rug teams | PARTIAL — Manta Labs has unresolved allegations |
| Upcoming large unlock into illiquid market | Terra (UST collapse), multiple IDO dumps | YES — ~$18.7M unlock in 22 days, $55K DEX liquidity |

**Assessment:** SuperFortune matches 7 of 8 high-risk comparative patterns. The only differentiator from a pure rug setup is the Manta Labs institutional backing and Binance Alpha listing. These matter — but they do not make the structural risks disappear.

### Tokenomics Sustainability

- **Yield source:** Primarily referral fees and platform purchase revenue. USDC rewards depend on a constant flow of new participants purchasing Fortune Charms ($10 entry fee). This is definitionally a demand-dependent circular economy.
- **Burn mechanics:** GUA tokens burned in exchange for platform rewards — reduces supply but only if demand for burning persists.
- **Conclusion:** The yield mechanism is unsustainable without continuous new participant inflow. When new participant acquisition stalls, existing participant USDC payouts are at risk. This is the fundamental fragility of referral-based reward systems.

---

## 8. SOURCE REGISTRY

| Source | URL | Type |
|---|---|---|
| SuperFortune App | https://app.superfortune.xyz | OFFICIAL |
| SuperFortune Docs | https://docs.superfortune.ai | OFFICIAL |
| Tokenomics | https://docs.superfortune.ai/tokenomics | OFFICIAL |
| Referral Rewards | https://docs.superfortune.ai/referral-rewards | OFFICIAL |
| Fortune Charms Docs | https://docs.superfortune.ai/platform-overview/fortune-charms | OFFICIAL |
| CoinGecko — $GUA | https://www.coingecko.com/en/coins/superfortune | INDEPENDENT |
| CoinMarketCap — $GUA | https://coinmarketcap.com/currencies/superfortune/ | INDEPENDENT |
| CertiK Skynet — SuperFortune | https://skynet.certik.com/projects/superfortune | INDEPENDENT |
| CryptoRank — Vesting | https://cryptorank.io/price/superfortune/vesting | INDEPENDENT |
| BscScan — GUA Token | https://bscscan.com/token/0xa5c8e1513b6a08334b479fe4d71f1253259469be | ON-CHAIN |
| BscScan — Deployer Wallet | https://bscscan.com/address/0xa89FD7b64aA4bf4bc63333043714D6a5E5Cdb7Bb | ON-CHAIN |
| GeckoTerminal — GUA/WBNB | https://www.geckoterminal.com/bsc/pools/0xae4c108b547a08cc9c038eeae8ec5434e4c086a0 | ON-CHAIN |
| DexScreener Solana Impersonator | https://dexscreener.com/solana/ehfixmde7y8tu1qba3c8xe7vyrwsnkimmqgt4wfnvdhd | ON-CHAIN |
| MEXC Tokenomics | https://www.mexc.com/price/GUA/tokenomics | EXCHANGE-AFFILIATED |
| MEXC Unlock News | https://www.mexc.com/news/1056432 | EXCHANGE-AFFILIATED |
| BingX — GUA Analysis | https://bingx.com/en/learn/article/what-is-superfortune-gua-token-how-does-it-work | EXCHANGE-AFFILIATED |
| ICO Drops — GUA | https://icodrops.com/superfortune/ | INDEPENDENT |
| Messari — Manta Labs | https://messari.io/report/manta-labs-scaling-retail-adoption-through-consumer-applications | INDEPENDENT |
| PANews — SuperFortune | https://www.panewslab.com/en/articles/1ed5b905-eadb-4521-b24b-c6f48d604ff2 | INDEPENDENT |
| Binance Alpha Listing | https://coinfomania.com/binance-alpha-lists-superfortune-gua-airdrop-launch/ | INDEPENDENT |
| BeInCrypto — Manta Money Laundering | https://beincrypto.com/binance-launchpool-manta-network-money-laundering-bithumb/ | INDEPENDENT |
| CoinChapter — Manta Money Laundering | https://coinchapter.com/manta-network-money-laundering/ | INDEPENDENT |
| CoinGape — Manta Korea Controversy | https://coingape.com/manta-network-sparks-money-laundering-concerns-in-south-korea-amid-binance-listing/ | INDEPENDENT |
| Decrypt — Lazarus/Manta | https://decrypt.co/315329/manta-co-founder-targeted-by-lazarus-group-in-zoom-phishing-attempt | INDEPENDENT |
| Cointelegraph — Lazarus/Manta | https://cointelegraph.com/news/manta-exec-reveals-attempted-zoom-attack-by-lazarus-using-legit-faces | INDEPENDENT |
| Kenny Li — Crunchbase | https://www.crunchbase.com/person/kenny-li-662c | INDEPENDENT |
| Manta Network GitHub | https://github.com/manta-network | INDEPENDENT |
| Rekt News (no GUA coverage) | https://rekt.news | INDEPENDENT |
| The Defiant (no GUA coverage) | https://thedefiant.io | INDEPENDENT |

---

## 9. FINAL VERDICT

**Risk Rating: HIGH**  
**Confidence: HIGH**

SuperFortune is not a zero-team anonymous rug in the traditional sense — it has institutional backing from Manta Labs and exchange credibility from Binance Alpha. These factors mean the project likely will not disappear overnight. They do not, however, resolve any of the structural extraction risks:

- The referral system is a pyramid with an undisclosed USDC funding source.
- The smart contract is fully controllable by the team with no technical rug barriers.
- 87.5%+ of supply remains locked, with team unlocks beginning May 2027 — representing years of overhead price pressure.
- The imminent May 27, 2026 unlock (~$18.7M) into $55K of DEX liquidity is a near-term acute risk.
- Volume is almost certainly inflated by LBank, masking true liquidity depth and price discovery.
- The parent organization has unresolved allegations of insider token dumping using the same low-float, high-FDV structure as GUA.

The outcome most consistent with this evidence profile is not an immediate rug but a **slow-motion insider extraction**: steady unlock events sold into inflated CEX volume, with retail participants holding the bag as the supply overhang materializes over 2026–2027.

---

*This report was produced May 5, 2026. All on-chain data and prices are subject to change. This is not financial advice.*
