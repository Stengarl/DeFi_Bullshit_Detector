# Spiko — Adversarial DeFi Due Diligence Report

**Date:** 2026-03-05
**Investigator:** Claude Sonnet 4.6 (Adversarial Research Framework)
**Confidence Level:** HIGH (regulated entity, extensive public record)
**Research Scope:** Phase 1–4 (Team, Third-Party Intelligence, On-Chain, Comparative)

---

## Executive Summary

Spiko is a Paris-based fintech that tokenizes EU-regulated money market funds (EUTBL and USTBL) on public blockchains. It is **not a traditional DeFi protocol** — it is a regulated financial product issuer using blockchain infrastructure. As such, the relevant risk framework differs substantially from permissionless DeFi.

**Verdict:** **LOW-TO-MODERATE RISK** for its core regulated product. **ELEVATED RISK** for users engaging via the Morpho DeFi lending layer or holding on newer, less-audited chains (Stellar, Starknet, Etherlink).

**Confidence:** HIGH — Both founders have deeply verifiable, independently crosschecked public records. AMF regulatory approval is independently verifiable through third-party fund registries. CACEIS custodianship confirmed through Crédit Agricole press room. No fraud signals identified across any research layer.

---

### Top 3 Risks

1. **Undisclosed multisig governance** — The super-admin group that can upgrade all smart contracts is described as a multisig, but the composition (signers, threshold, timelock duration) has never been publicly disclosed. This is the single most material smart contract governance failure.

2. **Critical vulnerability in Stellar contracts (production)** — Halborn's October 2025 audit of Spiko's Stellar smart contracts found a **Critical severity vulnerability** in the redemption logic (tokens burned from wrong address, risking permanent fund lockup). Stellar holds $337M TVL — the largest chain. The vulnerability was patched, but its discovery post-deployment is concerning.

3. **Audit staleness on EVM contracts** — The only EVM audit was conducted by Trail of Bits in **October 2023**. Since then, Spiko has added CCIP cross-chain functionality, Morpho integration, and expanded to 7 chains. No public evidence of a follow-up EVM audit exists.

---

### Top 3 Positive Signals

1. **Genuine regulatory compliance, independently verified** — UCITS SICAV status (ISINs FR001400ODL1, FR001400ODM9) is verifiable on Sicavonline, Quantalys, MarketScreener, and Bloomberg. AMF approval is real, not marketing.

2. **Founders have the single most verifiable backgrounds encountered in DeFi research** — Hyppolite: Corps des Mines, Harvard Fulbright, French Treasury deputy head. Michon: École Polytechnique, Palantir, French ministerial tech advisor. Academic papers trace back to 2016. These are not manufactured identities.

3. **Institutional validation from adversarial third parties** — Index Ventures (tier-1 VC), CACEIS Bank (Crédit Agricole subsidiary with €5.3T AUC), Arbitrum DAO STEP 2 selection after 50+ applicant competitive process (89% approval rate), PwC financial audit.

---

## 1. Team Assessment

### Paul-Adrien Hyppolite — Co-Founder & CEO

**Verified credentials:**
- École Normale Supérieure (normalien) — cross-verified via CEPR, Harvard CES, academic publications
- Harvard University visiting researcher 2015–2016 (Arthur Sachs and Fulbright scholar) — cross-verified via Harvard CES faculty page
- Corps des Mines, Mines ParisTech 2016–2019 — consistent across CEPR, CrunchBase, NFT Paris speaker profile
- French Treasury: Deputy Head, Savings and Financial Markets Division — consistent across 8+ independent sources
- European Commission: senior civil servant role — consistent across multiple sources
- Antin Infrastructure Partners and ArianeGroup — mentioned across CrunchBase, The Org

**Academic footprint (HIGH trust — pre-Spiko):**
- Published paper on Greek Depression / national balance sheets (2016) — indexed at Crisis Observatory, Harvard
- VoxEU column (May 2017) — CEPR platform
- Article on AI and the Economy in *Pouvoirs* journal (2019)
- Multiple papers on Eurozone crisis and euro area break-up costs

**GitHub:** No personal GitHub profile found. Appropriate for a policy/economics-background CEO. Engineering work is in the `spiko-tech` org (not attributed to him personally).

**Social media:** Active on X as @pahyppolite. Promotes Spiko. No evidence of prior project shilling, deleted content, or connections to known bad actors. Account predates Spiko (academic/policy content visible from prior years).

**Red flags found:** None.

---

### Antoine Michon — Co-Founder & COO

**Verified credentials:**
- École Polytechnique and Mines Paris (engineering, applied mathematics) — consistent across CrunchBase, LinkedIn, EU-Startups
- French Prime Minister's Digital Directorate (project manager, 2019–2020) — consistent across multiple sources
- Cabinet of French Minister of Public Sector Transformation (tech advisor, 2020–2022) — consistent across multiple sources
- Palantir Technologies (deployment strategist) — consistent across multiple sources
- Flowbird Group (project manager) — mentioned on CrunchBase
- Bloomberg LP (quant research intern) — consistent across sources
- European Central Bank (market operations analysis intern) — mentioned across sources
- Paris Fire Brigade (paramedic lieutenant) — an unusual detail that independently confirms his identity

**GitHub:** No public personal GitHub profile found. Engineering contributions go through spiko-tech org.

**Red flags found:** None.

---

### Engineering Team

**GitHub org:** `spiko-tech` — created June 14, 2023. Two public repos visible:
- `spiko-tech/contracts`: 218 commits, primary language JavaScript (79.9%) and Solidity (18.7%). 12 stars, 2 forks.
- Stellar contracts (separate, Halborn-audited)

**Code quality assessment:** OpenZeppelin-based EVM architecture (battle-tested base). EVM version: Cancun, Solidity 0.8.24 — current. Stellar deployment uses Soroban (new, less battle-tested). No evidence of fork-and-rebrand pattern. No copies of the codebase appearing in other projects. No deleted repos or suspicious private commits identified.

**Unverified:** Individual engineer identities and their broader contribution history are not public.

---

## 2. Third-Party Consensus

### Audits

#### Trail of Bits — EVM Contracts (October 2023)
- **Scope:** Core token contract, redemption contract, oracle contract, permission manager
- **Report:** Publicly linked from GitHub README at `github.com/trailofbits/publications/blob/master/reviews/2023-10-spiko-securityreview.pdf`
- **Firm reputation:** Top-tier, used by Ethereum Foundation, leading DeFi protocols
- **Limitation:** Audit conducted in October 2023. Significant new functionality added since (CCIP, Morpho, multi-chain) without confirmed follow-up EVM audit
- **Specific findings:** Not accessible without PDF download; the number and severity of original findings are unverified in this research

#### Halborn — Stellar Smart Account Contracts (September 16–18, 2025)
- **Scope:** Spiko-Tech Stellar Contracts GitHub repository
- **Findings:** 5 total — **1 Critical, 0 High, 0 Medium, 1 Low, 3 Informational**
- **Critical finding:** Redemption logic executed token burns from user account rather than the redemption contract's escrow balance. In production, this would cause transactions to revert and permanently lock escrowed funds.
- **Other issues:** Admin role could be renounced without recovery mechanism; idempotency keys could be consumed without state change; initialization outside constructors; insufficient documentation
- **Resolution:** 100% of findings remediated (commits from September 21 – October 3, 2025)
- **Halborn recommendation:** Follow-up assessment within 6 months or after material code changes
- **Assessment:** The critical finding was caught before funds were at imminent risk, but it demonstrates that Stellar was deployed with production-grade contract logic errors. The EVM contracts had similar risk-level architecture questions (UUPS, centralized admin); if the Stellar analogue had a critical flaw, the absence of a 2024/2025 EVM re-audit is a meaningful gap.

### Independent Media Coverage
- **Rekt News:** No coverage. (Positive signal — not hacked or exploited.)
- **The Defiant:** One article — Spiko-Concordium partnership for trade finance. Framing positive.
- **Ledger Insights:** Multiple articles covering Spiko launches and funding. No critical analysis; reporting is press-release adjacent.
- **The Block:** Covered Series A funding round factually. No investigative or critical coverage.
- **DL News:** No coverage found.
- **Ethresear.ch / governance forums:** Arbitrum STEP 2 forum discussion is substantive — no critical concerns raised, 89% DAO approval after 50+ applicant evaluation.

**Assessment of media coverage:** No critical or adversarial coverage exists. This is atypical for a DeFi protocol — but Spiko is arguably not a DeFi protocol in the conventional sense. It is a regulated fintech using blockchain rails. Its risks are TradFi risks (regulatory, custodial, counterparty) rather than DeFi risks (MEV, rug, oracle manipulation).

### Community Sentiment

**Finary community (independent French personal finance forum):**
- Users use Spiko for idle cash management
- Positive: fast withdrawals (same-day SEPA), no spread on FX, simple UX
- Negative: appeal declining as ECB rates fall; competition from Revolut, Trade Republic
- No fraud concerns, no trust concerns — the community debates competitiveness vs. TradFi alternatives, not safety

**Reddit/DeFi:**
- No specific Spiko threads found on r/DeFi, r/CryptoCurrency, or r/ethfinance
- Absence of criticism is notable but unsurprising given its regulatory positioning

**Arbitrum DAO:**
- 89% voted in favor of STEP 2 allocation. Only 0.01% voted against.
- Matthew Fiebach (Entropy Advisors co-founder) publicly praised Spiko's presence in DAO governance as an "unbelievable accomplishment for the whole crypto space"

---

## 3. On-Chain Findings

### Contract Addresses

| Token | Network | Address |
|-------|---------|---------|
| EUTBL | Ethereum | `0xa0769f7a8fc65e47de93797b4e21c073c117fc80` |
| EUTBL | Arbitrum One | `0xcbeb19549054cc0a6257a77736fc78c367216ce7` |
| USTBL | Ethereum | `0xe4880249745eac5f1ed9d8f7df844792d560e750` |
| USTBL | Arbitrum One | Via Arbiscan (arbiscan.io) |

### Smart Contract Risk Assessment

**Upgradeability (HIGH CONCERN):**
All EVM contracts use UUPS (Universal Upgradeable Proxy Standard). The super-admin group, controlled by a multisig wallet, has full authority to upgrade contracts. This is standard in regulated fintech (enables regulatory compliance updates) but means token holders face non-trivial admin key risk.

**Multisig disclosure gap (CRITICAL CONCERN — governance, not fraud):**
The multisig controlling contract upgrades has **never been publicly described**:
- Number of signers: Unknown
- Signature threshold (e.g., 2-of-3, 3-of-5): Unknown
- Timelock duration: Unknown
- Identity of signers: Unknown

This is the most significant transparency failure. For a regulated TradFi entity, the AMF may be aware of this governance structure as part of the licensing, but public users have no independent way to verify that upgrades are sufficiently secured.

**Centralized operational roles (MEDIUM CONCERN):**
- **Daily-operator:** Internal relayer mints new tokens for investors. Centralized minting.
- **Exceptional-operator:** Can pause/unpause the token. Emergency brake exists but is centrally held.
- **Oracle-operator:** Internal relayer publishes daily NAV. Centralized oracle for valuation.

These centralized roles are mitigated by the regulatory framework — AMF supervision theoretically constrains abuse — but smart contract enforcement of these constraints is not independently verifiable without the multisig details.

**Permission Manager architecture:**
Cap of 256 permission groups. Allowlist-based: only KYC-verified addresses can hold Spiko tokens. This restricts composability with permissionless DeFi but reduces MEV and flash-loan attack surface significantly.

### TVL Analysis

**Total TVL (DeFiLlama, as of research date): ~$1.024B**

| Chain | TVL | % of Total |
|-------|-----|------------|
| Stellar | $337.34M | 32.9% |
| Arbitrum | $317.71M | 31.0% |
| Polygon | $220.37M | 21.5% |
| Ethereum | $69.06M | 6.7% |
| Base | $33.5M | 3.3% |
| Starknet | $33.28M | 3.2% |
| Etherlink | $12.89M | 1.3% |

**CONCERN:** Stellar has the largest single-chain TVL ($337M) and was the chain where a Critical vulnerability was found by Halborn in October 2025. Though fixed, the ratio of critical bugs found per deployment is elevated. As Spiko rapidly expands to more chains (7 chains in <2 years), the attack surface widens without confirmed corresponding audit coverage on each new chain.

**TVL legitimacy:** DeFiLlama confirms TVL. Arbitrum DAO independently corroborated >$200M on Arbitrum. Given the UCITS structure and CACEIS custodianship, inflated/recursive TVL is structurally prevented — underlying assets are real T-Bills in segregated custody.

### Token Distribution Analysis

**USTBL on Ethereum mainnet:**
- Total supply: ~54.6M USTBL
- Holders: **24 addresses**
- Concentration: Extremely high, but substantially explained by cross-chain bridging (Arbitrum deployment has 715 holders; Polygon, Stellar deployments further distribute holdings)

**EUTBL on Arbitrum:**
- Holders: 715 (per Arbiscan)
- Total supply: 205,150,111+ EUTBL
- No wash-trading patterns identified (all holders are KYC-verified allowlisted addresses — wash trading is effectively impossible in this structure)

**Insider wallet patterns:** Not applicable — KYC whitelist prevents anonymous pre-launch wallet farming. The token is not tradeable by non-whitelisted addresses.

### Oracle Risk

The NAV oracle (publishing daily fund value) is operated by an internal "oracle-operator" relayer. This is a centralized oracle. While Chainlink is used for CCIP cross-chain transfers, the **daily NAV price is published by Spiko's own relayer**, not a decentralized oracle network. Compromise of the oracle-operator key could allow mispriced minting or redemptions before detection.

### Transaction Pattern Analysis

No suspicious patterns identified:
- No circular transactions
- No MEV front-running opportunity (KYC whitelist prevents permissionless interaction)
- No treasury wallet movements to exchanges
- Redemptions flow through CACEIS to SEPA bank accounts

---

## 4. Red Flags Register

| # | Flag | Evidence | Severity |
|---|------|----------|----------|
| 1 | Multisig admin governance undisclosed | Tech blog confirms multisig controls upgrades; zero public detail on signers, threshold, timelock | HIGH |
| 2 | Critical bug in Stellar production contracts | Halborn Oct 2025: Critical finding in redemption logic; Stellar holds $337M TVL | HIGH |
| 3 | EVM audit staleness (Oct 2023 Trail of Bits, no confirmed follow-up) | New EVM features (CCIP, Morpho) added since; no public re-audit identified | HIGH |
| 4 | 96.5% LLTV on Morpho integration | Morpho docs; Spiko blog. Extreme tightness risks cascading liquidations for DeFi users borrowing against MMF shares | MEDIUM (DeFi layer users) |
| 5 | Fund manager is a third party (Twenty-First Capital) | Prospectus, Sicavonline; Spiko is technology provider, not portfolio manager | MEDIUM |
| 6 | Centralized NAV oracle | Tech blog; oracle-operator is an internal Spiko relayer, not decentralized | MEDIUM |
| 7 | Rapid multi-chain expansion (7 chains in <2 years) | DeFiLlama TVL breakdown; each new chain = new contract deployment = new attack surface | MEDIUM |
| 8 | Rate compression risk | Finary community; ECB/Fed rate cuts erode the product's yield differential vs. alternatives | LOW |
| 9 | Stellar uses Soroban (immature, since 2024) | Tech blog; Soroban deployed 2024 — less battle-tested than EVM | LOW |
| 10 | No confirmed Morpho-specific audit for EUTBL/USTBL markets | No results found; the oracle configuration for the Morpho market was not independently audited per available public data | LOW |
| 11 | Only 24 USTBL holders on Ethereum mainnet | Etherscan; mitigated by cross-chain bridging (715 on Arbitrum) | LOW |
| 12 | Chainlink CCIP dependency | CCIP outage = cross-chain transfers halt; centralization in Chainlink's infrastructure | LOW |

---

## 5. Counterparty Chain Analysis

The full chain of trust for a Spiko MMF holder is:

```
User (KYC'd wallet)
  → Spiko Technology Layer (EVM/Stellar/etc. contracts)
    → Twenty-First Capital (AMF-licensed portfolio manager, GP-11000029)
      → CACEIS Bank (depositary/custodian, Crédit Agricole subsidiary)
        → Treasury Bills (US/EU sovereign)
          → US Treasury / Eurozone Governments
```

**Additional DeFi composability layer:**
```
Spiko MMF shares (EUTBL/USTBL)
  → Morpho Protocol (lending/borrowing)
    → EURCV / USDCV (SG Forge MiCA-compliant stablecoins)
      → MEV Capital (vault curator)
```

**Failure points:**
- **Twenty-First Capital failure:** Fund manager is not Spiko. If 21FC loses AMF license or becomes insolvent, fund management transfers. UCITS law mandates custodian segregation of assets, so assets are protected from 21FC insolvency by CACEIS holding them separately. Transition could create temporary operational disruption.
- **CACEIS failure:** Highly unlikely (€5.3T AUC under Crédit Agricole), but not zero. EU bail-in rules and deposit insurance frameworks apply. T-Bills in custody are segregated from CACEIS's balance sheet — theoretically recoverable.
- **Spiko technology failure:** If Spiko goes bankrupt, the on-chain contracts continue. However, minting/redemption requires Spiko's operational relayer (daily-operator). Redemption could be disrupted operationally while remaining legally valid.
- **Chainlink CCIP failure:** Cross-chain transfers halt. Single-chain operations continue.
- **Morpho exploitation:** Does not affect MMF holders who are not using the Morpho lending layer. Isolated risk.

---

## 6. Comparative Analysis

### RWA Competitor Comparison

| Provider | Custodian | Auditor | Regulatory | TVL | Key Risk |
|----------|-----------|---------|------------|-----|----------|
| Spiko EUTBL/USTBL | CACEIS (Crédit Agricole) | Trail of Bits + Halborn | AMF UCITS | $1.02B | Admin multisig opacity |
| BlackRock BUIDL | BNY Mellon | Multiple | SEC | $2.4B | Restricted to large institutions |
| Franklin Templeton BENJI | BoNY Mellon | Franklin (TradFi) | SEC/FINRA | $2.0B+ | US-only |
| Ondo USDY | Various | Multiple | — | $0.5B+ | Less regulated |

Spiko's structure is closer to BlackRock BUIDL than to permissionless DeFi. The risk profile is fundamentally different from, e.g., algorithmic stablecoins or yield farming protocols.

### Known Rug Pull Pattern Comparison

Comparing Spiko against known red flags of major DeFi failures:

| Pattern | Wonderland/TIME | Celsius | Terra/Luna | Spiko |
|---------|----------------|---------|------------|-------|
| Anonymous team | Yes (0xSifu) | Partially | No | No — fully identified |
| Unsustainable yield | Yes (3300% APY) | Yes | Yes (anchor 20%) | No (market rate T-bills) |
| No real collateral | Yes | Commingled | Algorithmic | No — sovereign T-bills |
| No audit | Partially | No | Partially | Two audits (partial gaps) |
| Regulatory status | None | None | None | AMF UCITS regulated |
| TVL = real liquidity | Questionable | No | Inflated | Yes — UCITS-regulated |

**Spiko does not match the pattern of any known major DeFi fraud.** Its structural protections (AMF, UCITS, CACEIS custodian, PwC audit, T-bill collateral) make a sudden rug pull essentially impossible under the current legal framework. The real risks are operational and technical, not fraudulent.

---

## 7. Business Model Sustainability

**Revenue:** 0.25% annual management fee on AUM.
**Current annualized fees (DeFiLlama):** ~$988K
**Current TVL:** ~$1.024B → implied fee at full rate: $2.56M/year

**Gap:** The fee income ($988K annualized per DeFiLlama) is ~38% of what full-rate fees on $1B AUM would imply. This could reflect: (a) some AUM received preferential rates for early adoption, (b) fee accrual methodology differences, or (c) a portion of AUM under negotiated institutional rates.

**Sustainability concern:** With $22M Series A, a 9-person team (as of Series A announcement), and ~$1-2.5M in annual fee revenue, Spiko is operating on a growth-stage funding model. They need continued AUM growth to reach profitability. Rate compression (ECB/Fed cuts) directly reduces yield attractiveness and could slow AUM inflows or trigger redemptions.

**Yield compression risk:** As the ECB has been cutting rates, the attractive yield differential that drove Spiko's growth (European businesses earning ~0% on idle cash vs. Spiko's T-bill rate) narrows. This is a business model risk, not a fraud risk.

---

## 8. Unresolved Questions

1. **Multisig configuration:** Who are the signers on the super-admin multisig? What is the threshold? Is there a timelock? This cannot be determined without on-chain contract inspection of the deployed multisig address, which was not provided in any public documentation.

2. **Specific Trail of Bits findings:** The October 2023 report findings are not publicly described anywhere. Without reading the PDF directly, the number, severity, and resolution status of findings are unverified.

3. **Post-2023 EVM audit status:** Was there a follow-up EVM audit after CCIP integration, Morpho integration, or Base/Starknet/Etherlink deployments? No public evidence found. Direct question to Spiko team recommended.

4. **Twenty-First Capital background:** The actual portfolio manager (Twenty-First Capital, AMF no. GP-110000029) was not independently researched in depth. Their track record, team composition, and financial health are relevant second-order risks.

5. **Oracle resilience:** The daily-operator/oracle-operator's key management infrastructure is not described. How is it secured? Who has access? What is the recovery procedure?

6. **Morpho market oracle risk:** The oracle used for Spiko's MMF shares in Morpho markets is not independently identified. If it's the same internal relayer oracle, an oracle-operator compromise would affect Morpho market pricing.

7. **Etherlink and Starknet deployments:** These are the newest chains with minimal public information. No audit evidence for Starknet or Etherlink contracts was found.

---

## Final Verdict

**Overall Risk Level: LOW-TO-MODERATE (for regulated MMF product) / ELEVATED (for DeFi-integrated use cases)**

Spiko's core product — AMF-regulated UCITS money market funds tokenized on blockchain — is among the best-structured RWA products in the European market. The founders are genuine, the regulatory approval is real, the custodian is institutional-grade, and there are no fraud signals anywhere in the research.

The risks that exist are:

1. **Smart contract governance opacity** (multisig not disclosed) — a transparency failure that a serious DeFi user should demand clarity on before significant capital deployment.

2. **Audit coverage gaps** — the EVM audit is 2+ years old, a critical bug was found on Stellar post-deployment, and newer chain deployments (Starknet, Etherlink) have no confirmed audit coverage.

3. **Business model fragility to rate cycles** — purely a function of central bank policy.

4. **DeFi composability layer risks** — users borrowing on Morpho against Spiko shares face 96.5% LLTV liquidation risk that is entirely separate from the regulated MMF structure.

**Recommended due diligence steps before material capital deployment:**
1. Request Spiko to publicly disclose multisig configuration (signers, threshold, timelock)
2. Verify existence of a post-2023 EVM audit covering CCIP and Morpho integrations
3. Confirm Halborn follow-up audit was conducted per their recommendation
4. Read the Trail of Bits October 2023 PDF directly to verify finding severity and resolution
5. Confirm Twenty-First Capital's financial health and regulatory standing independently

---

*Report generated using adversarial DeFi research framework. All on-chain addresses should be independently verified. This is not financial advice.*
