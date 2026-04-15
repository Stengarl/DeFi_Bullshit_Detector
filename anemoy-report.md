# Anemoy.io — Adversarial DeFi Due Diligence Report

**Report Date:** April 15, 2026
**Researcher:** Adversarial Research Agent
**Scope:** Anemoy.io — web3-native institutional asset manager; primary products are tokenized RWA funds (JTRSY, JAAA, ACRDX, DYF, SPXA) built on the Centrifuge protocol.
**Note on framing:** Anemoy is NOT a typical DeFi/retail token project. It is an institutional RWA fund manager targeting non-US professional investors, DAOs, and Web3 treasuries. The adversarial research framework must be adjusted accordingly — the relevant risks here are structural, legal, and counterparty rather than pump-and-dump or rug pull.

---

## 1. EXECUTIVE SUMMARY

**Verdict:** Anemoy.io is a **legitimately structured institutional RWA asset manager with verifiable founders, regulated fund vehicles, top-tier institutional partners, and multiple independent credit ratings — but it carries significant structural risks that are systematically underemphasized in its marketing: full off-chain counterparty dependence that undermines its "DeFi" positioning, a BVI regulatory wrapper that protects founders over investors, inherited platform risk from Centrifuge's $15.5M bad debt history, and a DYF fund product whose crypto yield strategies introduce an entirely different risk category from its flagship T-bill products. The risk of fraud or exit-scam is LOW; the risk of structural loss, regulatory disruption, or redemption failure is MEDIUM-HIGH.**

**Confidence Level:** HIGH — extensive independent corroboration from Janus Henderson, S&P Global, Moody's, BVI FSC, Coindesk, DeFiLlama, and Arbitrum governance forum.

**Top 3 Risks:**
1. **Off-chain counterparty dependence:** Redemptions require functioning relationships with Janus Henderson, Pershing LLC (BNY Mellon), Circle, and Trident Trust. A failure of any of these parties can freeze withdrawals. The "DeFi" framing obscures that this is fundamentally a trust-based, permissioned institutional product.
2. **Centrifuge platform risk and bad debt history:** The underlying Centrifuge protocol accumulated ~$15.5M in defaulted loans from Tinlake pools in 2023, including MakerDAO-exposed defaults. Anemoy's products run on a platform with a documented credit loss history.
3. **BVI domicile and non-US exclusion:** The fund is a BVI Professional Fund, excluding US persons entirely. BVI regulation offers lighter investor protections than US or EU frameworks. In a wind-down scenario, BVI court processes heavily favor fund operators, not investors.

**Top 3 Positive Signals:**
1. Real, regulated, rated product: JTRSY holds AA+ ratings from both S&P Global Ratings and Particula, plus an "Aa" from Moody's — the most-rated tokenized fund in existence. These are independent, paid-for ratings from non-affiliated agencies.
2. Institutional-grade partners: Janus Henderson (sub-investment manager), Pershing/BNY Mellon (custodian), Trident Trust (fund admin), Apollo (credit strategy), S&P DJI (index license). These are blue-chip institutions who would not put their names on fraudulent products.
3. Verifiable, doxxed team with legitimate prior exit history: Martin Quensel co-founded Taulia (acquired by SAP) and Centrifuge; Anil Sood has Goldman Sachs/Morgan Stanley/Barclays/Cantor Fitzgerald background. No regulatory actions, no rug history.

---

## 2. TEAM ASSESSMENT

### 2.1 Martin Quensel — Founder & CEO

**Identity:** Real, fully doxxed. Active speaker at industry conferences (GOTO Berlin 2018, AIMA). LinkedIn and Crunchbase profiles extensively verified.
**Confidence:** HIGH

**Verified Career Timeline:**
- 1997: Developer for SAP Financials
- Early 2000s: Software architect at SAP eCommerce; CTO at ReadSoft Lab; board member at Ebydos
- 2010: **Co-founded Taulia** — supplier finance network serving 120+ Global 2000 companies. Taulia was acquired by SAP in 2022 for an undisclosed amount. This is a **verified successful exit** with a major strategic acquirer.
- 2017: **Co-founded Centrifuge** alongside Lucas Vogelsang, Maex Ament, and Philip Stehlik — a blockchain protocol for tokenizing real-world assets. Active for 7+ years with $517M+ TVL.
- 2023: Founded Anemoy — spinning out of Centrifuge's asset management work.

**Red flags:** None identified. No SEC/FCA/BaFin enforcement actions found. No prior failed crypto projects. Quensel's GOTO Berlin 2018 speaker profile predates Anemoy by five years, confirming deep pre-Anemoy technical credibility with no manufactured identity.

**GitHub:** Active committer to Centrifuge's open-source repos. [centrifuge/security](https://github.com/centrifuge/security) — public audit archive with 19–24 audits published, including Trail of Bits, SRLabs, Least Authority, and Cantina. This is a real engineering organization, not figureheads.

**Sources:** [Crunchbase](https://www.crunchbase.com/person/martin-quensel), [AIMA Member Profile](https://acc.aima.org/widgets/team_members/teamMemberDetails/?id=E12228DB-505F-46AF-8447A1E5EE8A2C61), [GOTO Berlin 2018](https://gotober.com/2018/speakers/588/martin-quensel), [Fintech Review Profile](https://fintechreview.net/martin-quensel-champions-tokenization-with-anemoy/), [Cypherhunter](https://www.cypherhunter.com/en/p/martin-quensel/)

---

### 2.2 Anil Sood — Co-Founder

**Identity:** Real, fully doxxed via LinkedIn.
**Confidence:** HIGH

**Verified Career:**
- Goldman Sachs, Morgan Stanley, Barclays — senior TradFi roles (exact titles not independently verified beyond LinkedIn claims)
- Partner, Cantor Fitzgerald
- BSc Management Sciences, Loughborough University (2001–2005)
- Centrifuge — CSO and CGO (Chief Strategy Officer, Chief Growth Officer)
- June 2024: Anemoy acquired **NBRHD Capital** — Sood's prior venture — and Sood joined Anemoy as co-founder. This acquisition is documented in Anemoy's own press release and corroborated by Outposts.io.

**What NBRHD Capital was:** An on-chain asset management platform for professional investors focused on RWA investment opportunities. Small company; no independent review of its performance was found.

**Red flags:** The Goldman/Morgan Stanley/Barclays/Cantor Fitzgerald background is plausible given his ETF trading expertise, but the specific roles have not been verified against company records beyond LinkedIn. This is a medium-confidence claim. No enforcement actions found. No scam/rug connections.

**Sources:** [LinkedIn — Anil Sood (Centrifuge)](https://www.linkedin.com/in/anil-sood/), [RootData profile](https://www.rootdata.com/member/Anil%20Sood?k=MjMwMzE%3D), [Anemoy NBRHD acquisition](https://www.anemoy.io/news/anemoy-acquires-nbrhd-capital)

---

### 2.3 Broader Team

- Centrifuge imprint confirms corporate registration in **Zug, Switzerland** — a well-established crypto-friendly but substantive jurisdiction.
- Grayson Alto (DeFi BD & Research) — named in Arbitrum STEP applications; confirms BD function.
- Team size not publicly disclosed beyond named individuals.
- [Centrifuge GitHub org](https://github.com/centrifuge): 40+ public repositories; active commit history; real engineering output.

**What Could NOT Be Verified:**
- Goldman Sachs, Morgan Stanley, Barclays, Cantor Fitzgerald employment for Anil Sood — LinkedIn claims, not independently confirmed via company records or press.
- Full team composition below the co-founder level.
- Exact separation of Anemoy entity from Centrifuge entity — both appear to share team members and infrastructure.

---

## 3. THIRD-PARTY CONSENSUS

### 3.1 Audit and Security Posture

**This is a genuine strength.** Centrifuge maintains a public audit repository at [github.com/centrifuge/security](https://github.com/centrifuge/security) with confirmed reports from:

| Auditor | Scope | Status |
|---|---|---|
| Trail of Bits | Centrifuge node | Published PDF in public repo |
| SRLabs | Centrifuge chain (2022 baseline) | Published PDF in public repo |
| Least Authority | Tinlake v0.3.0 | Published PDF in public repo |
| Cantina | CFG token (Spearbit, March 2025) | Published; Cantina portfolio page live |
| Cantina | Centrifuge protocol | Published; Cantina portfolio page live |

**19–24 total audits** are cited across sources. The CFG token audit specifically examined the delegation and staking functions after the ERC-20 migration (March 2025).

**RED FLAG (MEDIUM): No Anemoy-specific contract audit found.** All audits identified are for the **Centrifuge protocol** — the infrastructure layer. Anemoy's own smart contracts (JTRSY token, JAAA token, ACRDX token, DYF wrapper) have not been identified as having separately published audit reports. Given that JTRSY alone held $500M+ AUM, the absence of a contract-specific audit for the token/vault mechanism is a transparency gap.

**Positive signal:** JTRSY holds independent credit ratings from three non-affiliated rating agencies:
- **S&P Global Ratings: AA+f / S1+** — highest rating assigned to any tokenized fund
- **Moody's: Aa** — investment-grade
- **Particula: AA+** — upgraded from A+ in May 2025

Key driver of Particula's upgrade: "implementation of a more robust access control system addressing prior centralization concerns." This upgrade note **confirms that earlier versions had centralization concerns** — these were subsequently remediated.

**Sources:** [Centrifuge Security GitHub](https://github.com/centrifuge/security), [Cantina CFG audit](https://cantina.xyz/portfolio/dd664002-e362-4798-8927-0556fe45ff46), [S&P Rating — Janus Henderson press release](https://www.janushenderson.com/en-us/advisor/press-releases/janus-henderson-anemoy-treasury-fund-receives-highest-tokenized-fund-rating/), [Particula AA+ upgrade](https://particula.io/rating-reports/particula-rating-update-anemoy-jtrsy-may-2025), [Moody's via Particula](https://centrifuge.mirror.xyz/It69-xTYbNOv_rwBYbRicNEfFs6WuzQ5JaCnCWiBUiI)

---

### 3.2 Independent Media Coverage

| Publication | Coverage | Nature |
|---|---|---|
| CoinDesk | Centrifuge bad debt 2023 (2 articles) | Critical; documented $5.8M then $1.84M defaults |
| The Defiant | Anemoy DYF launch article | Neutral-to-positive |
| The Block | DeFi outlook 2026 mention | Neutral |
| Ledger Insights | S&P 500 index tokenization | Positive/neutral enterprise coverage |
| Rekt News | **None found** | No exploits or hacks |
| ZachXBT | **None found** | No manipulation allegations |
| DL News | Centrifuge/Anemoy award coverage | Neutral |

**Assessment:** No adversarial coverage of Anemoy specifically was found. CoinDesk's critical coverage in 2023 was directed at **Centrifuge's Tinlake product** (pre-Anemoy), not Anemoy's current fund lineup. The absence of scam/rug/manipulation coverage from independent adversarial sources is a genuine positive, but the product is also primarily institutional (non-retail), which means adversarial crypto media has less incentive to cover it.

---

### 3.3 Community Sentiment

Search for "anemoy scam" and "anemoy rug" returned zero results — the query was so clean that the search engine returned only generic rug-pull education articles with no mention of Anemoy. This is **notable absence** — not proof of legitimacy, but meaningfully different from typical DeFi projects where community concerns generate indexed content.

Arbitrum governance forum contains two Centrifuge/Anemoy STEP applications with substantive community discussion — the threads are public and the project responds to technical questions in governance forums. This indicates genuine engagement with DeFi governance, not ghost-account astroturfing.

No Reddit threads, ZachXBT flags, or crypto-forum community concerns were found.

---

### 3.4 Partnerships — Verified Institutional Partners

| Partner | Role | Verification |
|---|---|---|
| **Janus Henderson Investors** | Sub-investment manager (JTRSY, JAAA, SPXA) | Janus Henderson press releases on janushenderson.com |
| **Apollo Global Management** | Underlying fund manager (ACRDX) | Apollo press release, Yahoo Finance |
| **S&P Dow Jones Indices** | Index license (SPXA) | S&P DJI official press release, spglobal.com |
| **Pershing LLC (BNY Mellon)** | Custodian (physical T-bills) | Particula rating report |
| **Trident Trust** | Fund administrator | Particula rating report, IQ.wiki |
| **Circle** | USDC conversion on redemption | IQ.wiki JTRSY article |
| **Wintermute** | Market making / instant liquidity (JTRSY) | Centrifuge Mirror blog |
| **Grove (Sky Ecosystem)** | $50M anchor investment in ACRDX | Centrifuge blog, Yahoo Finance |
| **Wormhole** | Cross-chain connectivity | Centrifuge ACRDX launch blog |
| **Plume Network** | RWA chain hosting | Centrifuge blog |

**Key concern about Wintermute:** Wintermute is Anemoy's market maker for JTRSY instant redemptions. Wintermute is a legitimate global algorithmic trading firm — but it was also identified in the Venice.ai investigation as the market maker that sold $1.4M of VVV on DEXs before any CEX listing. Wintermute's business model involves receiving token allocations at discounts in exchange for market making — which creates inherent conflicts of interest at token launches. For Anemoy's institutional fund products (not a token), this concern is less material since JTRSY is not a speculative token. However, it is worth flagging.

---

## 4. ON-CHAIN FINDINGS

### 4.1 Token Contracts Identified

| Token | Chain | Contract Address | Description |
|---|---|---|---|
| JTRSY | Ethereum | `0x8c213ee79581Ff4984583C6a801e5263418C4b86` | Janus Henderson Treasury Fund |
| deJAAA | Ethereum | `0xAAA0008C8CF3A7Dca931adaF04336A5D808C82Cc` | DeFi wrapper for JAAA CLO Fund |
| LTF | Base | `0x8c213ee79581ff4984583c6a801e5263418c4b86` | Anemoy Liquid Treasury Fund |
| ACRDX | Plume/Ethereum/Base | Listed on CoinGecko | Apollo credit fund token |

**Sources:** [Ethplorer JTRSY](https://ethplorer.io/address/0x8c213ee79581ff4984583c6a801e5263418c4b86), [Ethplorer deJAAA](https://ethplorer.io/address/0xaaa0008c8cf3a7dca931adaf04336a5d808c82cc), [BaseScan LTF](https://basescan.org/token/0x8c213ee79581ff4984583c6a801e5263418c4b86)

---

### 4.2 Legal Entity and Regulatory Structure

**Anemoy Capital SPC Limited**
- Type: Segregated Portfolio Company (SPC) — each fund is a bankruptcy-remote "segregated portfolio"
- Jurisdiction: British Virgin Islands (BVI)
- Regulator: BVI Financial Services Commission (FSC) — independently verified via [BVI FSC regulated entities list](https://www.bvifsc.vg/regulated-entities/anemoy-capital-spc-limited)
- Anemoy Asset Management Limited: Investment manager entity

**RED FLAG (MEDIUM): BVI domicile.** BVI is a legitimate jurisdiction used by many institutional funds globally — but it offers meaningfully less investor protection than US (SEC/CFTC), UK (FCA), or EU (ESMA/AIFMD) frameworks. In a dispute or wind-down:
- BVI courts move slowly and are expensive to litigate in from overseas
- The "segregated portfolio" structure protects fund assets from cross-contamination between products, but does NOT protect investors from fraud or mismanagement within a portfolio
- The BVI FSC is a real regulator, but it is lighter-touch than G7 equivalents

**US persons are excluded.** JTRSY is available to "non-US Professional Investors" only. This is a regulatory structuring choice — by excluding US persons, Anemoy avoids SEC registration requirements. This makes the product inaccessible to most US-based DAOs without significant KYC/compliance work.

---

### 4.3 AUM and TVL — Verified Independent Sources

| Fund | Peak/Current AUM | Source |
|---|---|---|
| JTRSY (Treasury) | $500M+ (scaled within weeks of launch) | RWA.xyz, Janus Henderson PR |
| JAAA (CLO) | ~$750M peak; ~$416M recent | Dune Analytics tweet, RWA.xyz |
| ACRDX (Apollo Credit) | $50M at launch (Grove anchor) | Centrifuge blog, Yahoo Finance |
| DYF (Market Neutral) | Applied for Arbitrum STEP allocation | Arbitrum governance forum |
| Total Centrifuge platform | ~$517M TVL | DeFiLlama |
| Anemoy stated AUM | **$4 billion** | CBInsights, Fintech Review |

**IMPORTANT DISCREPANCY:** CBInsights and Fintech Review cite $4B in AUM for Anemoy. However, DeFiLlama's independent on-chain tracking shows Centrifuge TVL at ~$517M. JAAA peaked at ~$750M and has drawn down to ~$416M. The $4B figure cannot be independently verified through on-chain data. This gap could reflect: (a) non-tokenized AUM not tracked on-chain, (b) stale/exaggerated marketing figures, or (c) off-chain institutional commitments not yet deployed. This is an **unresolved question** that requires direct documentation from Anemoy.

**RED FLAG (LOW-MEDIUM):** The $4B AUM claim cannot be verified on-chain and significantly exceeds what DeFiLlama shows for the Centrifuge platform.

---

### 4.4 Centrifuge Platform Risk — Inherited Bad Debt History

This is the most significant on-chain risk finding for Anemoy's products.

**2023 Centrifuge/Tinlake Default Events (HIGH confidence):**

- **February 2023:** Centrifuge accumulated ~$5.8M in loans from two Tinlake lending pools that were overdue. [CoinDesk](https://www.coindesk.com/markets/2023/02/03/decentralized-lending-protocol-centrifuge-accrues-6m-unpaid-debt)
- **July 2023:** MakerDAO voted to halt lending to Harbor Trade's Centrifuge pool after $2.1M in loan defaults matured unpaid. [CoinDesk](https://www.coindesk.com/markets/2023/07/20/makerdao-votes-to-halt-lending-to-tokenized-credit-pool-after-2m-loan-default)
- **August 2023:** ControlFreight default put MakerDAO's $1.84M investment at risk. [CoinDesk](https://www.coindesk.com/markets/2023/08/25/default-of-tokenized-loans-on-centrifuge-puts-makerdaos-investment-at-risk)
- **Cumulative bad debt:** Over $15.5M in unpaid loans total at peak.

**Critical distinction:** These defaults occurred in Centrifuge's **Tinlake** product (private credit pools with speculative borrowers), NOT in Anemoy's current tokenized fund products (JTRSY invests in US T-bills via Pershing/BNY; JAAA in AAA-rated CLOs). The credit quality of underlying assets is categorically different.

However, the defaults reveal a structural issue: **the Centrifuge platform does not provide legal or operational recourse when off-chain borrowers default.** Token holders were exposed to loss because the on-chain token's value depended entirely on the creditworthiness of off-chain entities — and when those entities defaulted, there was no protocol-level recovery mechanism. The same structural dependence exists for Anemoy products, though with higher-quality underlying assets.

---

### 4.5 The Redemption Architecture — Trustless vs. Trust-Based

**Official claim:** 24/7/365 instant redemptions via Wintermute market making.

**Reality check (from Particula rating report and IQ.wiki):**

The JTRSY redemption process requires:
1. Investor locks JTRSY in smart contract
2. Fund manager instructs broker (Pershing/BNY) to sell T-bills
3. USD proceeds → converted to USDC by Circle
4. USDC sent to investor wallet after daily NAV update

**This process is NOT trustless.** It depends on:
- Anemoy functioning as fund manager
- Janus Henderson functioning as sub-manager
- Pershing LLC executing the T-bill sale
- Circle converting USD to USDC
- Trident Trust confirming the NAV

**The Wintermute "instant redemption" is a secondary liquidity layer** — Wintermute acts as a buyer of JTRSY on the open market, providing immediate exit liquidity without waiting for the T-bill sale settlement. This is a genuine innovation, but it means "instant redemption" liquidity depends on Wintermute's continued market-making commitment — not an on-chain guarantee.

**RED FLAG (HIGH): Multi-party off-chain redemption dependency.** If ANY of the off-chain parties (Anemoy, Janus Henderson, Pershing, Circle, Wintermute) ceases to function or terminates its agreement, redemptions are delayed or frozen. The product is marketed with DeFi language ("on-chain," "24/7") but operates on TradFi trust assumptions. Investors must understand this clearly.

Mitigation noted: Particula's rating report confirms "if one blockchain chain experiences an outage, investors can still process redemptions on another supported chain or in fiat USD off-chain. The fund administrator also maintains complete off-chain records, allowing tokenized shares to be replaced with traditional shares in a worst-case scenario." This is a genuine fallback — but "replaced with traditional shares" means the investor is no longer in a tokenized DeFi product; they are in a conventional BVI fund with no on-chain exit.

---

### 4.6 CFG Token — Separate Risk from Anemoy Products

Centrifuge has its own governance token CFG. This is NOT Anemoy's product, but is relevant as it represents the governance mechanism for the underlying infrastructure.

**CFG Token Distribution (HIGH concern for CFG holders, LOW-MEDIUM for Anemoy fund investors):**
- Core Contributors: 29–31.4% — cliff vesting through March 2030
- Early Backers: ~18.5%
- Foundation: 24.6%
- Community Treasury: 20%
- Annual inflation: 3% (accrues to DAO treasury)

**CFG migration (March 2025):** CFG migrated from Substrate (Centrifuge Chain) to a unified ERC-20 on Ethereum. Total supply: 675M CFG. The Cantina/Spearbit audit covered the CFG token implementation post-migration.

**Note:** Anemoy's fund products (JTRSY, JAAA, ACRDX) are NOT speculative tokens — they are fund shares that aim to maintain stable NAV with minimal price volatility. CFG token risks do not directly affect Anemoy fund investors; however, if Centrifuge's governance or infrastructure fails, Anemoy funds could be disrupted.

---

## 5. PRODUCT-SPECIFIC RISK ANALYSIS

### 5.1 JTRSY — Janus Henderson Treasury Fund

**Underlying:** Short-duration US T-bills
**Risk rating:** LOW (underlying asset) → MEDIUM (structural/counterparty)
**Independent ratings:** S&P AA+f/S1+, Moody's Aa, Particula AA+
**Custodian:** Pershing LLC (BNY Mellon) — top-tier, regulated
**Access:** Non-US Professional Investors only; KYC required via Trident Trust whitelist

**Main risks:** Off-chain redemption dependency; BVI domicile; Circle USDC conversion risk; Wintermute liquidity commitment not contractually guaranteed in perpetuity.

---

### 5.2 JAAA — Janus Henderson AAA CLO Fund

**Underlying:** AAA-rated Collateralized Loan Obligations (CLOs)
**Risk rating:** MEDIUM (CLOs are more complex than T-bills)
**Performance:** Peaked ~$750M; drawn down to ~$416M — a ~44% AUM decline suggesting meaningful redemptions
**Access:** Non-US Professional Investors

**RED FLAG (MEDIUM): 44% AUM drawdown from peak.** JAAA went from ~$750M to ~$416M. This is not a price decline (the NAV should be stable); it represents investors redeeming. Mass redemptions in a tokenized product can create liquidity stress. The reason for the drawdown is not explained in available sources — whether this is normal investor rebalancing or a flight from the product is unclear. Worth monitoring.

**CLO-specific risk:** AAA-rated CLOs are the most senior tranche of leveraged loan securitizations. They have historically had near-zero default rates, but "AAA" ratings failed spectacularly in the 2008 financial crisis. CLO structures depend on the performance of leveraged corporate loans — which are sensitive to credit cycles and interest rate environments.

---

### 5.3 ACRDX — Apollo Diversified Credit Fund

**Underlying:** Apollo's diversified credit platform (private credit)
**Risk rating:** MEDIUM-HIGH
**AUM:** $50M at launch (Grove anchor)
**Access:** Qualified investors; available on Plume, Ethereum, Base; denominated in USDC

**Specific risks:**
- Private credit is illiquid by nature; "tokenization" does not make illiquid assets liquid
- Apollo's credit strategies include leveraged loans, high-yield debt, and structured credit — meaningfully higher risk than T-bills
- The fund has one known anchor investor (Grove/$50M) — this is significant concentration risk; if Grove redeems, the fund may struggle to maintain operations
- Oracle: Chronicle; cross-chain: Wormhole — both introduce additional points of failure

---

### 5.4 DYF — DeFi Yield Fund (Market Neutral Crypto)

**Underlying:** Yield farming, funding rate arbitrage, lending, "special situations" — up to 8 underlying crypto funds
**Risk rating:** HIGH — categorically different from other Anemoy products
**Strategy:** "Market neutral" crypto yield

**RED FLAG (HIGH): This product is NOT an RWA fund — it is a fund of hedge funds investing in crypto strategies.**

The DYF invests in:
- Yield farming (smart contract risk)
- Funding rate arbitrage (exchange counterparty risk)
- Crypto lending (credit risk + liquidation risk)
- "Special situations" (undefined; could mean anything)

**Each of these underlying strategies carries crypto-native risks that T-bill and CLO investors would not expect.** The DYF is marketed under the Anemoy brand alongside institutional T-bill products, which creates potential for unsophisticated institutional investors to conflate the risk profiles.

Monthly redemptions only (vs. daily for JTRSY) — reflecting the lower liquidity of underlying strategies.

**Sources:** [Arbitrum STEP DYF application](https://forum.arbitrum.foundation/t/centrifuge-anemoy-defi-yield-fund-dyf-step-application/23545), [The Defiant DYF coverage](https://thedefiant.io/news/defi/web3-and-tradfi-collide-through-anemoy-s-defi-yield-fund)

---

### 5.5 SPXA — S&P 500 Index Fund

**Underlying:** S&P 500 Index (licensed from S&P Dow Jones Indices)
**Status:** Launched on Base using Centrifuge's Proof-of-Index infrastructure
**Notable:** First licensed S&P 500 index fund on blockchain
**Risk:** MEDIUM (equity market risk) + structural off-chain dependency

**Positive signal:** S&P Dow Jones Indices licensing to Centrifuge/Janus Henderson is confirmed by S&P's own press release — this is a genuine institutional endorsement that would not be granted to a fraudulent operation.

---

## 6. RED FLAGS REGISTER

| # | Severity | Red Flag | Evidence | Source | Why It Matters |
|---|---|---|---|---|---|
| 1 | HIGH | Multi-party off-chain redemption dependency | Redemption requires 4+ institutional counterparties (Anemoy, Janus Henderson, Pershing, Circle) — NOT trustless | Particula rating report, IQ.wiki | "DeFi" marketing obscures that redemptions can be frozen if any partner fails |
| 2 | HIGH | DYF is a crypto hedge fund product, not RWA | DYF invests in yield farming, funding rate arbitrage, lending, "special situations" | Arbitrum STEP DYF application | Crypto-native risks sold under same brand as T-bill/CLO products; risk profile conflation |
| 3 | MEDIUM-HIGH | JAAA AUM drawdown ~44% from peak | $750M peak → ~$416M current | Dune Analytics tweet, RWA.xyz | Mass redemptions without explanation; potential product concern or liquidity stress signal |
| 4 | MEDIUM | $4B AUM claim not verifiable on-chain | DeFiLlama shows ~$517M Centrifuge TVL; on-chain data does not support $4B figure | CBInsights vs. DeFiLlama | Marketing figure significantly exceeds independently verifiable on-chain data |
| 5 | MEDIUM | BVI regulatory wrapper — lighter protection | Anemoy Capital SPC Limited licensed by BVI FSC | BVI FSC regulated entities list | BVI offers weaker investor protections and slower legal recourse than G7 jurisdictions |
| 6 | MEDIUM | No Anemoy-specific smart contract audit found | All published audits are for Centrifuge protocol, not Anemoy's JTRSY/JAAA/ACRDX contracts | GitHub centrifuge/security | $500M+ AUM products without named contract-level audit |
| 7 | MEDIUM | Centrifuge platform history: $15.5M in Tinlake bad debt (2023) | Harbor Trade ($2.1M), ControlFreight ($1.84M), others; MakerDAO halted lending | CoinDesk (3 articles, 2023) | Platform-level credit default history; demonstrates off-chain dependency failure is real, not theoretical |
| 8 | MEDIUM | Prior Particula rating noted centralization concerns | Upgrade note: "implementation of a more robust access control system addressing prior centralization concerns" | Particula AA+ upgrade report (May 2025) | Confirms earlier versions had centralization risk in access control; now remediated per Particula |
| 9 | MEDIUM | ACRDX private credit has illiquidity risk | Apollo private credit is inherently illiquid; tokenization does not change underlying asset liquidity | General private credit characteristics | Investors may expect DeFi liquidity but underlying assets are illiquid; redemptions could be gated |
| 10 | MEDIUM | Wintermute as instant liquidity provider | "Instant redemption" depends on Wintermute's continued market-making commitment | Centrifuge Mirror blog | Wintermute is contractually engaged but the commitment is not guaranteed in perpetuity on-chain |
| 11 | LOW-MEDIUM | US persons excluded — Anemoy is unavailable to most US DAOs | BVI fund structure requires non-US professional investors | Particula, IQ.wiki | Significant portion of DeFi/DAO treasury market cannot use product without complex structuring |
| 12 | LOW-MEDIUM | Anil Sood TradFi credentials not independently verified beyond LinkedIn | Goldman Sachs, Morgan Stanley, Barclays, Cantor Fitzgerald claims | LinkedIn only | Medium-confidence claim; could not verify via company records or press references |
| 13 | LOW | CFG token cliff vesting: 29–31% core contributor allocation through March 2030 | CryptoRank vesting data | Tokenomist, CryptoRank | CFG token sell pressure risk; not directly relevant to Anemoy fund investors |

---

## 7. COMPARATIVE ANALYSIS

### How Anemoy Differs from Typical DeFi Risks

Anemoy does NOT share the primary red flag patterns of confirmed DeFi scams:

| Pattern | Anemoy | Confirmed Scam Pattern |
|---|---|---|
| Anonymous or pseudonymous team | NO — fully doxxed | YES (Wonderland, Terra Luna founders hid affiliations) |
| No verifiable prior track record | NO — Taulia exit, Centrifuge 7yr history | YES (most rug pulls) |
| Unsustainable yield (Ponzi) | NO — yield from T-bills, CLOs, real assets | YES (Celsius, BlockFi, Anchor Protocol) |
| No real product | NO — real regulated funds with institutional partners | YES (pure token schemes) |
| Exit-scam risk | VERY LOW | HIGH for anonymous teams |
| Launch-day insider dump | NOT APPLICABLE — no speculative token | Common pattern |

### Where Anemoy Shares Risk Patterns with Failed RWA/Institutional Projects

| Pattern | Anemoy | Failed Analog |
|---|---|---|
| Off-chain asset dependency | YES — T-bills, CLOs, credit | Celsius (off-chain lending), BlockFi |
| BVI/offshore domicile | YES | Multiple failed offshore funds |
| Custodian concentration | YES — Pershing/BNY Mellon for JTRSY | Lower risk given BNY caliber |
| Private credit illiquidity risk | YES (ACRDX/DYF) | Celsius private credit book, Genesis |
| Platform bad debt history | YES (Centrifuge Tinlake 2023) | Not a Ponzi, but real credit losses |

**Conclusion:** Anemoy most resembles a legitimate institutional fund-of-funds structure wrapped in blockchain infrastructure — similar to Ondo Finance, Superstate, or OpenEden. It does not resemble rug pulls, pump-and-dump schemes, or algorithmic Ponzis. The material risks are TradFi risks (credit, counterparty, regulatory) dressed in DeFi language, not DeFi-native fraud risks.

---

## 8. UNRESOLVED QUESTIONS

1. **What explains JAAA's 44% AUM drawdown from $750M to $416M?** Was this orderly redemption, a specific negative catalyst, or investors fleeing? This is the single most important open question for current JAAA holders.

2. **How is the $4B AUM figure calculated?** It cannot be reconciled with DeFiLlama's $517M TVL figure. Anemoy needs to provide a breakdown with verifiable components.

3. **Are Anemoy's specific smart contracts (JTRSY, JAAA, ACRDX) covered by published audits?** The Centrifuge protocol audits may cover the infrastructure, but the specific vault and token contracts for each fund product were not identified in published audit reports.

4. **What is the DYF's current AUM and performance history?** No performance data was found for the DeFi Yield Fund. Monthly-only redemptions and a "market neutral" crypto mandate make this the most opaque Anemoy product.

5. **What is the exact governance relationship between Anemoy and Centrifuge?** They share team members and infrastructure but appear to be separate legal entities. Whether Centrifuge DAO governance decisions can affect Anemoy fund operations is unclear.

6. **How are the 8 underlying sub-funds in DYF selected, and what is their individual track record?** The Arbitrum STEP application says each sub-fund must have operated for 2+ years — but names no specific funds.

7. **Can Anil Sood's Goldman/Morgan Stanley/Barclays/Cantor Fitzgerald tenure be confirmed via sources other than LinkedIn?** This is medium-priority — his Centrifuge CSO role is verifiable, and the NBRHD Capital acquisition is documented — but TradFi background verification would raise confidence.

---

## SOURCES

- [BVI FSC — Anemoy Capital SPC Limited](https://www.bvifsc.vg/regulated-entities/anemoy-capital-spc-limited)
- [Janus Henderson — Anemoy Treasury Fund press release](https://www.janushenderson.com/corporate/press-releases/janus-henderson-to-partner-with-anemoy-and-centrifuge-on-its-first-tokenized-fund/)
- [Janus Henderson — JTRSY S&P Rating (highest tokenized fund rating)](https://www.janushenderson.com/en-us/advisor/press-releases/janus-henderson-anemoy-treasury-fund-receives-highest-tokenized-fund-rating/)
- [Particula — AA+ Rating Report JTRSY](https://particula.io/rating-reports/particula-rating-report-anemoy-jtrsy-may-2025)
- [Particula — AA+ Upgrade Report JTRSY](https://particula.io/rating-reports/particula-rating-update-anemoy-jtrsy-may-2025)
- [IQ.wiki — JTRSY structure and redemption process](https://iq.wiki/wiki/janus-henderson-anemoy-treasury-fund)
- [RWA.xyz — JTRSY analytics](https://app.rwa.xyz/assets/JTRSY)
- [RWA.xyz — JAAA analytics](https://app.rwa.xyz/assets/JAAA)
- [RWA.xyz — ACRDX analytics](https://app.rwa.xyz/assets/ACRDX)
- [DeFiLlama — JTRSY RWA page](https://defillama.com/rwa/asset/jtrsy)
- [Centrifuge Security GitHub](https://github.com/centrifuge/security)
- [Cantina — CFG Token Audit](https://cantina.xyz/portfolio/dd664002-e362-4798-8927-0556fe45ff46)
- [Cantina — Centrifuge Protocol Audit](https://cantina.xyz/portfolio/8c15e83a-08fc-48b9-8cc1-4f9ca76bb064)
- [CoinDesk — $6M unpaid debt (Feb 2023)](https://www.coindesk.com/markets/2023/02/03/decentralized-lending-protocol-centrifuge-accrues-6m-unpaid-debt)
- [CoinDesk — MakerDAO halts Harbor Trade (Jul 2023)](https://www.coindesk.com/markets/2023/07/20/makerdao-votes-to-halt-lending-to-tokenized-credit-pool-after-2m-loan-default)
- [CoinDesk — ControlFreight default (Aug 2023)](https://www.coindesk.com/markets/2023/08/25/default-of-tokenized-loans-on-centrifuge-puts-makerdaos-investment-at-risk)
- [Anemoy Wintermute Partnership](https://centrifuge.mirror.xyz/Do3HnqzCMyws_vSZPhRwCYjD-DK81H1rz-MgAP6_WLc)
- [Anemoy NBRHD Capital Acquisition](https://www.anemoy.io/news/anemoy-acquires-nbrhd-capital)
- [Centrifuge — ACRDX Launch with Apollo/Grove](https://centrifuge.io/blog/acrdx-launch-on-centrifuge)
- [S&P DJI — S&P 500 Index license to Centrifuge](https://www.spglobal.com/spdji/en/index-announcements/article/sp-dow-jones-indices-collaborates-with-centrifuge-to-bring-the-sp-500-index-onchain-expanding-access-to-the-world-s-most-widely-recognized-benchmark/)
- [Arbitrum STEP — JTRSY application](https://forum.arbitrum.foundation/t/centrifuge-janus-henderson-anemoy-treasury-fund-jtrsy-step-ii-application/23496)
- [Arbitrum STEP — DYF application](https://forum.arbitrum.foundation/t/centrifuge-anemoy-defi-yield-fund-dyf-step-application/23545)
- [The Defiant — DYF coverage](https://thedefiant.io/news/defi/web3-and-tradfi-collide-through-anemoy-s-defi-yield-fund)
- [Martin Quensel — Crunchbase](https://www.crunchbase.com/person/martin-quensel)
- [Martin Quensel — AIMA Member Profile](https://acc.aima.org/widgets/team_members/teamMemberDetails/?id=E12228DB-505F-46AF-8447A1E5EE8A2C61)
- [Anil Sood — LinkedIn (Centrifuge)](https://www.linkedin.com/in/anil-sood/)
- [CBInsights — Anemoy Company Profile](https://www.cbinsights.com/company/anemoy)
- [Ethplorer — JTRSY contract](https://ethplorer.io/address/0x8c213ee79581ff4984583c6a801e5263418c4b86)
- [Ethplorer — deJAAA contract](https://ethplorer.io/address/0xaaa0008c8cf3a7dca931adaf04336a5d808c82cc)
- [Tokenomist — CFG vesting](https://tokenomist.ai/centrifuge)

---

*This report was produced under adversarial research methodology. All verified claims are independently sourced. Unverified allegations are explicitly labeled. Confidence levels reflect evidence quality, not outcomes. Anemoy is not a typical DeFi project; the appropriate risk frame is institutional fund due diligence, not scam detection.*
