# Adversarial Due Diligence Report: Circle USYC (Hashnote US Yield Coin)

**Report Date:** 2026-04-04
**Analyst:** DeFi Adversarial Research Agent
**Framework:** Guilty-Until-Proven-Innocent
**Confidence Level:** High
**Overall Risk Verdict:** LOW-MEDIUM RISK (with specific centralization and regulatory vectors warranting close monitoring)

---

## ⚠️ LEAD FINDING — THIS IS NOT A DeFi PROTOCOL: IT IS A REGULATED FUND WITH BLOCKCHAIN WRAPPERS THAT CAN BE FROZEN, UPGRADED, AND REDEEMED WITHOUT YOUR CONSENT

USYC appears on-chain as an ERC-20 token, but it is legally a tokenized share of the **Hashnote International Short Duration Yield Fund Ltd.**, a Cayman Islands mutual fund licensed by CIMA. The key properties that distinguish it from typical DeFi are:

1. **The smart contract is an ERC1967 upgradeable proxy** — the implementation was upgraded at least once already (December 9, 2025). The upgrade key holder is not publicly disclosed. Circle/Hashnote can change the contract logic with no announced timelock.

2. **An Entitlements contract can freeze ALL USYC transactions globally** — Hashnote retains the power to "prevent any transaction from being completed" across the entire token system during "suspicious activity." This is not a standard blacklist; it is a global transaction halt.

3. **Fund directors can compulsorily redeem your USYC without notice** — per the fund's own documentation, directors have broad discretionary powers including forced redemption of any holder at any time.

4. **84% of the total $2.2B AUM sits on BNB Chain, controlled by Binance's custody arm (Ceffu)** — Binance (under active DOJ monitoring agreement through 2028 following 2023 conviction) holds indirect custody of the vast majority of all USYC. If Binance terminates the partnership, USYC loses its primary use case overnight.

The underlying assets (US Treasury Bills in short-duration repo) are among the safest instruments in existence. The risk is not the T-bills. The risk is the operational, legal, and custodial architecture wrapping those T-bills in a tokenized format that concentrates enormous control in Circle, Hashnote directors, and Binance.

---

## Executive Summary

| Category | Finding |
|---|---|
| Protocol Type | Tokenized money market fund (regulated Cayman Islands fund, Bermuda-issued token) |
| Underlying Assets | US T-bills + repo/reverse-repo (minimal credit/duration risk) |
| Chains | Ethereum, BNB Chain, Solana, Arbitrum, Canton Network |
| Total AUM | ~$2.2B (March 2026); #1 tokenized treasury product globally |
| AUM Concentration | ~$1.84B ($84%) on BNB Chain via Binance institutional collateral |
| Issuer | Circle International Bermuda Limited (BMA-regulated) |
| Fund Domicile | Cayman Islands (CIMA-registered mutual fund — filing-only, not substantive oversight) |
| Original Founders | Leo Mizuhara (CEO→VP Product at Circle), David Shapiro (CTO→Director of Engineering at Circle) |
| Incubated By | Cumberland Labs ($5M, DRW subsidiary) |
| Contract | ERC1967 upgradeable proxy; source verified on Etherscan; upgraded Dec 9, 2025 |
| Ethereum Holders | 32 wallets |
| Audits | Contract "externally audited" per docs; specific firm NOT publicly disclosed |
| Price | ~$1.12 (reflects yield accumulation since $1.00 issuance) |
| Top Risk | Binance concentration + Circle regulatory exposure (CRCL stock -70% from IPO) |

---

## Team Assessment

### Leo Mizuhara — Hashnote Co-Founder (CEO → VP Product at Circle)

- **Identity:** Fully named, public LinkedIn, documented podcast appearances (AIMA, Epicenter, Blockworks bylines), media-cited extensively.
- **Prior career (verified):**
  - 5 years at DRW as Head of Systematic Trading, FICC Options — ran 40+ traders, engineers, and researchers.
  - 12 years at Bank of America, Managing Director and Senior Portfolio Manager, Corporate Investments Group.
  - Deep institutional fixed income pedigree — the credentials are real and verifiable.
- **Post-acquisition:** Leo became **VP of Product at Circle** (confirmed via The Org, RocketReach). He did not maintain an independent founder role. He now reports to Circle's management hierarchy.
- **Key relationship: Leo worked at DRW** before Hashnote was incubated by Cumberland Labs (DRW's crypto arm). He left DRW to found a company that was then funded by his former employer. This is not fraud, but it is a tightly circular relationship.

### David Shapiro — Hashnote Co-Founder (CTO → Director of Engineering at Circle)

- **Identity:** Fully named, public LinkedIn.
- **Prior career (verified):**
  - Co-founded Scout Security (ASX IPO) — a verifiable, publicly traded exit.
  - VP Engineering at Latch Inc. (NASDAQ IPO) — second verifiable public company exit.
  - JPMorgan Chase (2010–2012, Product Engineer, Private Banking).
- **Verdict:** Two successful IPO exits with institutional engineering background. The strongest possible legitimacy anchor for a technical co-founder.
- **Post-acquisition:** Director of Engineering at Circle (confirmed via The Org).

### Organizational Notes

- Hashnote originally had only 5 employees total. Circle absorbed the entire team.
- Both named founders are now full-time Circle employees — they are no longer independent operators of the USYC product.
- **The product that users interact with is now operated by Circle (NYSE: CRCL), a publicly traded company** — not an anonymous team or small startup.

---

## The Cumberland/DRW Triple Conflict

This relationship deserves explicit documentation as it spans multiple layers:

| Layer | Role | Implication |
|---|---|---|
| **2022 — Founding** | Cumberland Labs (DRW) incubated Hashnote with $5M | Cumberland acquired equity in Hashnote |
| **Founder origin** | Leo Mizuhara came FROM DRW | Founder had prior financial relationship with his lead investor |
| **2025 — Acquisition** | Circle acquired Hashnote; DRW became strategic partner simultaneously | Cumberland's equity converted to Circle stock (CRCL) |
| **Post-acquisition** | Cumberland is primary liquidity provider for USDC and USYC | Cumberland earns trading spreads on products it helped create and owns equity in |
| **Ongoing** | Cumberland uses USYC as institutional collateral itself | Cumberland is both market-maker and end-user of the product |

**Verdict:** All parties are regulated TradFi entities with public identities, reducing outright fraud risk. However, the incubator/liquidity-provider/equity-holder tri-role for DRW/Cumberland means there are multiple undisclosed incentive alignments that USYC investors should understand.

---

## Third-Party Consensus

### Steakhouse Financial (Independent Research, 2024)

Published an independent analysis of USYC. Key findings:
- **Positive:** BNY Mellon custody (top-tier custodian), professional prime brokerage (Marex), independent annual audit.
- **Concern 1: 10% performance fee** — substantial drag on yield in high-rate environments. For a T-bill fund yielding 4–5%, a 10% performance fee could consume 0.4–0.5% of annual yield.
- **Concern 2: Compulsory redemption without notice** — directors retain broad discretionary powers to redeem any holder at any time.
- **Concern 3: KYC/AML procedures vary** across comparable products — regulatory landscape unsettled.

### Chaos Labs / Renzo Protocol Governance (March 2025)

No specific Chaos Labs risk briefing for USYC was found (unlike the cap.app equivalent). USYC is viewed as collateral by multiple governance forums; the absence of formal risk briefings is itself a signal that the product is considered relatively low-risk by the DeFi risk community.

### Nansen Research (2024)

Published "What is Hashnote USYC?" as a neutral informational article confirming the T-bill backing structure. No adversarial findings.

### CoinDesk / Fortune / The Block

All coverage is positive or neutral. No critical investigative journalism found targeting USYC specifically.

### Circle Stock (CRCL) Market Signal

The equity market's view of Circle's business model is worth noting:
- Circle IPO'd on NYSE June 5, 2025.
- CRCL stock has declined approximately **70% from its IPO-day high** (per Motley Fool, December 2025).
- On March 24, 2026, CRCL fell **20.1% in a single session** following draft CLARITY Act language banning yield on stablecoins, wiping ~$5.6B in market cap.
- The stock's poor performance signals market doubt about Circle's revenue model sustainability — a concern that could, if Circle faces financial stress, affect its governance of USYC.

---

## On-Chain Findings

### Contract Architecture

**Ethereum address:** `0x136471a34f6ef19fE571EFFC1CA711fdb8E49f2b`

| Property | Detail |
|---|---|
| Standard | ERC-20 (ERC1967 upgradeable proxy) |
| Implementation | `0xbf0f2f3aad6b99893d80c550fbacec915545eb92` |
| Decimals | 6 |
| Compiler | Solidity v0.8.17 |
| Source Verified | Yes (Etherscan) |
| Upgrade History | At least one upgrade: December 9, 2025 |
| Holders (ETH) | 32 wallets |

**Upgradeability Risk:** The ERC1967 proxy means Circle/Hashnote can replace the entire token logic. There is no publicly disclosed admin key address, timelock duration, or multisig configuration for the upgrade authority. The December 2025 upgrade was conducted without a public announcement found in search results.

**Entitlements Contract:** The token enforces a permissioned allowlist. Every transfer checks:
1. Whether the sender and recipient are on the allowlist
2. Whether either wallet matches an OFAC sanctions oracle on-chain
3. If Hashnote has globally frozen all transfers (emergency mode)

**Implications:**
- Any wallet can be de-whitelisted by Circle/Hashnote at any time, rendering their tokens non-transferable (but still redeemable through the Teller).
- A global transaction freeze is possible with no minimum notice requirement.
- The OFAC oracle is a third-party dependency — if it fails or is manipulated, legitimate transfers could be blocked.

### Multi-Chain Deployment and AUM Distribution

| Chain | Approximate AUM | Notes |
|---|---|---|
| BNB Chain | ~$1,840M (~84%) | Binance institutional collateral via Ceffu custody |
| Ethereum | ~$110M (~5%) | Primary DeFi integration hub |
| Solana | Growing (launched Oct 2025) | Circle-native SPL token |
| Arbitrum | Active | STEP program approved |
| Canton Network | Active | Privacy-preserving deployment |

**Critical finding: 84% AUM concentration on BNB Chain.** The Binance integration (July 2025) allowed institutional clients to use USYC as yield-bearing collateral for derivatives trading with no service fees until 2026. This drove explosive AUM growth but created extreme single-partner dependency:
- Binance is subject to a DOJ monitoring agreement through 2028 following its November 2023 criminal plea and $4.3B settlement (Changpeng Zhao resigned as CEO).
- Binance's custody arm (Ceffu, formerly Binance Custody) holds the institutional USYC positions.
- If Binance terminates the partnership, is forced to unwind by regulators, or suffers a custody failure, $1.84B of USYC collateral would need to be redeployed or redeemed rapidly.

### Token Price and Yield Mechanics

- USYC is NOT a stablecoin. It starts at $1.00 and appreciates as yield accrues.
- Current price: ~$1.12 (reflecting ~12% cumulative yield since launch, approximately consistent with 2023–2025 T-bill rates).
- Redemptions are processed via the Teller contract: 24/7, T+0 settlement, at the latest reported price.
- Subscriptions after 2 PM EST are priced at next business day's NAV.
- **Daily pricing** (not continuous): NAV updates once per day, not in real-time. Intra-day redemptions receive the most recently reported price, not a real-time T-bill market price.

### Smart Contract Audit Status

- USYC docs state contracts are "externally audited" by an unspecified firm.
- **No publicly identified audit firm found** in web search results (no Zellic, Trail of Bits, Certora, or other named firm credited).
- **No public audit report found** — no published PDF, no GitHub audit repository.
- Etherscan source code is verified (readable), which is a minimum transparency standard met.
- **Verdict:** This is the single most significant gap in USYC's security documentation for a $2.2B product. An unidentified, unpublished audit for a contract that has been upgraded at least once is below the standard of every DeFi protocol investigated in this session series.

### Fund Custody and Attestation

- **Custodian:** BNY Mellon (confirmed by Steakhouse Financial) — the world's largest custodian bank.
- **Prime Broker:** Marex (mid-tier institutional broker).
- **Annual Audit:** Independent (auditor not named in available sources).
- **Proof of Reserves:** No on-chain proof of reserve mechanism was identified. Users must trust:
  1. BNY Mellon holds the T-bills
  2. The fund's annual audit accurately reflects holdings
  3. Circle International Bermuda Ltd. accurately reports NAV

---

## Red Flags Register

| # | Severity | Finding | Evidence |
|---|---|---|---|
| 1 | 🔴 HIGH | **84% of AUM on BNB Chain via Binance/Ceffu** — single-partner dependency on an exchange under active DOJ monitoring agreement | BNB Chain blog, Circle press releases, Binance DOJ settlement |
| 2 | 🔴 HIGH | **Smart contract audit firm and report NOT publicly disclosed** — $2.2B product with undisclosed, unpublished audit; below industry standard | Web search, USYC docs: "externally audited" without naming firm |
| 3 | 🔴 HIGH | **ERC1967 upgradeable proxy with undisclosed upgrade authority** — contract was already upgraded Dec 9, 2025; no public timelock or multisig config identified | Etherscan proxy contract |
| 4 | 🔴 HIGH | **Global transaction freeze power** — Hashnote/Circle can halt ALL USYC transfers across all holders simultaneously; no minimum notice required | USYC docs; Entitlements contract documentation |
| 5 | 🟠 MEDIUM | **Circle stock (CRCL) down ~70% from IPO high and -20% in single session** — market is signaling severe doubt about Circle's revenue model; parent company financial stress could affect USYC governance | Motley Fool, CoinDesk CRCL coverage |
| 6 | 🟠 MEDIUM | **CLARITY Act threat to Circle's broader business model** — while USYC (a fund) may be exempt from the yield ban, Circle's USDC revenue model is threatened; Circle's institutional standing as USYC issuer depends on its financial health | CoinDesk CLARITY Act coverage |
| 7 | 🟠 MEDIUM | **Compulsory redemption without notice** — fund directors can forcibly redeem any holder at their discretion | Steakhouse Financial analysis; product structuring docs |
| 8 | 🟠 MEDIUM | **10% performance fee** — substantial yield drag in high-rate environments; reduces USYC's competitive advantage over direct T-bill access | Steakhouse Financial analysis |
| 9 | 🟠 MEDIUM | **CIMA registration is filing-only, not substantive oversight** — fund is not supervised "in respect of its investment activities" by any Cayman regulator | USYC product structuring docs |
| 10 | 🟠 MEDIUM | **DRW/Cumberland triple conflict** — incubated Hashnote, converted equity to Circle stock, and is now primary USDC/USYC liquidity provider | Multiple sources; no public conflict-of-interest disclosure |
| 11 | 🟠 MEDIUM | **Founders now Circle employees with no independent governance role** — post-acquisition, Leo Mizuhara and David Shapiro are VP/Director-level employees with no formal power to protect USYC holders against Circle decisions | The Org profiles |
| 12 | 🟡 LOW | **Daily NAV pricing, not real-time** — intra-day redemptions price at last daily NAV; during market dislocations, this could create arb gaps or delays | USYC docs subscription & redemption page |
| 13 | 🟡 LOW | **"No-US persons" restriction with on-chain enforcement** — USYC is restricted to non-US persons for direct on-chain ownership; US investors must use feeder fund structures; regulatory compliance depends on OFAC oracle accuracy | USYC docs; Entitlements contract design |
| 14 | 🟡 LOW | **Canton Network deployment** — USYC on Canton uses privacy features (private blockchain); less verifiable than public Ethereum deployment | Canton Network press release |
| 15 | 🟡 LOW | **Acquisition price undisclosed** — Circle paid undisclosed amount for Hashnote; Cumberland/DRW's equity return on their $5M incubation is unknown; no independent fairness opinion published | Multiple sources; standard for private M&A |

---

## Unresolved Questions

1. **Who holds the ERC1967 proxy upgrade key?** Is it a multisig? How many signers? What is the timelock? This is the most important unanswered technical question for any USYC holder.

2. **Which firm audited the USYC smart contracts?** Why is the audit firm and report not publicly named or linked? This is standard for any DeFi protocol with more than $100M TVL.

3. **What changes were made in the December 9, 2025 contract upgrade?** Was this upgrade announced publicly? Was the new implementation re-audited before deployment?

4. **Is USYC exempt from the CLARITY Act yield ban?** USYC is a fund (not a stablecoin), which likely exempts it from provisions targeting "stablecoin issuers." But regulators may disagree. Is there a legal opinion on this?

5. **What is the actual annual fund audit process?** Who is the independent auditor for the Hashnote International Short Duration Yield Fund Ltd.? Are the annual financial statements publicly available?

6. **What is the exact fee structure?** The performance fee is 10% of what base? Is there also a management fee? What is the total expense ratio?

7. **What happens to USYC if Circle (CRCL) faces financial stress, bankruptcy, or regulatory shutdown?** Who controls the fund in that scenario? Is there a continuation vehicle? Is there a separation between Circle's operating company and the fund's assets at BNY Mellon?

8. **How does the Binance integration unwind?** If Binance's DOJ agreement is violated, if Binance faces additional regulatory action, or if the partnership simply expires — is there a redemption process for the $1.84B in institutional USYC collateral? What is the timeline?

9. **What are the Feeder Fund LP lock-up terms for US investors?** US persons must access USYC through the Hashnote Master Fund structure. What are the redemption terms there, and are they different from the direct USYC on-chain redemption?

10. **Has Marex (prime broker) ever faced regulatory action or financial stress?** Marex is a mid-tier broker, not a bulge-bracket institution. What happens to USYC if Marex faces a prime brokerage disruption?

---

## Positive Signals

- **Underlying assets:** US Treasury Bills and reverse repo are among the safest instruments in human financial history. Default risk is effectively zero.
- **BNY Mellon custody:** The world's largest custodian bank holds the T-bill collateral. This is a legitimate institutional safeguard.
- **Named, verifiable team with elite pedigree:** Leo Mizuhara (DRW, Bank of America) and David Shapiro (Scout Security ASX IPO, Latch NASDAQ IPO) are among the most credentialed founders in the RWA tokenization space.
- **Circle (NYSE: CRCL):** For all its stock performance issues, Circle is a publicly traded, SEC-reporting company subject to Sarbanes-Oxley, continuous disclosure, and multiple regulatory frameworks. This accountability layer is absent in pure DeFi.
- **$2.2B AUM:** Scale itself is a signal — BNY Mellon, Binance, Arbitrum DAO, and multiple institutional users have conducted their own due diligence.
- **DeFi integrations:** USYC is approved collateral in Aave Horizon, the Arbitrum STEP program, and multiple institutional venues — third-party risk teams at these protocols reviewed USYC and approved it.
- **No exploits, no incidents in 2+ years of operation** (Hashnote launched February 2023, Circle acquired January 2025).
- **CIMA + BMA dual regulation:** While Cayman oversight is filing-only, the Bermuda Monetary Authority (BMA) supervises Circle International Bermuda Ltd. as the token issuer — providing a second layer of regulatory oversight.
- **Daily independent pricing:** NAV is set daily by an independent process, not by Circle/Hashnote unilaterally.

---

## On-Chain Contract Reference

| Asset | Address | Chain |
|---|---|---|
| USYC Token | `0x136471a34f6ef19fE571EFFC1CA711fdb8E49f2b` | Ethereum |
| USYC Token | `0x8D0fA28f221eB5735BC71d3a0Da67EE5bC821311` | BNB Chain |
| USYC Token | `7LWanZteUKtvFjv4MHYgKXXdAuCQYFPJysL9pxxdRQGn` | Solana |
| Implementation | `0xbf0f2f3aad6b99893d80c550fbacec915545eb92` | Ethereum |
| Circle CRCL | NYSE: CRCL | Public market |
| Docs | usyc.docs.hashnote.com | — |
| DeFiLlama | defillama.com/stablecoin/cap-cusd | — |

---

## Summary Verdict

**LOW-MEDIUM RISK** | Confidence: High

USYC is the safest underlying instrument in this series of investigations — US Treasury Bills cannot rug-pull, and BNY Mellon cannot exit-scam. The token is issued by a publicly traded company (Circle, NYSE: CRCL) with SEC oversight. The original founders have exceptional, verifiable credentials.

However, USYC is **not a DeFi-native instrument** and should not be evaluated as one. It is a permissioned, upgradeable, freezable, compulsorily-redeemable tokenized fund share. The risk profile is:
- **Near-zero:** Underlying asset default risk (T-bills)
- **Low:** Team legitimacy / fraud risk (Circle is a public company, founders have institutional backgrounds)
- **Medium:** Concentration risk (84% AUM tied to Binance/DOJ monitoring)
- **Medium:** Regulatory risk (Circle's stock has been devastated by CLARITY Act concerns)
- **Medium:** Operational centralization risk (undisclosed upgrade key, global freeze capability, no published audit report)
- **Unknown:** Smart contract audit quality (unpublished, unidentified firm)

For a DeFi user expecting permissionless, non-custodial exposure to T-bill yield: **USYC is not that product.** Holders are subject to Circle/Hashnote's discretion in ways that no other protocol in this series — not even Polymarket — concentrates in a single corporate entity.

For an institutional user seeking tokenized T-bill exposure with Circle's brand behind it: **the T-bill backing is real, the custody is real, and the yield is real. The centralization is also real.**
