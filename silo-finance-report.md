# Silo Finance — Adversarial Due Diligence Report

**Report Date:** 2026-03-26
**Protocol:** Silo Finance (Isolated Lending Markets)
**Chains:** Ethereum, Arbitrum, Base, Optimism, Sonic
**Category:** Non-Custodial Lending / Permissionless Money Markets
**Token:** SILO (migrated V1 → V2)
**Researcher Stance:** Guilty until proven innocent

---

## ⚠️ LEAD WITH THE MOST ALARMING FINDING

**An unaudited "unreleased" smart contract was deployed to Ethereum mainnet with real DAO funds. It was subsequently exploited for $545,000 in June 2025.**

The co-founder's public statement frames this as "internal testing" — but testing contracts do not belong on mainnet with real ETH value. Hypernative Labs detected the attack 3 minutes and 20 seconds before execution. That window was not used to stop it. The attacker pre-funded from Tornado Cash, meaning this was a pre-planned, targeted exploit of a contract the protocol itself had labeled "unreleased."

This is a process and governance failure, not an abstract theoretical risk — it materialized.

---

## 1. EXECUTIVE SUMMARY

**Verdict:** MEDIUM RISK — Legitimate protocol with significant unresolved security process failures.

**Confidence Level:** High (named founder, substantial public record, multi-chain on-chain data accessible)

Silo Finance is a real, operational DeFi lending protocol with a legitimate founding story (ETHGlobal 2021 hackathon finalist), named and partially verifiable leadership, $33M in institutional funding, $277M TVL across four chains, and one of the most comprehensive audit programs in DeFi lending. Its core innovation — isolated lending silos per asset — is technically sound and independently validated as a meaningful advance over shared-pool lending.

However, the June 2025 exploit exposes a critical gap between the protocol's rigorous audit culture on core contracts and its lack of controls around experimental/peripheral contract deployment. The SILO token's governance history (uncapped V1 mint, now migrated) and the ~44.8% insider supply now fully liquid raise governance centralization concerns. A single unmitigated Code4rena finding and Certora's uncovering of critical vulnerabilities that two professional audit firms missed are additional signals that the security process, while extensive, is not infallible.

### Top 3 Risks
1. **Unaudited contract on mainnet exploited for $545K (June 2025)** — Process failure: a pre-release contract with DAO funds was deployed to live Ethereum mainnet with no audit, was targeted by a pre-planned attacker funded via Tornado Cash, and the 3m20s early warning from Hypernative was not actionable in time.
2. **~44.8% insider token supply fully vested and liquid** — Founding contributors, early contributors, advisors, and investors hold nearly as much SILO as the community treasury. veSILO governance model amplifies whale voting power. Governance capture is structurally possible.
3. **Certora Formal Verification found CRITICAL vulnerabilities that both Quantstamp AND ABDK professional audits missed** — This pattern means the set of "audited" contracts may still contain unknown vulnerabilities that manual audit processes are structurally unable to detect.

### Top 3 Positive Signals
1. **Named, non-anonymous founding team with verifiable track record** — Aiham Jaabari is publicly identified, interview-accessible, and his prior project (Coreum Inc.) is independently verifiable via Crunchbase and Tracxn.
2. **Most comprehensive audit program in DeFi lending** — 8+ audit engagements across Trail of Bits, Certora, Spearbit/Cantina, Sigma Prime, Code4rena, Enigma Dark, ABDK, and Quantstamp. This level of coverage is rare and suggests genuine security investment.
3. **Isolated market design delivers on its core promise** — LlamaRisk independently validated that Silo's architecture genuinely limits systemic contagion risk, addressing the real failure modes of Aave/Compound shared pools (Venus, CREAM precedents).

---

## 2. TEAM ASSESSMENT

### Primary Identified Individual: Aiham Jaabari

**Role:** Founding Contributor, Silo Finance

| Claim | Source | Verified? |
|---|---|---|
| Founding Contributor at Silo Finance | Crunchbase, CoinCodex interview, multiple media | ✅ VERIFIED |
| Co-founded Silo with others in September 2021 | Multiple sources | ✅ VERIFIED |
| ETHGlobal 2021 hackathon finalist | Multiple sources | ✅ VERIFIED — ETHGlobal maintains public records |
| Previously Co-Founder at Coreum Inc. | Crunchbase, Tracxn | ✅ VERIFIED — Coreum listed as deadpooled startup |
| In blockchain since 2018 — music copyright protocol | Multiple interview sources | ✅ PARTIALLY VERIFIED — Coreum's music copyright focus confirmed independently |
| Education: University of Wollongong | Multiple sources | UNVERIFIED — no independent confirmation found |
| Based in Austin, Texas | Multiple sources | UNVERIFIED — no independent confirmation found |

**Personal Website:** aiham.io — returns 404 as of research date. A functioning personal website was previously listed on GitHub and Crunchbase. Absence of a maintained personal site is a minor yellow flag.

**GitHub:** [github.com/aiham02](https://github.com/aiham02)
- GitHub handle "aiham02" confirmed affiliated with Silo Finance (links to silo.finance, Twitter: @aihamjaabari)
- Public repositories: fork of `trustwallet/assets` and fork of `flashbots/mev-job-board`
- **No original public code contributions found** — only forks of third-party repositories
- This is surprising for a protocol founder who was a hackathon finalist. The original Silo prototype code is not public under this handle.
- Possible explanations: contributions happen under org account (silo-finance), or under a different alias. Neither can be confirmed.

**Twitter:** @aihamjaabari — active, regularly posts about Silo developments. No deleted-tweet patterns found. No connections to known bad actors identified.

**Prior Project (Coreum Inc.) — Critical Assessment:**
- Coreum Inc. was a blockchain music royalty/rights management startup founded in 2018
- Co-founded with Tomasz Zacharczuk (CTO) and Piotr Byczuk
- Product: "Lumen" (songwriters protect songs) and "Radium" (smart contract music contracts)
- Status: **DEADPOOLED** (Tracxn classification)
- **Assessment:** A failed blockchain startup from 2018 is not a red flag — the vast majority of 2018 blockchain projects failed. What matters is how they failed. No evidence of exit scam, investor fraud, or misconduct was found in connection with Coreum. This appears to be a legitimate failed startup.

---

### Other Team Members

Silo Finance's GitHub organization (github.com/silo-finance) has **no publicly listed members**. Beyond Aiham Jaabari, no other core contributors are publicly identified by name on official channels.

**Identified Advisors/Investors (VERIFIED — these are real DeFi figures):**
| Person | Affiliation | Verifiability |
|---|---|---|
| Sam Kazemian | Frax Protocol co-founder | ✅ Highly public DeFi figure |
| Joey Santoro | Fei Protocol founder | ✅ Highly public DeFi figure |
| Tyler Ward | BarnBridge co-founder | ✅ Public DeFi figure |
| Santiago R Santos | Independent DeFi investor | ✅ Known in DeFi circles |
| Ameen Soleimani | Reflexer (RAI) | ✅ Known Ethereum developer |
| Regan Bozman | Lattice Capital | ✅ Verifiable |
| Electric Capital | Institutional VC | ✅ Major DeFi fund |

**Assessment:** The advisor/investor roster is unusually high-quality for a DeFi protocol. These are not random names. Sam Kazemian, Joey Santoro, and Ameen Soleimani are respected builders with independent reputations — their public association with Silo functions as a meaningful accountability anchor.

---

### GitHub Organization Analysis

**Organization:** [github.com/silo-finance](https://github.com/silo-finance)
- 22 public repositories
- **0 publicly listed organization members** — this is a recurring privacy pattern
- Key repos: `silo-contracts-v2`, `silo-foundry-utils`, `silo-v2-ponder`, `yield-server`
- Development activity confirmed: 39 weekly commits, 433 monthly commits (DeFiLlama data)
- 9 monthly developers — small but active team
- Repos show genuine development activity; not a fork-and-rebrand pattern

**Code quality signals:**
- The protocol originated from ETHGlobal 2021 hackathon — verifiable event with real code submission required
- V2 codebase underwent 8+ independent security reviews, including formal verification
- Code structure described as complex with novel architecture (ERC-4626 compatible, Hooks system)
- These are markers of genuine engineering depth

---

## 3. THIRD-PARTY CONSENSUS

### Independent Analyst Coverage

**LlamaRisk Asset Risk Assessment (VERIFIED — independent)**
Source: https://www.llamarisk.com/research/archive-llamarisk-asset-risk-assessment-silo-finance

This is the highest-quality independent analysis found. Key findings:

- *"Silo Finance has introduced some innovative new primitives that are mostly targeted toward the more risk-aware DeFi users."*
- *"In general, LlamaRisk gained the impression that Silo is very focused on reducing risks and increasing security where possible."*
- Certification audit findings noted: Certora FV found 2 HIGH and 3 MEDIUM issues missed by both ABDK and Quantstamp
- Recommendation: Better bad debt dashboard, careful collateral onboarding per silo, risk assessments per new collateral
- **Overall assessment: POSITIVE, with caveats on risk management tools**

**Note on timing:** LlamaRisk's assessment was written during V1 era. A current V2-era assessment was not found. Given the exploit in June 2025, an updated LlamaRisk assessment would be valuable.

**The Defiant:** Coverage was **SPONSORED by Silo Finance** — labeled as such. Not independent editorial. No analytical value from a risk perspective.

**IntoTheBlock DeFi Risk Radar (October 2024):** Added Silo Finance with 17 risk indicators. This is a tool integration, not an adversarial analysis.

**Nansen:** Published a factual explainer — not adversarial, but acknowledges isolation design rationale.

**Independent critical coverage:** LIMITED. No adversarial analysis from Rekt News, DL News, or independent researchers was found specifically targeting Silo Finance's risks. This cuts both ways — no exposed scandals, but also no external scrutiny of the June 2025 exploit's process failures.

---

### Audit Assessment

#### Complete Audit History

**Silo V1:**
| Firm | Focus | Key Findings | Status |
|---|---|---|---|
| Quantstamp | V1.1.1 core | 0 high, 5 medium, 3 low, 6 info (14 total) | All resolved |
| ABDK | V1.1.1 core | 6 major, 1 moderate, 65 minor | All resolved |
| ChainSecurity | Curve/Convex integration | Not publicly detailed | Resolved |
| Certora | Formal Verification | **2 HIGH + 3 MEDIUM missed by both Quantstamp and ABDK** | All resolved |

**CRITICAL FINDING:** Certora's formal verification discovered critical vulnerabilities that **two separate professional audit firms failed to find**. This is the most important signal in the audit history — not because the issues weren't fixed (they were), but because it demonstrates that manual audits can miss material security flaws in DeFi lending code. The same pattern could apply to V2 contracts that have not undergone FV for every component.

**Silo V2:**
| Firm | Date | Scope | Key Findings |
|---|---|---|---|
| Trail of Bits | 2024 | Core contracts + veSILO | Completed; specific findings not publicly indexed |
| Certora | Nov 2024 | Core V2 | Report available on docs.silo.finance |
| Spearbit/Cantina | Jan–Feb 2025 | Full contest | Report available |
| Sigma Prime | March 2025 | Security assessment | All issues resolved |
| Code4rena | Mar 24–31, 2025 | Core V2 | 6 medium findings |
| Code4rena Mitigation Review | May 2025 | M01–M06 from above | **M-06 not mitigated** (severity adjusted by judges) |
| Certora | May 2025 | Additional V2 | Further issues found and addressed |
| Enigma Dark | May 2025 | V2 Core | Report on GitHub |

**CODE4RENA M-06 — UNRESOLVED FINDING:**
One finding from the March 2025 Code4rena audit (M-06) was **not mitigated**. The Code4rena judging staff "adjusted the severity" after reviewing additional context from the sponsor. This is a potential red flag — when sponsors provide context that changes a finding's severity, it can represent a legitimate edge case or a rationalization. The specific nature of M-06 requires reading the full report to assess.
Source: https://code4rena.com/reports/2025-03-silo-finance

**Audit reports location:** All V2 reports are hosted on Google Drive links from docs.silo.finance — not in a dedicated public GitHub audits repository. This is functional but less durable than a versioned repository. Web content disappears.

**Trail of Bits report:** Completed per 2024 roadmap, but specific findings are not publicly indexed in Trail of Bits' own publications repository at github.com/trailofbits/publications. This is a minor concern (less critical than Enosys's invisible Coinspect audit, as ToB completion is confirmed by multiple sources including the Code4rena repo).

---

### Community Sentiment

**Reddit:** No indexable Reddit threads found for Silo Finance across r/DeFi, r/CryptoCurrency, or r/ethfinance. This is partially explained by the niche technical user base (institutional/advanced DeFi users, not retail Reddit demographics).

**Governance Forum (gov.silo.finance):** Active forum with genuine proposal discussions. No major governance controversies uncovered. The veSILO tokenomics and 30% incentive allocation for V2 markets generated community discussion but no significant opposition.

**Twitter/CT:** Protocol is followed and discussed by legitimate DeFi participants. No coordinated shilling or suspicious promotion patterns found.

**Arca (VC) disclosure:** Arca publicly disclosed being a top SILO token holder — this was noted in community searches as a whale concentration concern. However, Arca's public disclosure is transparent behavior, not deceptive.

---

## 4. ON-CHAIN FINDINGS

### Contract Architecture — V2

**Chains:** Ethereum, Arbitrum, Base, Optimism, Sonic
**TVL:** ~$277M (DeFiLlama, as of May 2025 snapshot)
**Annual Fees:** ~$1.2M | P/S Ratio: 9.3x
**Revenue (daily):** ~$330K annualized per separate protocol suite listing

**Design:** Permissionless, immutable two-asset lending markets per V2. ERC-4626 compatible. Modular Hooks system. Factory-deployed silos — each is independent.

**Critical note on "immutable":** Silo V2 is described as "permissionless, immutable" in official docs. However:
- The team multisig can **pause** individual Silos
- A team multisig controls emergency oracle-switching until DAO governance matures
- This is documented and represents a compromise between immutability and emergency response capacity

### The June 2025 Exploit — Detailed Analysis

**Exploited Contract:** `LeverageUsingSiloFlashloanWithGeneralSwap`
**Address:** `0xCbEe4617ABF667830fe3ee7DC8d6f46380829DF9`
**Network:** Ethereum Mainnet AND Sonic

**What happened:**
1. Contract described as "pre-release" and "unreleased" — officially for testing with DAO funds only
2. Contract contained NO input validation for `swapArgs` parameter in `openLeveragePosition`
3. Attacker set `receiver = attacker_address`, `borrower = victim_address`
4. Victim had granted maximum token allowance to the contract (this victim was likely DAO/internal)
5. 224 ETH (~$545K) drained from DAO treasury to attacker
6. Attacker was pre-funded via Tornado Cash — this was a **targeted, pre-planned attack**
7. Hypernative Labs detected the attack **3 minutes and 20 seconds** before execution
8. The 3m20s lead time was not used to prevent the exploit

**Why this matters — what it reveals:**
- An **unaudited contract** was deployed to **production mainnet** with **real ETH value**
- "Testing with DAO funds on mainnet" is not a testing methodology — it is mainnet deployment with disguised production risk
- The attacker specifically targeted this contract, implying knowledge of its existence and vulnerability — possibly through on-chain monitoring or insider information (unproven)
- **No public audit** of the leverage contract was found pre-exploit
- The official response correctly clarified no user funds were lost — but $545K of community-owned DAO funds is not a trivial sum to "test" on mainnet

**Process failure classification: CRITICAL** — Not a vulnerability in audited code. A failure to apply deployment controls (audit-before-mainnet) to a peripheral contract.

---

### SILO Token — On-Chain Analysis

**V1 Token (Legacy):** `0x6f80310ca7f2c654691d1383149fa1a57d8ab1f8`
- Contains `mint(address _to, uint256 _amount) public onlyOwner` function
- **The contract owner could mint arbitrary SILO tokens at any time**
- This is a CRITICAL centralization risk that existed for years until V2 migration
- No evidence this mint function was abused — but the capability existed

**V2 Token (Current):** `0xf0b2dd79324a66d2108c961d680f7616e1486bb0`
- Inherits: `ERC20`, `ERC20Burnable`, `ERC20Permit`, `ERC20Capped`, **`Pausable`**, **`Ownable2Step`**
- **`Pausable`**: Owner/designated account can freeze token transfers and migration
- **`Ownable2Step`**: Privileged owner key; two-step transfer reduces but does not eliminate risk
- Max supply capped — arbitrary minting not possible in V2
- V1→V2 migration: V1 tokens are burned, V2 minted — **owner can pause this migration**
- **No audit found for the SILO token contract itself** (separate from protocol contracts)

**Arbitrum SILO (for reference):** `0x0341c0c0ec423328621788d4854119b97f44e391` (Arbiscan)

### Governance Multisig

**Structure:** Team multisig of **5 core team members** — threshold not publicly stated, but 3/5 cited for vault-specific multisigs

**Capabilities:**
- Pause individual Silos
- Freeze Silos pending oracle replacement governance vote
- Switch price oracles (after governance vote)

**Assessment:**
- Multisig configuration provides meaningful safeguards against single-key compromise
- However, the team holds admin capability without full public accountability of signer identities
- "Will hand over to DAO" is a promise, not a current fact

### Token Distribution Analysis

| Allocation | % | Status |
|---|---|---|
| Community Treasury | 45% | Fully vested |
| Founding Contributors | 21.75% | Fully vested |
| Future Contributors & Advisors | 10% | Fully vested |
| Early Contributors | 6.75% | Fully vested |
| Early Investors & Advisors | 6.3% | Fully vested |
| Early Community Rewards | 0.2% | Airdropped |
| Genesis Protocol-Owned Liquidity | 10% | From public auction |

**Combined insider/VC supply: ~44.8%** — founders (21.75%) + early contributors (6.75%) + future contributors/advisors (10%) + investors/advisors (6.3%)

**All vesting periods now complete as of 2024.** This means all insider tokens are fully liquid and can be sold or used to vote in governance at any time. SILO's governance model (veSILO) further amplifies concentration since large holders can lock for 3 years to gain disproportionate voting weight, while retail holders cannot afford to lock meaningful amounts or pay Ethereum gas repeatedly.

**SILO holder count:** ~3,000 addresses holding 1 billion tokens — very low holder count suggesting significant concentration. Could not independently verify top-10 holder breakdown (Etherscan 403).

**SILO price performance:** ATH of $0.96 → current ~$0.002–$0.016 (range across platforms due to migration). **99%+ decline from ATH.** Market cap ~$1–2M against $277M TVL. This extreme divergence suggests either: (a) significant governance token selling pressure from vested insiders, (b) lack of retail demand for governance in a professional/institutional user base, or (c) both.

### TVL Assessment

- **$277M TVL** (DeFiLlama, May 2025) across Ethereum, Arbitrum, Base, Optimism
- Silo V2 and Silo V1 are listed separately on DeFiLlama
- TVL growth has been organic across multiple chains — not artificially concentrated
- 39 weekly commits, 9 monthly developers confirms active protocol maintenance
- Annual fees of $1.2M with 9.3x P/S ratio — reasonable for a DeFi lending protocol

---

## 5. RED FLAGS REGISTER

| # | Flag | Severity | Evidence | Why It Matters |
|---|---|---|---|---|
| 1 | **Unaudited "unreleased" contract deployed to mainnet, exploited for $545K** | CRITICAL | QuillAudits analysis, official post-mortem, Cryptopolitan, OKX report (June 2025) | Demonstrates that the protocol's rigorous audit culture does not extend to peripheral/experimental contracts. Attacker was pre-funded via Tornado Cash (targeted, pre-planned). |
| 2 | **3m20s early warning from Hypernative not actionable** | HIGH | QuillAudits, official post-mortem | Real-time monitoring was deployed but insufficient to prevent the attack. Raises questions about incident response procedures. |
| 3 | **Certora FV found CRITICAL vulnerabilities that two professional audit firms missed** | HIGH | LlamaRisk assessment, official V1 audit documentation | Industry-standard professional audits (Quantstamp, ABDK) failed to find what formal verification caught. Implies unknown residual vulnerabilities may still exist in unverified contract components. |
| 4 | **SILO V1 token had uncapped admin-controlled mint function** | HIGH | Etherscan V1 contract analysis, on-chain code | The owner of the V1 token could mint unlimited SILO at any time. Existed for years. No evidence of abuse, but the capability represented a permanent governance integrity risk. Now migrated. |
| 5 | **~44.8% insider/VC supply fully vested and liquid** | HIGH | Token allocation docs, Silopedia; all vesting periods expired by 2024 | Founders, contributors, advisors, and investors hold nearly as much as the community treasury. All tokens unlocked. Governance capture is structurally possible without requiring disclosure. |
| 6 | **Code4rena M-06 finding NOT mitigated** | MEDIUM | Code4rena Mitigation Review report (May 2025): "The wardens confirmed the mitigations for all in-scope findings except for M-06" | One formally-identified vulnerability from competitive audit was accepted as-is (severity adjusted by judges post-sponsor context). The specific risk posed by M-06 requires reading full report. |
| 7 | **SILO V2 token is Pausable — owner can freeze migration** | MEDIUM | On-chain Etherscan code: inherits OpenZeppelin `Pausable` and `Ownable2Step` | Admin can halt token transfers or V1→V2 migration. If admin key is compromised, this creates a freeze-and-ransom scenario. |
| 8 | **veSILO model structurally favors whales** | MEDIUM | Official veSILO docs, governance forum discussion | Locking 80/20 SILO/WETH BLP for 3 years for max governance power systematically disenfranchises smaller holders. High gas on Ethereum further excludes retail governance participation. |
| 9 | **No meaningful original public GitHub contributions from Aiham Jaabari** | MEDIUM | github.com/aiham02: only TrustWallet assets fork and MEV job board fork visible | The named founder's public GitHub shows only forks. Core protocol code may be entirely under the org account without individual attribution. Cannot independently verify founder's coding capability. |
| 10 | **Trail of Bits V2 audit not in ToB public publications index** | LOW | github.com/trailofbits/publications — no Silo entry found | Less critical than Enosys's invisible Coinspect audit (ToB completion confirmed via multiple sources and Code4rena references), but worth noting the specific report is not directly accessible. |
| 11 | **The Defiant "coverage" is sponsored content** | LOW | The Defiant article explicitly labeled as sponsored | The most prominent media coverage is paid marketing, not editorial. Distorts the apparent coverage depth. |
| 12 | **99%+ token price decline from ATH** | LOW | CoinGecko: ATH $0.96, current ~$0.002–$0.016 | May indicate sustained insider selling pressure from fully vested allocations. Could also reflect general DeFi bear market. Context-dependent but worth monitoring. |
| 13 | **Coreum Inc. deadpooled** | LOW | Tracxn classification | Founder's prior blockchain venture failed. Normal in 2018 blockchain era; no evidence of misconduct. Treat as contextual data, not a red flag on its own. |

---

## 6. UNRESOLVED QUESTIONS

1. **What exactly is Code4rena finding M-06 and why was it not mitigated?**
   The full Code4rena report (https://code4rena.com/reports/2025-03-silo-finance) contains the specific M-06 description. The severity was "adjusted by judges" post-sponsor context. Without reading the specific finding and the sponsor's justification, it is not possible to assess whether this represents a real risk or a legitimate out-of-scope edge case.

2. **Who are the 5 members of the team multisig and what are their addresses?**
   The protocol discloses a 5-member core team multisig controls emergency functions. Individual identities, addresses, and the signing threshold are not publicly documented. Cannot assess signer quality or geographic concentration.

3. **Was the leverage contract exploit pre-planned with insider information?**
   The attacker was funded via Tornado Cash — clearly pre-planned. The attacker specifically targeted a pre-release contract that was not formally announced. Whether this required insider knowledge of its existence/vulnerability cannot be determined from on-chain data alone.

4. **What is the exact nature and scope of the unmitigated M-06 finding?**
   Confirmed not fully mitigated. The severity was downgraded by judges after sponsor context. Requires full Code4rena report reading for proper risk assessment.

5. **Are there other unaudited "experimental" contracts currently deployed to mainnet?**
   The June 2025 exploit revealed a category risk: Silo may deploy other peripheral/experimental contracts to mainnet that are not in scope of formal audits. No way to enumerate these from public sources.

6. **What controls were put in place post-exploit to prevent re-occurrence?**
   The official post-mortem was inaccessible (Medium 403). No public post-exploit deployment policy was found via web search.

7. **Why does SILO have 99%+ price decline while TVL remained at $277M?**
   The extreme governance token/TVL divergence is unusual. Understanding whether this represents sustained insider selling, liquidity incentive farming by TVL depositors with no SILO interest, or other dynamics requires deeper Dune analytics investigation.

8. **Full Trail of Bits V2 findings and severity breakdown?**
   Confirmed completed but not publicly indexed in ToB's own repository. Official docs.silo.finance hosts PDF links on Google Drive — these should be archived but were not independently fetched during this research session.

---

## 7. COMPARATIVE ANALYSIS

### Similarities to Known Exploited Protocols
- **No meaningful pattern match to exit scam / rug pull** — Silo passes the most basic test of not being a hit-and-run scheme. Named team, 4+ years of operation, institutional backing.
- **Comparison to Euler Finance hack (March 2023, $197M):** Euler also had multiple audits and the exploit targeted a peripheral feature (donateToReserves). The pattern of "audited core + unaudited peripheral = exploit" is structurally similar to Silo's June 2025 incident, though at a drastically smaller scale.
- **Comparison to Rari Capital / Fuse (April 2022, $80M):** Permissionless markets (like Silo's) that allow any token as collateral face systematic oracle manipulation risk. Fuse's failure illustrates what happens when permissionless listing is combined with low-liquidity collateral and degraded oracles. Silo's isolated design is specifically intended to contain this — but the risk vector exists.

### Tokenomics Sustainability
- **Yield source is clearly identifiable:** Borrower interest rates → lenders. Stability pool mechanics are not Ponzi-dependent. Revenue model is transparent.
- **rFLR / incentive farming risk:** Some TVL may be driven by token incentive programs (veSILO gauge emissions). If incentives are reduced, TVL could compress. This is common in DeFi and not unique to Silo.
- **Protocol-owned liquidity (10% of supply from genesis auction):** This creates a treasury with market-bought liquidity that can sustain incentives without selling from insider allocations.

---

## APPENDIX: KEY SOURCES

### Primary Research Sources
- Silo Finance Exploit Post-Mortem: https://silofinance.medium.com/post-mortem-unreleased-leverage-contract-exploitd-0ab8f37afcbb
- QuillAudits Exploit Analysis: https://www.quillaudits.com/blog/hack-analysis/how-silo-finance-lost-500k
- LlamaRisk Assessment: https://www.llamarisk.com/research/archive-llamarisk-asset-risk-assessment-silo-finance
- Code4rena Silo Finance Report: https://code4rena.com/reports/2025-03-silo-finance
- Silo V2 Audit Documentation: https://docs.silo.finance/docs/audits/
- Silo V1 Audit Documentation: https://devdocs.silo.finance/security/audits-and-formal-verification
- SILO V1 Token Etherscan: https://etherscan.io/token/0x6f80310ca7f2c654691d1383149fa1a57d8ab1f8
- SILO V2 Token Etherscan: https://etherscan.io/token/0xf0b2dd79324a66d2108c961d680f7616e1486bb0
- Token Allocation & Vesting: https://silopedia.silo.finance/silodao/usdsilo/token-allocation-and-vesting
- Aiham Jaabari Crunchbase: https://www.crunchbase.com/person/aiham-jaabari
- Coreum Inc. Tracxn: https://tracxn.com/d/companies/coreum/
- Silo Finance GitHub: https://github.com/silo-finance
- Aiham Jaabari GitHub: https://github.com/aiham02
- DeFiLlama TVL: https://defillama.com/protocol/silo-finance
- Silo Governance Forum: https://gov.silo.finance
- AINvest Exploit Report: https://www.ainvest.com/news/silo-finance-loses-545-000-smart-contract-exploit-silo-price-drops-11-2506/

### Official Sources (Treated as Marketing Material)
- Silo Finance Website: https://www.silo.finance/
- Silopedia: https://silopedia.silo.finance/
- Silo V2 Docs: https://docs.silo.finance
- Silo Medium: https://silofinance.medium.com/

---

*Research conducted under adversarial methodology. Trust hierarchy applied: on-chain data → independent third-party analysis → community intelligence → digital footprints → official communications. Unverified claims labeled. Absence of evidence not treated as evidence of absence.*
