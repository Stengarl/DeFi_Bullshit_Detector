# Adversarial Due Diligence Report: cap.app (Cap Protocol / cUSD)

**Report Date:** 2026-04-04
**Analyst:** DeFi Adversarial Research Agent
**Framework:** Guilty-Until-Proven-Innocent
**Confidence Level:** Medium-High
**Overall Risk Verdict:** MEDIUM RISK (with systemic architecture caveats warranting MEDIUM-HIGH)

---

## ⚠️ LEAD FINDING — THE "BLOW-UP-PROOF" GUARANTEE IS AN OFF-CHAIN LEGAL CLAIM BACKED BY CONFLICTED PARTIES

Cap's central marketing claim is that cUSD is "blow-up-proof" because operator defaults are covered by restaker slashing and, beyond that, by **off-chain legal agreements with regulated financial institutions.** Independent risk firm Chaos Labs (assessing the protocol for Renzo Protocol integrations) concluded that "recovery depends heavily on off-chain legal agreements rather than on-chain protections" and that "a credit event could result in losses equaling the full loan value."

The most structurally alarming element: the "regulated financial institutions" who serve as operators — Franklin Templeton, Susquehanna, Flow Traders, IMC Trading, GSR, Nomura's Laser Digital — are **simultaneously equity investors in Cap Labs**. These firms collected equity upside from Cap's growth, AND they are the primary borrowers of user funds from the protocol. If an operator-investor fails, users suffer the primary loss while the entity in default is the same entity that helped capitalize and promote the protocol. This is a textbook conflict of interest that the protocol does not address publicly.

Compounding this: **over 80% of all cUSD reserves (~$360M) are currently deployed into Aave V3** — a single third-party DeFi protocol. The protocol's "safe" idle reserve layer is itself a concentrated DeFi counterparty risk. An Aave exploit or freeze would be existential for cUSD backing.

---

## Executive Summary

| Category | Finding |
|---|---|
| Protocol Type | Covered-credit yield stablecoin (cUSD / stcUSD) |
| Chain | Ethereum mainnet; MegaETH (L2, launched Feb 2026) |
| TVL | ~$271M (DeFiLlama); self-reported $500M at peak Jan 2026 |
| Mainnet Launch | August 19, 2025 |
| Founder | Benjamin Sarquis Peillard (@Benjamin918_); named, verifiable |
| Prior Role | COO at Hashing Systems (crypto infrastructure) |
| Funding | $11M total (Pre-seed $1.9M + Seed $8M + Community $1.1M) |
| Lead Investors | Franklin Templeton, Triton Capital, Susquehanna, Flow Traders, Nomura/Laser Digital, GSR, IMC Trading, RockawayX |
| Audits | 8 engagements: Zellic, Trail of Bits, Electisec, Spearbit (×2), Recon, Sherlock, Certora |
| CAP Token | Not yet fully launched; 40% insider allocation (team 20% + investors 20%); no vesting schedule disclosed |
| Overall Risk | MEDIUM (no exploits; systemic design risks and conflicts unresolved) |

---

## Team Assessment

### Founder: Benjamin Sarquis Peillard

- **Identity:** Fully named and public. Twitter: @Benjamin918_, LinkedIn active, featured on Epicenter podcast (Episode 618), multiple media profiles (Fortune, CoinDesk, The Block quotes).
- **Claimed history:** "3x crypto founder, OG DeFi contributor" per LinkedIn post.
- **Verifiable prior role:** COO at Hashing Systems (crypto infrastructure company). F6S profile confirms this title.
- **Unverifiable claims:** The "3x founder" claim cannot be independently verified from public records. No names or outcomes of the prior two ventures were found in open sources. Hashing Systems itself is not a well-documented public company — no website, no CrunchBase listing found.
- **Argentine background:** @gsarquis (Gonzalo Sarquis) is active on Twitter and appears to be a relative — consistent with a Latin American background for Benjamin Sarquis Peillard. Not a red flag, merely context.
- **Public accountability:** High. Founder has given podcast interviews, appeared in mainstream financial press (Fortune, Fortune Crypto), and is named in regulatory filings context. This is a meaningful legitimacy anchor.

### Team Transparency

- **GitHub org:** `github.com/cap-labs-dev` — 7 public repositories, 0 public members listed, membership is private.
- **Publicly named team members:** Only the founder is named in press coverage. No CTO, Head of Engineering, or other named team members appear in search results.
- **Known partnerships:** WisdomTree (institutional asset manager — Cap provides protected yield to WisdomTree users), Aave (reserve deployment), RedStone (oracle provider), EigenLayer and Symbiotic (restaking infrastructure).
- **Assessment:** Single named public face is a moderate concern for a $271M+ protocol. The underlying technical team is anonymous.

---

## Third-Party Consensus

### Independent Risk Assessment — Chaos Labs (Renzo Protocol Governance)

Chaos Labs conducted an independent risk briefing specifically evaluating Cap protocol's risk for the Renzo ecosystem. Their documented concerns:

1. **"Full loan value" slashing exposure**: A credit event can produce losses equal to the entire borrowed amount — far exceeding the partial slashing common in PoS slashing conditions.
2. **Active position management required**: Restakers must continuously monitor health factors and inject collateral during stress events — a demanding operational requirement.
3. **Off-chain legal agreements as primary protection**: On-chain mechanisms cover collateral up to the staked amount. Beyond that, recourse is contractual, not algorithmic.
4. **Liquidity lockup**: Delegated stake is locked for the full loan duration; withdrawals require loan completion plus additional waiting periods.
5. **Undefined governance for slashing parameters**: Liquidation bonuses, grace periods, and key parameters lack defined governance procedures — can change without restaker input.

### Serenity Research (Independent Research Substack, August 2025)

Described Cap's structure as analogous to a **Credit Default Swap (CDS) on-chain** — not a CDO, but a CDS. Restakers sign legal agreements to cover defaults and post on-chain collateral. The structure works as long as (a) restakers remain solvent and (b) legal agreements are enforceable across jurisdictions. Neither is guaranteed.

### OAK Research (MegaETH Protocol Report)

Published analysis confirming the three-sided marketplace model (minters, operators, delegators) with yield derived from idle reserves deployed to Aave and Fluid. Acknowledged the EigenLayer dependency as a systemic risk factor.

### Positive Coverage

- **The Block, Fortune, CoinDesk:** Standard funding announcement coverage; uniformly positive tone.
- **Blocmates Guide (August 2025):** Detailed explainer; notes the model is genuinely novel but acknowledges restaker risk.
- **Aave Blog:** Confirms the Cap cUSD integration on Aave; treated as a positive signal by Aave governance.

---

## On-Chain Findings

### Protocol Architecture

Cap operates as a three-sided credit marketplace:
- **Minters:** Deposit USDC/USDT (1:1) → receive cUSD; stake cUSD → receive stcUSD (yield-bearing)
- **Operators:** Whitelisted institutional borrowers (Franklin Templeton, Susquehanna, Flow Traders, etc.) — borrow cUSD from the vault, generate yield off-platform
- **Delegators/Restakers:** Post overcollateralized restaked assets (ETH via EigenLayer or Symbiotic) → vouch for operators; slashed if operator health factor < 1

### Reserve Deployment — Aave Concentration Risk

**This is an active, observable, high-severity risk:**

- Over 80% of cUSD reserves (reported: $300M–$360M) are deployed into **Aave V3 Core Ethereum market**.
- Cap's "Fractional Reserve" contracts auto-deploy idle capital to Aave to earn base yield for stcUSD holders.
- This means a critical path to cUSD depeg: **Aave V3 exploit → reserve loss → cUSD undercollateralization**.
- Cap acknowledges Aave as a "protocol risk" in their documentation but frames it as low-probability.
- **Verdict:** Concentration of 80%+ reserves in a single protocol contradicts the stated "blow-up-proof" design principle. This is the most immediately verifiable systemic risk.

### Contracts and Upgradeability

- **GitHub:** `github.com/cap-labs-dev/cap-contracts` — 16 stars, 8 forks, updated April 4, 2026 (today).
- Repository includes `check-proxy-implem.txt` and `check-access.txt` files — indicating upgradeability/access control was considered during development.
- The precise proxy configuration (UUPS vs. TransparentUpgradeableProxy, timelock duration, admin addresses) could not be confirmed from public search results. Cap's audit reports in `cap-audits` suggest the contracts are within Sherlock's competitive audit scope.
- **Sherlock audit (July 2025):** 0 open findings. Scope: Symbiotic integration; Mint, Burn, Redeem, Liquidate, Repay, RealizeInterest. Accepted known issues: 1-wei rounding in withdrawals (seeded), debt token index rounding (+1 wei to total supply).

### Oracle Dependency

- **RedStone** oracle integration (confirmed December 2025 blog post).
- RedStone is an established oracle provider but represents an additional off-chain dependency.
- Oracle failure scenarios: incorrect price feeds could allow undercollateralized borrowing or prevent liquidations.

### TVL and Growth

- **DeFiLlama:** ~$271M current TVL (all Ethereum).
- **Self-reported (January 2026):** $500M peak TVL.
- **Timeline:** Mainnet launched August 19, 2025 → $500M in ~5 months.
- Rapid TVL accumulation without incident is NOT the same as proven security. The protocol has not been stress-tested through a major market downturn.

### cUSD Stablecoin Mechanics

- 1:1 backed by USDC/USDT at issuance.
- Reserve assets include: USDC, USDT, tokenized money market funds (MMFs), Aave-deposited USDC.
- cUSD is a **LayerZero OFT** asset — bridgeable across chains.
- **Bridge risk:** As acknowledged in Cap's own risk docs, cross-chain use of cUSD introduces third-party bridge and oracle risk.

### CAP Token (Governance)

- **Status:** Not fully launched as of report date. Public sale registration opened February 5, 2026 via Uniswap CCA mechanism.
- **Token allocation:**
  - Ecosystem development: 46.72%
  - Team: up to 20%
  - Investors: up to 20%
  - Community ICO: 10%
  - Echo community sale: 3.28%
- **Vesting schedule: NOT PUBLICLY DISCLOSED** for the 40% insider bucket.
- Insider allocation of 40% with no disclosed vesting is a major governance red flag — if the token launches and unlocks immediately, selling pressure could be severe.
- **"Stabledrop":** $12M in cUSD distributed to early Frontier phase participants (February 2026). Framed as equivalent to ~5% of a $250M FDV. Source of the $12M: Cap's own protocol treasury (funded by the $11M raise + early yield earnings). This is a legitimate community distribution mechanism, not a Ponzi dynamic.

---

## Red Flags Register

| # | Severity | Finding | Evidence |
|---|---|---|---|
| 1 | 🔴 HIGH | **Investor-operator conflict of interest** — Franklin Templeton, Susquehanna, Flow Traders, IMC, GSR, Nomura are simultaneously equity investors and protocol borrowers | Fortune, The Block funding coverage; Cap blog posts confirming same entities as operators |
| 2 | 🔴 HIGH | **80%+ of cUSD reserves concentrated in Aave V3** — single DeFi counterparty failure would be existential for cUSD backing | Stabledash article; Aave blog; stcUSD mechanics docs |
| 3 | 🔴 HIGH | **"Blow-up-proof" guarantee relies on off-chain legal recourse** — Chaos Labs confirmed primary protection is legal contracts, not on-chain code; credit event can equal full loan value loss | Chaos Labs Cap Risk Briefing (gov.renzoprotocol.com) |
| 4 | 🟠 MEDIUM | **Trail of Bits audit NOT in their public publications GitHub** — claimed audit at `github.com/trailofbits/publications` not listed; cannot be independently cross-referenced via firm's standard publication index | Direct GitHub check of trailofbits/publications |
| 5 | 🟠 MEDIUM | **40% insider token allocation with no disclosed vesting schedule** — if team/investor tokens unlock at or near TGE, severe sell pressure possible | Cap docs token page; airdrop review sites |
| 6 | 🟠 MEDIUM | **Undefined governance for slashing parameters** — liquidation bonuses, grace periods changeable without restaker input; restakers locked in for full loan duration | Chaos Labs Risk Briefing |
| 7 | 🟠 MEDIUM | **MegaETH deployment on 2-month-old mainnet** — cUSD launched on MegaETH (mainnet: Feb 9, 2026) introducing compounded L2 infrastructure risk on brand-new chain | CoinDesk MegaETH mainnet coverage |
| 8 | 🟠 MEDIUM | **Only founder is named publicly; technical team is anonymous** — GitHub org has 0 public members; no CTO, Head of Smart Contracts, or other key personnel named | GitHub cap-labs-dev; media coverage |
| 9 | 🟠 MEDIUM | **"3x founder" claim unverifiable** — Benjamin Sarquis Peillard's prior two ventures cannot be identified or assessed from public records | F6S profile; no corroborating sources |
| 10 | 🟡 LOW | **Hashing Systems background unclear** — "COO at Hashing Systems" as prior role appears on F6S but Hashing Systems has no public web presence, CrunchBase listing, or searchable history | F6S member profile |
| 11 | 🟡 LOW | **$500M TVL growth in 5 months untested through market downturn** — protocol has never operated through a significant market stress event or liquidity crisis | DeFiLlama; self-reported cap figures |
| 12 | 🟡 LOW | **LayerZero OFT bridge risk** — cUSD bridgeable across chains; cross-chain scenarios introduce third-party bridge failure modes | Cap docs risk page |
| 13 | 🟡 LOW | **RedStone oracle dependency** — single oracle provider; incorrect feeds could allow undercollateralized loans or blocking of legitimate liquidations | RedStone blog post Dec 2025 |
| 14 | 🟡 LOW | **Certora audit not in their public SecurityReports GitHub** — audit report exists as CDN PDF but is not indexed in `github.com/Certora/SecurityReports` as of review date | Direct GitHub search |
| 15 | 🟡 LOW | **MegaETH is not formally EVM-equivalent** — ultra-high-throughput L2 may have execution differences; new audit surface for contracts deployed there | MegaETH documentation |

---

## Unresolved Questions

1. **Exact collateralization ratio:** What is the minimum required overcollateralization ratio for operator loans? Is it hardcoded or governance-adjustable? What happens if restaker collateral value drops faster than the grace period allows liquidation?

2. **Off-chain legal agreements — jurisdiction and enforceability:** Which jurisdictions govern the "Guarantor Agreements" with operators? If a Flow Traders entity in Amsterdam defaults, how long does legal recourse take? Who bears the loss in the interim?

3. **Operator whitelist process:** Who controls the whitelist? How are operators added or removed? Is there a timelock? Can the Cap Labs team add themselves or affiliated entities as operators?

4. **Vesting schedule for team/investor tokens:** When do the 40% insider CAP tokens unlock? Are there cliffs? This is the single most important undisclosed tokenomics parameter.

5. **Hashing Systems:** What was this company? When did it operate? What was Benjamin's role/tenure? Any prior project failures?

6. **Trail of Bits audit content:** Why is the May 2025 Trail of Bits audit not listed in their public publications index? What were the findings? Were all issues resolved?

7. **Proxy/upgradeability config:** What are the exact upgrade mechanisms in the deployed contracts? Who controls the admin keys? Is there a timelock and what is its duration?

8. **Aave concentration — is there a cap?** Is there a governance-set maximum percentage of reserves that can be deposited in any single protocol? Currently 80%+ suggests no enforced diversification requirement.

9. **Flow Traders as publicly traded operator:** Flow Traders (AEX: FLOW) disclosed in a Cap blog post that it uses Cap via EigenLayer. Does this appear in their public financial disclosures? What exposure size is disclosed?

10. **MegaETH contract audit:** Were the contracts deployed on MegaETH separately audited, or were only the Ethereum contracts reviewed?

---

## Positive Signals

- Named, media-facing, publicly accountable founder who has given multiple interviews
- Franklin Templeton as strategic investor — one of the most compliance-conscious asset managers in TradFi
- 8 audits from reputable firms over a 9-month period; Sherlock competitive audit found 0 valid issues
- $271M TVL demonstrates genuine user adoption
- WisdomTree partnership demonstrates institutional demand for the product
- Protocol went mainnet August 2025 and has had no exploits in its first 8 months
- The "Stabledrop" mechanism (distributing $12M of yield as stablecoin, not a volatile token) is a sophisticated community distribution that avoids the pump-and-dump token airdrop dynamic
- Certora formal verification performed on EigenLayer integration
- GitHub public and actively maintained

---

## On-Chain Contract Addresses (Partial — From Available Sources)

| Asset | Address | Chain |
|---|---|---|
| cUSD | Not confirmed in public search results | Ethereum |
| stcUSD | Not confirmed in public search results | Ethereum |
| GitHub | github.com/cap-labs-dev/cap-contracts | — |
| Twitter | @capmoney_ | — |
| Docs | docs.cap.app | — |
| DeFiLlama | defillama.com/protocol/cap | — |

---

## Summary Verdict

**MEDIUM RISK** | Confidence: Medium-High

Cap is a structurally ambitious, well-funded, and genuinely novel protocol — but its "blow-up-proof" marketing claim obscures a model that depends on: (a) off-chain legal agreements with counterparties who have conflicts of interest; (b) 80%+ reserve concentration in a single external DeFi protocol (Aave); and (c) restaker collateral being sufficient to cover full operator defaults in a stress scenario.

The protocol has not been tested through a bear market or liquidity crisis. TVL of $271M–$500M in <8 months with no exploits is a positive signal but not a security guarantee. The Franklin Templeton brand provides a legitimacy anchor but does not resolve the structural conflict of interest inherent in investor-operators.

**The critical unknown is the vesting schedule for 40% of CAP tokens.** If unlocks are near-term and uncliffed, token launch could be an exit event for early insiders.

For users: cUSD itself may be relatively safe for short-term holding given its USDC backing and Aave yield layer. The greater risk is a black swan scenario (Aave exploit + simultaneous operator default + restaker liquidation cascade), which while unlikely, would be existential. The "blow-up-proof" guarantee should be read as "blow-up-resistant with off-chain backstop" — a meaningfully different claim.
