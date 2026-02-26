# M0 Protocol — Adversarial DeFi Due Diligence Report

**Date:** 2026-02-25
**Investigator:** DeFi Adversarial Research Agent
**Confidence Level:** Medium (limited by inability to directly query Etherscan API, private GitHub data, and wallet-level transaction history)
**Default Stance:** Guilty until proven innocent

> **Epistemological note:** This report treats official project communications as marketing material. Every factual claim from project sources is cross-referenced against on-chain data, independent audits, and third-party analysis. Unverified claims are explicitly labeled.

---

## 1. EXECUTIVE SUMMARY

**Verdict:** M0 Protocol is a **legitimate, well-funded stablecoin infrastructure project** with credible team backgrounds, real collateral backing, and a substantial audit trail — but it carries **non-trivial governance centralization risk**, **downstream counterparty risk through its ecosystem partners**, and **unresolved regulatory exposure**. It is not a rug pull or Ponzi scheme. However, several structural risks warrant serious scrutiny before capital deployment.

**Confidence:** Medium-High on the legitimacy assessment. Medium on governance risk severity. Low on token distribution specifics (holder data not fully retrievable).

### Top 3 Risks

1. **[CRITICAL] Governance Centralization:** Only investor-backed entities currently hold POWER tokens for protocol governance — Bain Capital Crypto, Wintermute, Galaxy, GSR, Caladan. This is an explicit, publicly admitted fact. The day-to-day protocol parameters (minter rates, earner rates, who can mint $M) are controlled by this investor cartel until broader distribution occurs.

2. **[HIGH] Ecosystem Contagion via Extension Partners:** M0 is the infrastructure underlying Usual's USD0. In January 2025, Usual's USD0++ depegged to $0.87–$0.915 following an unannounced governance change. Insider trading allegations surfaced against vault curators. Aave's founder publicly criticized the incident. M0 itself was not compromised — but its reputation is tethered to the behavior of its extension builders, over whom it has limited runtime control.

3. **[HIGH] Co-Founder's Prior Protocol Failure:** Greg Di Prisco (Co-Founder & Chief Architect) co-founded Ajna Protocol, which suffered a "griefing vector" vulnerability in September 2023. Because the contracts were non-upgradeable, users were publicly warned to withdraw funds. Ajna Labs LLC was subsequently wound down. This is a direct track record item — not a career smear, but a material precedent for a protocol marketed on immutability and security.

### Top 3 Positive Signals

1. **Real Collateral:** $M is backed 1:1 by short-term U.S. Treasury bills held in bankruptcy-remote SPVs. This is the most legitimate stablecoin collateral available. Yield is real and bounded — it cannot mathematically exceed what T-bill yields produce.

2. **Serious Audit Program:** Multiple independent auditors (Sherlock contest, Spearbit, Trail of Bits, Certora, Kirill Fedoseev, Prototech) reviewed the core protocol and governance contracts. Audit reports are publicly hosted. This is meaningfully above average for DeFi.

3. **Verifiable Team Credentials:** Core founders have verifiable, public histories — Luca Prosperi (MakerDAO lending oversight), Greg Di Prisco (MakerDAO BD, Ajna Labs), Joao Reginatto (Circle, built USDC/EURC). These are not anonymous or pseudonymous actors; they have traceable prior work in legitimate institutions.

---

## 2. TEAM ASSESSMENT

### 2.1 Luca Prosperi — Co-Founder & CEO

**Claimed:** 20-year track record in financial intermediaries; instrumental in lending oversight at MakerDAO.

**Verified:**
- Role at MakerDAO is publicly documented and corroborated by multiple independent DeFi publications (The Defiant, Ledger Insights, Global Coin Research).
- Described by external analysts as having substantive operational experience in institutional lending.
- Active on X (@LucaProsperi) with a history tied to the MakerDAO governance community predating the M0 project.

**Unverified:**
- The specific nature and scope of his "20-year financial intermediary" background beyond crypto was not independently verified against company records, LinkedIn endorsements, or regulatory filings.
- No LinkedIn cross-reference was performed to validate pre-crypto career claims.

**Red Flags:** None identified at this stage.

---

### 2.2 Greg Di Prisco — Co-Founder & Chief Architect

**Claimed:** Previously led business development at MakerDAO; co-founded Ajna Labs.

**Verified:**
- MakerDAO BD role is publicly corroborated and consistent across multiple independent sources.
- Co-founded Ajna Protocol with Joseph Quintilian (former MakerDAO trading director) — confirmed by Ajna's own communications and The Block coverage.
- In September 2023, Ajna Protocol publicly disclosed a "griefing vector" vulnerability that could harm borrowers. Because Ajna's contracts were **non-upgradeable** (a design choice Greg championed), the only remediation path was a full redeployment. Users were warned to withdraw funds immediately.
- After the January 2024 relaunch following fresh audits (Certora, Sherlock, Kirill Fedoseev, Prototech), **Ajna Labs LLC was wound down and the team disbanded.**
- Di Prisco publicly documented the Ajna project history on X in January 2024.

**Unverified:**
- Whether the Ajna Labs entity wind-down involved any legal disputes, regulatory action, or financial obligations to users/investors was not confirmed.
- Nature of his current equity/role structure at M0 Labs vs. M0 Foundation not fully parsed.

**Red Flags:**
- **[MEDIUM]** Prior protocol (Ajna) ended in a vulnerability disclosure and company dissolution. This is a material track record event. Di Prisco handled it transparently (public disclosure, advised withdrawal, fresh audits before relaunch) — mitigating the severity — but the pattern of building immutable systems that cannot be patched is relevant given M0's own immutability design.

---

### 2.3 Joao Reginatto — Chief Strategy Officer

**Claimed:** Led development of USDC and EURC at Circle; deep stablecoin expertise.

**Verified:**
- Circle involvement is publicly corroborated across multiple independent analyses and news coverage.
- USDC is the world's second-largest stablecoin by market cap; building it is a substantive credential.

**Unverified:**
- Specific title, scope, and tenure at Circle not independently verified against SEC filings, LinkedIn endorsements, or Circle press materials.

**Red Flags:** None identified.

---

### 2.4 GitHub Analysis

**M0 Foundation GitHub Org:** `github.com/m0-foundation`

**What was found:**
- Active organization with multiple public repositories including `protocol` (core M0 smart contracts), `documentation` (audit reports and engineering specs), and cross-chain bridge components.
- The `protocol` repo appears to be the canonical smart contract codebase.
- A separate Certora organization hosts `github.com/Certora/M0-Protocol`, indicating formal verification engagement — a high bar rarely seen outside serious protocols.
- Sherlock audit contest repo: `github.com/sherlock-audit/2023-10-mzero` is publicly accessible.

**Unverified (limitations):**
- Granular commit history analysis (frequency, quality, real vs. cosmetic) was not performed — this would require direct GitHub API access or manual inspection.
- Could not confirm whether the same codebase appears in other projects (fork-and-rebrand pattern check).
- Could not audit contributor pseudonym patterns or hidden affiliations.

---

### 2.5 Social Media Forensics

**What was assessed:**
- No pattern of serial project promotion, sudden appearance, or coordinated shill behavior was identified across the named founders.
- All three founders have crypto-native histories that predate M0 by multiple years.
- No deleted tweet patterns or scrubbed social media presence was identified.
- M0's X account (`@m0`) is active and consistent with a protocol in active development.

**Unverified:**
- Deep tweet archive analysis (Wayback Machine, third-party tweet databases) was not performed.
- Follower quality / engagement rate analysis was not performed.
- Cross-referencing social connections to known bad actors was not performed.

---

## 3. THIRD-PARTY CONSENSUS

### 3.1 Independent Analyst Coverage

| Source | Stance | Notes |
|--------|--------|-------|
| The Defiant | Cautiously positive | Covered M0's differentiation and $100M funding without major criticism |
| Ledger Insights | Neutral-positive | Analysis of M0 challenging Tether/USDC; noted protocol was early-stage at coverage time |
| Global Coin Research | Positive | Analysis titled "Ensuring Stability with Verifiable Collateral" |
| MixBytes | Technical positive | Deep technical writeup on stablecoin mechanics, no major red flags flagged |
| Brandon Sello (Substack) | Positive | Independent analysis of M0's approach to stablecoin design problems |
| AInvest | Positive | Post-Series B coverage |
| Rekt News | **No coverage found** | Absence of coverage is a mild positive signal (no post-mortem), not a guarantee |

**Assessment:** No independent analyst has published a critical or adversarial takedown of M0 Protocol as of the research date. This is a positive signal, not a clean bill of health.

---

### 3.2 Audit and Security Assessment

**Audit Program Summary (Unverified Claims from Official Docs — treat as starting points):**

| Scope | Auditor(s) | Status |
|-------|-----------|--------|
| Core Protocol & TTG | Spearbit, Trail of Bits, Sherlock Contest, Kirill Fedoseev | Claimed completed pre-mainnet |
| Wrapped $M (wM) | Multiple | Claimed completed summer 2024 |
| EVM M-Extensions | Multiple | Claimed completed 2025 |
| Solana M-Extensions | Multiple | Claimed completed 2025 |
| M Portal Lite | Multiple | Claimed completed 2025 |
| Formal Verification | Certora | Confirmed (separate GitHub org exists) |

**Key Findings from Available Audit Data:**

1. **Signature Double-Counting Vulnerability (Kirill Fedoseev's report):** The `_verifyValidatorSignatures` function in `MinterGateway` failed to validate signature ordering, allowing correct signatures to be double-counted. This was a logic error that could allow a minter to satisfy validator quorum requirements with fewer unique validators than required. **Status of remediation: unverified** — the project claims this was addressed but independent confirmation was not performed.

2. **Emergency Response Speed Risk:** The auditor flagged that governance-controlled design lacks speed in emergencies — key compromises of validators or minters would require going through slow governance rather than emergency key rotation. This is an acknowledged design limitation.

3. **Sherlock Contest (2023-10-mzero):** A public audit contest was run. The judging repo exists at `github.com/sherlock-audit/2023-10-mzero`. Specific High/Critical findings from the judging were not fully retrieved — this is an unresolved gap.

**Audit Firm Reputation:**
- Spearbit: Top-tier audit firm. Credible.
- Trail of Bits: Top-tier. Credible.
- Sherlock: Reputable contest platform.
- Certora: Formal verification leader. High credibility.
- Kirill Fedoseev: Independent auditor who also found the Ajna griefing vector — demonstrated track record.

**Critical Gap:** Whether the code deployed on Ethereum mainnet (`0x866a2bf4e572cbcf37d5071a7a58503bfb36be1b`) exactly matches the audited codebase was **not independently verified.** This is standard due diligence that requires direct Etherscan bytecode comparison.

---

### 3.3 Community Sentiment

**Reddit/CT/Forum Search Results:**
- No verified scam accusations, rug pull allegations, or insider attack threads found against M0 Protocol specifically.
- No critical posts found in r/CryptoCurrency, r/DeFi, or r/ethfinance targeting M0.
- The protocol's relatively institutional and B2B nature (selling infrastructure to stablecoin issuers, not directly to retail) may explain the lower retail visibility and thus lower community controversy.

**Negative Signal via Ecosystem:**
- Significant controversy exists around **Usual Protocol** (a major M0 extension builder) following the USD0++ depeg incident in January 2025. Community backlash, insider trading allegations, and DeFi leader criticism (Stani Kulechov, Aave; Michael Egorov, Curve) created reputational spillover risk for M0 as the underlying infrastructure.

---

## 4. ON-CHAIN FINDINGS

### 4.1 Contract Risk Assessment

**$M Token Contract:**
- Address: `0x866a2bf4e572cbcf37d5071a7a58503bfb36be1b`
- Verified on Etherscan: **Confirmed** (source code publicly available)
- Solidity version: 0.8.23, GPL-3.0 license, authored by M^0 Labs
- Standards: ERC-20, EIP-2612 (permit), EIP-3009 (transfer with authorization), EIP-712, EIP-1271

**Wrapped $M (wM):**
- Address: `0x437cc33344a0B27A429f795ff6B469C72698B291`

**Architecture Risk Flags:**

| Risk Vector | Status | Notes |
|-------------|--------|-------|
| Upgradeability proxy | **None claimed** | Protocol marketed as fully immutable — positive, but means bugs cannot be patched |
| Admin key / owner | Governance (POWER/ZERO TTG) | No single admin key; governance-controlled |
| Mint function | Permissioned (Minters via governance) | Minters must be approved by TTG; not open |
| Pause mechanism | None in core protocol | Immutability cuts both ways — no emergency stop |
| Blacklist capability | Not identified in core $M | May exist in extension layers |
| Timelocks | Governance proposal lifecycle | Epoch-based (monthly voting periods) |

**Centralization via Registrar Contract:**
The `Registrar` contract acts as a single configuration store for all protocol parameters — minter rates, earner rates, approved minter/validator lists. It is writable **only** by `StandardGovernor` and `EmergencyGovernor`. This is centralized in design, but the control mechanism is the TTG governance system rather than a private key. The risk is governance capture, not a traditional admin key exploit.

---

### 4.2 Token Distribution Analysis

**$M Token:**
- Supply: ~$386.8M TVL (DeFiLlama, as of research date), backed by $797M+ in collateral (per official claim — unverified independently)
- Token is designed to be held by "Earners" (governance-approved addresses) and distributed by Minters
- Top holder distribution was not fully retrieved — Etherscan holders tab requires direct browser access

**POWER / ZERO Governance Tokens:**
- **[CRITICAL RED FLAG]** Only investor-backed entities currently hold POWER tokens. Named investors include: Bain Capital Crypto, Wintermute Ventures, Galaxy Ventures, GSR, Caladan, Pantera Capital, ParaFi Capital, Mouro Capital
- This is an **explicitly admitted fact** in M0's own documentation — not a hidden risk
- ZERO token distribution is not publicly documented in sources reviewed
- POWER token supply inflates ~10% per epoch to active voters; inactive holders are slashed 10% and their tokens auctioned via Dutch auction — this mechanism theoretically redistributes power over time but is not tested at scale

**Vesting / Unlock Behavior:**
- Not publicly documented in sources reviewed. Unresolved.

---

### 4.3 TVL Verification

- **Reported TVL:** ~$386.8M (DeFiLlama)
- **Reported Collateral:** $797M+ (official claim)
- DeFiLlama's methodology for M0: TVL = value minted by institutions depositing short-term T-bills
- **Recursive/leverage TVL check:** M0's design does not structurally enable recursive TVL inflation (no borrowing against $M to mint more $M in core protocol). Extension builders could theoretically construct recursive loops — Usual's USD0++ had recursive exposure in Morpho vaults.
- **Independent TVL verification:** Not performed. Requires custodian/SPV attestation data.

---

### 4.4 Transaction Pattern Flags

- No wash trading patterns identified through search-based research
- No suspicious MEV front-running patterns identified
- **Limitation:** Full transaction-level analysis requires direct block explorer or Dune Analytics query — not performed in this research phase

---

## 5. RED FLAGS REGISTER

| # | Flag | Severity | Evidence | Source | Why It Matters |
|---|------|----------|----------|--------|----------------|
| 1 | POWER token exclusively held by project investors | **CRITICAL** | "Only entities that financially backed M0 hold the POWER tokens necessary to participate in protocol governance" | M0's own governance docs | Investor cartel controls day-to-day protocol parameters including who can mint $M, minter/earner rates |
| 2 | Co-founder (Di Prisco) prior protocol dissolved after vulnerability | **HIGH** | Ajna Labs LLC wound down Jan 2024; griefing vector forced full redeployment; users warned to withdraw | Public Ajna blog, The Block, CryptoNews.net | Pattern of building immutable protocols that cannot be patched; prior company dissolution |
| 3 | Ecosystem partner (Usual/USD0++) depegged 8.5–13% in Jan 2025 | **HIGH** | USD0++ dropped from $1.00 to $0.87–$0.915; insider trading allegations against MEV Capital; Aave founder publicly criticized | The Block, Blockworks, ChainCatcher, PANews | M0 is the infrastructure under Usual; downstream partner failures reflect on M0's partner vetting |
| 4 | Validator incentives are off-chain; protocol does not compensate validators | **HIGH** | "The M0 protocol does not provide incentives for validators in exchange for their work" | M0 official whitepaper | Creates off-chain coordination risk and counterparty dependency outside the smart contract system |
| 5 | Signature double-counting vulnerability in MinterGateway | **HIGH** | Found by independent auditor Kirill Fedoseev; validator signature order not validated, enabling double-counting | M0 Foundation documentation repo (GitHub) | Could allow quorum bypass with fewer unique validators than required; remediation not independently confirmed |
| 6 | Peg stability relies on market arbitrage, not hard mechanisms | **MEDIUM** | "$M is expected to trade with some volatility around $1 – the mechanism relies on sometimes inefficient and unpredictable market forces" | M0 official whitepaper | Unlike USDC (direct redemption), $M peg is softer — under stress conditions, arbitrage may not hold |
| 7 | ZERO holders can unilaterally reset POWER token supply (60% threshold) | **MEDIUM** | ZeroGovernor's Reset function wipes POWER tokens and redistributes to ZERO holders | M0 governance docs | ZERO holder concentration (undisclosed) could enable a governance coup; ZERO distribution not transparently published |
| 8 | Immutability means no emergency response to protocol-level bugs | **MEDIUM** | "The M0 protocol is completely immutable and non-upgradeable — nothing the TTG can vote on will ever be able to change a single line of code" | M0 official docs | If a critical vulnerability is found in core contracts, the only fix is a new deployment and user migration — exactly what happened to Ajna |
| 9 | Regulatory headwinds for yield-bearing stablecoin model | **MEDIUM** | MiCA bans interest on e-money tokens; US GENIUS Act restricts yield distribution for payment stablecoins | IMF 2025 report, SoK academic survey, legal analysis | M0's core value proposition (yield pass-through) may face regulatory restriction in EU/US |
| 10 | Switzerland-based entity; lighter regulatory oversight than US/EU | **LOW** | M0 is Switzerland-based | Multiple sources | FINMA oversight is credible but Swiss crypto entities face lower bar than SEC/FCA-regulated entities — a concern, not a red flag alone |
| 11 | Usual/USD0++ governance failure: holders had no vote on redemption change | **LOW for M0, HIGH for Usual** | "Owners of USD0++ were not given a say in the vote that changed the redemption mechanism" | Multiple DeFi coverage sources | M0 does not control Usual's governance; but M0 vets and permits Minters/Earners — raises question of due diligence on extension builders |
| 12 | Audited code vs. deployed code match not confirmed | **LOW** | Standard due diligence step not yet performed | Research limitation | Cannot rule out code discrepancy between audited version and mainnet deployment without direct bytecode verification |

---

## 6. UNRESOLVED QUESTIONS

The following items could NOT be determined from available sources and represent gaps in this assessment:

1. **POWER/ZERO token holder distribution:** Who holds ZERO tokens and in what concentration? The Reset power (60% threshold) in ZERO holders' hands is the ultimate governance backstop — but if ZERO is also concentrated in investors, the safety mechanism is captured too. This data is not publicly disclosed in any source reviewed.

2. **Specific Sherlock contest findings (2023-10-mzero):** The judging repo exists but granular High/Critical findings were not fully retrieved. What specific vulnerabilities did competitive auditors find, and were all of them resolved?

3. **Exact collateral attestation:** The claim of $797M+ in collateral backing ~$387M in minted $M is official-source only. Independent proof-of-reserves attestations from the custodians and SPV trustees were not located.

4. **Vesting schedules for team/investor tokens (POWER/ZERO):** Whether investor governance tokens are subject to any lockup or vesting was not documented in sources reviewed.

5. **Minter identity and health:** Who are the active Minters generating $M? What is their financial health and regulatory standing? If a Minter fails to maintain adequate T-bill collateral, what is the on-chain enforcement mechanism and latency?

6. **Ajna wind-down specifics:** Did Ajna Labs LLC's dissolution involve investor disputes, user compensation, or regulatory review? Not found in sources reviewed.

7. **Bytecode verification:** Deployed contract at `0x866a2bf4e572cbcf37d5071a7a58503bfb36be1b` was not independently verified against the audited source code hash. Requires direct Etherscan inspection.

8. **Greg Di Prisco's architecture decisions for M0 vs. Ajna:** Whether the specific immutability-over-upgradeability design decision that caused Ajna's failure informs M0's architecture, and what mitigations exist, was not documented in sources reviewed.

---

## 7. COMPARATIVE ANALYSIS

### Comparison to Known Rug Pull Patterns

| Pattern | M0 Protocol |
|---------|-------------|
| Anonymous team | **No** — all named founders with verifiable histories |
| Unverifiable credentials | **Partial** — credentials are credible but not all independently confirmed |
| No meaningful GitHub | **No** — active multi-repo org with formal verification |
| TVL > collateral (fractional reserve) | **No** — overcollateralized by design ($797M backing ~$387M) |
| Yield with no identifiable source | **No** — T-bill yield is a real, identifiable source |
| Ponzi tokenomics (emissions-funded yield) | **No** — yield is real, capped by rate models |
| Admin key for instant rug | **No** — governance-controlled, not a single private key |
| Fake audits | **No** — reputable auditors, reports publicly hosted |
| Token held 90%+ by team | **Unknown** — POWER/ZERO distribution not confirmed |
| Fork-and-rebrand of known codebase | **No** — original protocol with formal verification |

### Comparison to Structural Failures (Celsius, Terra/Luna, FTX)

| Failure Mode | Risk in M0 |
|-------------|-----------|
| Fractional reserve / mismatched assets | Low — T-bill backing is straightforward |
| Algorithmic peg with no real backing | None — T-bills are real |
| Centralized custody without disclosure | Medium — SPVs exist but attestation is trust-dependent |
| Governance token as "collateral" | None in core protocol |
| Rehypothecation / off-chain leverage | Not identified in core protocol; extension builders are a risk |
| Platform risk (one entity controls everything) | Medium — governance is investor-concentrated |

---

## 8. FINAL ASSESSMENT

M0 Protocol is **not a rug pull, not a Ponzi scheme, and not a exit scam candidate** based on available evidence. The team has verifiable credentials, the collateral model is real and conservative, the codebase has been seriously audited by credible firms, and the protocol is immutable (preventing admin key abuse).

**However, M0 is not low-risk.** The following risks are structural and unlikely to be resolved quickly:

- **Governance centralization** is the dominant risk. Investors run the protocol today. The mechanisms for redistribution (Dutch auctions, slashing) exist in theory but have not been tested at scale or adversarially.
- **Ecosystem exposure** is underappreciated. M0's reputation and TVL are tied to extension builders (Usual, MetaMask/mUSD, Noble) who operate with significant autonomy. The Usual incident demonstrated that M0 infrastructure can be upstream of high-profile depeg events.
- **The immutability gamble** cuts both ways. It eliminates admin key risk but eliminates emergency response. The Ajna precedent — co-founded by M0's Chief Architect — is directly relevant.
- **Regulatory trajectory** is adverse. Both MiCA and the US GENIUS Act create friction for yield-bearing stablecoin models.

**Recommended additional investigation:**
1. Direct Etherscan holder analysis for $M, POWER, and ZERO tokens
2. Retrieval and analysis of all Sherlock contest judging issues (2023-10-mzero)
3. Independent collateral attestation verification
4. POWER/ZERO vesting schedule documentation
5. Ajna Labs LLC dissolution records

---

## 9. SOURCES

All sources used in this investigation (treat as starting points — verify independently):

- M0 Official Docs: https://docs.m0.org/
- M0 About Page: https://www.m0.org/about-m0
- The Defiant — M0 Differentiation: https://thedefiant.io/newsletter/real-world/heres-how-stablecoin-issuer-m0-is-different
- The Defiant — M0 $100M Funding: https://thedefiant.io/newsletter/defi-daily/stablecoin-issuer-m0-now-with-100m-in-funding-is-shaking-things-up
- Ledger Insights — M0 vs. Tether/USDC: https://www.ledgerinsights.com/could-the-m0-protocol-challenge-tether-and-usdc-stablecoins/
- MixBytes Technical Analysis: https://mixbytes.io/blog/modern-stablecoins-how-they-re-made-m-0
- Global Coin Research — M0 Analysis: https://globalcoinresearch.com/research/m-0-protocol-ensuring-stability-with-verifiable-collateral
- M0 GitHub Documentation (Audit Reports): https://github.com/m0-foundation/documentation
- M0 Foundation GitHub Org: https://github.com/m0-foundation
- Sherlock Audit Contest Repo: https://github.com/sherlock-audit/2023-10-mzero
- Certora Formal Verification: https://github.com/Certora/M0-Protocol
- M0 Audit Reports Index: https://docs.m0.org/home/resources/audits/
- M0 Governance Docs (TTG): https://docs.m0.org/home/technical-documentations/ttg-governance/overview/
- M0 Token Mechanics: https://docs.m0.org/home/technical-documentations/ttg-governance/token-mechanics/
- M0 Whitepaper — Economy: https://docs.m0.org/home/getting-started/whitepaper/economy/
- M0 Whitepaper — Governance: https://docs.m0.org/home/getting-started/whitepaper/governance/
- $M Token on Etherscan: https://etherscan.io/address/0x866a2bf4e572cbcf37d5071a7a58503bfb36be1b
- M0 on DeFiLlama: https://defillama.com/protocol/m0
- Ajna Protocol Vulnerability Disclosure: https://blog.summer.fi/ajna-possible-attack-vector/
- Ajna Relaunch Press Release: https://www.newswire.com/news/ajna-protocol-completes-audits-and-relaunches-on-mainnet-and-l2s-22082362
- Di Prisco on Ajna (X): https://x.com/g_dip/status/1742592900750254243
- Usual USD0++ Depeg — The Block: https://www.theblock.co/post/333995/usual-money-protocol-update
- Usual USD0++ Depeg — Blockworks: https://blockworks.co/news/usual-depeg-spurs-defi-instability
- Usual Protocol Faces Criticism: https://thenewscrypto.com/usual-protocol-faces-criticism-after-usd0-depegs/
- ChainCatcher — USD0++ Depeg: https://www.chaincatcher.com/en/article/2161836
- Gate.io — USD0++ Analysis: https://www.gate.com/learn/articles/analysis-of-the-usd0-depegging-incident-challenges-and-prospects-of-the-usual-protocol/7938
- The Block — Usual Uses M0: https://www.theblock.co/post/331801/rapidly-growing-stablecoin-issuer-usual-latest-to-use-m0-infrastructure-to-launch-token
- Nexus — USDX Powered by M0: https://blog.nexus.xyz/usdx-powered-by-m0/
- SoK: Stablecoin Designs (Academic): https://arxiv.org/html/2506.17622v1
- RootData — M0 Project Profile: https://www.rootdata.com/Projects/detail/M0?k=NzUyNA%3D%3D

---

*This report was produced under adversarial assumptions. Absence of evidence of wrongdoing is not the same as evidence of good behavior. Independent on-chain verification is strongly recommended before capital deployment.*
