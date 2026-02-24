# A7A5 — DeFi Adversarial Due Diligence Report
**Investigator:** Claude (Adversarial Research Framework)
**Date:** 2026-02-24
**Confidence:** HIGH

---

## CRITICAL ALERT

This is not a conventional DeFi rug pull risk. This is a U.S., UK, and EU-SANCTIONED
financial crime network. Interacting with A7A5 — holding, trading, providing liquidity,
or receiving tokens — may constitute a violation of OFAC sanctions regulations, carrying
civil penalties up to $1.5M per violation and criminal penalties including imprisonment.

---

## Executive Summary

VERDICT: AVOID — maximum confidence.

A7A5 is a ruble-backed stablecoin and Russian sanctions evasion instrument. It is
operationally linked to Ilan Shor (convicted of $1B Moldovan bank fraud), Promsvyazbank
(sanctioned Russian defense bank), and the network that succeeded Garantex (a
$100M+ ransomware/darknet laundering exchange).

Sanctioned by:
- United States (OFAC): August 14, 2025
- United Kingdom (OFSI): May 2025 + August 2025
- European Union: July 2025 + October 2025 (19th package, transaction ban)

Top 3 Risks:
1. OFAC/Sanctions exposure: Transacting as a U.S. person = federal crime
2. Beneficial owner convicted of $1B fraud, is a sanctioned Kremlin operative
3. Reserves held at sanctioned Promsvyazbank — unattested, controllable by Russian state

---

## Team Assessment

### Ilan Shor (51% owner of A7 LLC)
- VERIFIED: Convicted 2017, Moldovan courts, for masterminding $1B+ bank theft
- VERIFIED: Sentenced 15 years in absentia, Moldova, 2023
- VERIFIED: Sanctioned US (2022), EU, UK for election interference in Moldova on behalf of Russia
- VERIFIED: Met Putin in September 2025, boasted A7 processed $89B in payments
- Currently residing in Moscow

### Pyotr Fradkov (Co-executive, A7 LLC)
- VERIFIED: Head of Promsvyazbank since 2018
- VERIFIED: Son of Mikhail Fradkov (Putin's PM 2004-2007; FSVRdirector)

### Promsvyazbank (PSB) — Major shareholder
- VERIFIED: Russian state-owned bank, nationalized 2018
- VERIFIED: Sanctioned US, EU, UK for financing Russia's defense sector
- Holds ruble reserves backing every A7A5 token

### Old Vector LLC — Formal token issuer
- VERIFIED: Registered Kyrgyzstan, December 2024
- VERIFIED: Registered at residential address (shell company indicator)
- VERIFIED: Sanctioned by OFAC, August 2025
- Zero named founders or technical staff

### UNVERIFIED / NOT FOUND:
- Any technical developers or smart contract authors
- GitHub profiles or commit history for any team member
- Any academic or professional credentials

---

## Third-Party Consensus

ALL major blockchain intelligence firms have covered A7A5:

- Chainalysis: "A unique sanctions evasion tool." $51B+ cumulative volume.
  Monday-Friday trading dominance = commercial/corporate sanctions evasion.
- Elliptic: $1B+/day peak; $1.2-1.3B USDT injected into A7A5 DEX post-Garantex seizure.
- TRM Labs: Traced Garantex wallet TNDjh6WGLYyWmkh8vfu42bXVHUqFNQ3rDq seeding
  A7A5 in January 2025 — 2 months BEFORE Garantex seizure in March 2025.
  FINDING: Enforcement evasion was deliberately pre-planned.
- Centre for Information Resilience: Shared digital infrastructure with Moldovan
  election interference network.
- RFE/RL: Full investigative report with Kyrgyz corporate registry documentation.

Security Audit Status: NONE FOUND. Zero results from CertiK, PeckShield, Trail of Bits,
Hacken, or any recognized auditor.

---

## On-Chain Findings

### Contract Addresses
- Ethereum (ERC-20): 0x6fA0BE17e4beA2fCfA22ef89BF8ac9aab0AB0fc9
- wA7A5 (Ethereum): 0xF442fF10b8deF89514560A66C0AD28777094636a
- wA7A5 deprecated: 0x0d57436f2d39c0664c6f0f2e349229483f87ea38
- Tron (TRC-20): TLeVfrdym8RoJreJ23dAGyfJDygRtiWKBZ

### Contract Properties
- Compiler: Solidity v0.8.22 | Optimization: DISABLED
- Verified on Etherscan: YES (source code public)
- Admin functions present: pause(), unpause(), updateBasisPointsRate(), distributeInterest()
- Timelock: NOT FOUND | Multisig: NOT DOCUMENTED | Governance: NONE

### Token Metrics (Ethereum)
- Total supply: ~531M tokens
- Holders: ~10,200-13,600
- Price: ~$0.0128 (~1 RUB)
- Total transactions: 8,637+

### Scale (All Chains)
- All-time volume: $68B-$100B+
- Peak daily volume: $1.5B+
- Tokens in circulation: 41.6B (majority on TRON)
- Market cap: ~$496-521M

### Transaction Pattern Flags
- Grinex (primary exchange, itself OFAC-sanctioned) drives majority of volume
- A7A5 DEX routes to no-KYC Russian-linked payment processors
- Garantex wallet seeded A7A5 liquidity 2 months before Garantex enforcement action
  = deliberate pre-planning for sanctions circumvention

---

## Red Flags Register

CRITICAL:
1. OFAC-sanctioned entity (Aug 2025) — federal crime for U.S. persons to transact
2. EU-sanctioned (transaction ban, Oct 2025) — illegal for EU persons
3. UK-sanctioned (May + Aug 2025) — illegal for UK persons
4. 51% owner convicted of $1B bank fraud + 15-year sentence
5. Reserve custodian (PSB) is a sanctioned Russian defense bank
6. Network is direct successor to Garantex ($100M+ in ransomware/darknet flows)
7. Pre-planned enforcement evasion: infrastructure built before Garantex seizure

HIGH:
8. Completely anonymous technical team — zero accountability
9. No security audit from any recognized firm
10. pause() + updateBasisPointsRate() with no governance or timelock
11. Shell company issuer (Old Vector, residential address, Dec 2024 registration)
12. Reserves unattested — peg integrity unverifiable
13. Primary exchange (Grinex) is itself OFAC-sanctioned

LOW:
14. Optimization disabled at contract deployment
15. Deprecated wrapped token contract (unexplained iteration)

---

## Unresolved Questions

1. Who holds the admin/owner private keys for the Ethereum contract?
2. What is the actual RUB reserve proof at PSB?
3. Who are the technical developers?
4. Full token distribution on TRON (majority volume chain)?
5. Has Kyrgyzstan taken domestic enforcement action against Old Vector/Grinex?
6. Who controls A7A5's proprietary DEX contracts?

---

## Sources

- Centre for Information Resilience: https://www.info-res.org/reports/a7a5-circumventing-sanctions-with-stablecoin-cryptocurrency/
- Elliptic (multiple reports): https://www.elliptic.co/blog/the-rise-of-a7a5-the-ruble-stablecoin-now-transfers-1-billion-per-day
- Chainalysis: https://www.chainalysis.com/blog/a7a5-grinex-russian-crypto-economy-ofac-sanctions-august-2025/
- TRM Labs: https://www.trmlabs.com/resources/blog/garantex-grinex-and-the-a7a5-token-a-deep-dive-into-sanctions-evasion-networks
- CoinDesk OFAC: https://www.coindesk.com/policy/2025/08/14/ofac-sanctions-crypto-network-behind-ruble-backed-stablecoin-and-shuttered-exchange-garantex
- RFE/RL Investigation: https://www.rferl.org/a/russia-cryptocurrency-moldova-kyrgyzstan-a7-sanctions/33609918.html
- Etherscan contract: https://etherscan.io/token/0x6fA0BE17e4beA2fCfA22ef89BF8ac9aab0AB0fc9
