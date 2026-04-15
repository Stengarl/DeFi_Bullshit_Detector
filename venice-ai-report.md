# Venice.ai (VVV Token) — Adversarial DeFi Due Diligence Report

**Report Date:** April 15, 2026  
**Researcher:** Adversarial Research Agent  
**Token Ticker Correction:** The token is **VVV** (Venice Token), not "VCE." No VCE token is associated with Venice.ai. All findings below use VVV.  
**Contract:** `0xacfE6019Ed1A7Dc6f7B508C02d1b04ec88cC21bf` on Base (Ethereum L2)  
**Chain:** Base  
**Launch Date:** January 27, 2025  

---

## 1. EXECUTIVE SUMMARY

**Verdict:** Venice.ai is a **real product with a documented founder and verifiable track record — but the VVV token launch was materially compromised by insider trading, alleged undisclosed minting, and a founder with a pattern of regulatory friction spanning three enforcement events over a decade. The token is HIGH RISK for investors despite the platform being LOW-MEDIUM risk for users of the AI service.**

**Confidence Level:** HIGH — multiple independent sources corroborate all major findings.

**Top 3 Risks:**
1. **Insider trading at token launch (CONFIRMED):** Aerodrome Finance contributors front-ran the VVV launch with insider knowledge; VVV crashed 50% on Day 1 and is now -82% from ATH. Separate allegations of a secret 1M-token post-listing mint (~$5.79M) by the Venice team itself remain unresolved.
2. **Founder regulatory history (HIGH CONFIDENCE):** Erik Voorhees has two direct SEC settlements (2014 personal; 2024 ShapeShift corporate), one SEC investigation resolved without personal charges (2018 SALT), and a history of building no-KYC infrastructure later used by sanctioned actors. VVV is his third token-adjacent event involving insider-benefit allegations.
3. **Platform used as a cybercrime tool (CONFIRMED by 6+ independent security firms):** Venice is documented as the tool of choice in underground hacking forums for generating malware, ransomware, keyloggers, and phishing. Regulatory action targeting Venice directly is a non-trivial risk.

**Top 3 Positive Signals:**
1. Real AI product with 900,000+ users and 50,000 daily active users — not a token-only scheme.
2. Self-funded by Voorhees with no VC backing — no external investor pressure or cliff-unlock events.
3. Meaningful deflationary actions: 32.6M tokens permanently burned (March 2025), emission cuts from 14M → 6M/year, buy-and-burn program active since November 2025.

---

## 2. TEAM ASSESSMENT

### 2.1 Erik Voorhees — Founder & CEO

**Identity:** Real, fully verified. One of the most documented figures in crypto, active since 2011.  
**Confidence:** HIGH

**Verified Career Timeline:**
- 2011: Director of Marketing, BitInstant (early Bitcoin on-ramp)
- 2012: Co-founded SatoshiDice (Bitcoin gambling) and FeedZeBirds
- 2014: Founded ShapeShift AG (Switzerland) — operated until 2021
- 2021: Dissolved ShapeShift, converted it to a DAO via FOX token airdrop
- May 2024: Founded Venice.ai — self-funded, no external investors
- January 2025: Launched VVV token on Base

**Sources:** [The Block](https://www.theblock.co/post/293593/erik-voorhees-founds-generative-ai-platform-venice), [Wikipedia](https://en.wikipedia.org/wiki/Erik_Voorhees), [CoinDesk](https://www.coindesk.com/tech/2024/12/10/erik-voorhees-merging-crypto-and-ai)

---

#### RED FLAG #1 — 2014 SEC Settlement: Unregistered Securities (HIGH confidence | CRITICAL)

Voorhees sold shares in SatoshiDice and FeedZeBirds through public Bitcoin-denominated solicitations ("FeedZeBirds IPO") without registering them as securities. The SEC charged him under Sections 5(a) and 5(c) of the Securities Act of 1933.

**Settlement terms:**
- $15,843.98 in disgorgement + $35,000 penalty ($50,843 total)
- **Five-year ban (2014–2019)** on participating in any unregistered securities issuance in exchange for virtual currency
- Did not admit or deny findings

**Source:** [SEC Order PDF](https://www.sec.gov/files/litigation/admin/2014/33-9592.pdf), [SEC Press Release](https://www.sec.gov/newsroom/press-releases/2014/111)

---

#### RED FLAG #2 — 2018 SEC Investigation: SALT Lending Potential Ban Violation (MEDIUM confidence | HIGH)

While under the five-year ban, Voorhees sat on the board of SALT Lending, which ran a $50M ICO in late 2017. The WSJ reported the SEC was investigating whether Voorhees violated his 2014 ban through SALT board participation. Voorhees denied any violation. He was not named in the SEC's final SALT order, which charged the entity and required refunds. Outcome: SEC penalized SALT; no personal charges against Voorhees in this instance.

**Why it matters:** Pattern of operating in regulatory gray areas with board-level involvement in activities that later drew SEC scrutiny.

**Sources:** [CoinDesk SALT Investigation](https://www.coindesk.com/markets/2018/11/16/erik-voorhees-salt-lending-being-investigated-by-sec-report-says), [Decrypt SALT Settlement](https://decrypt.co/43405/crypto-startup-salt-lending-47-million-ico-sec)

---

#### RED FLAG #3 — 2024 ShapeShift SEC Settlement: $275,000 Penalty (HIGH confidence | HIGH)

ShapeShift AG settled SEC charges for operating as an unregistered national securities exchange and unregistered broker-dealer/clearing agency from August 2014 through early 2021. The $275,000 fine was finalized March 2024.

This is a corporate-level settlement, not a personal charge against Voorhees — but **Voorhees was the sole owner and CEO during the entire violation period.** This is his second SEC settlement in a decade.

**Sources:** [CoinGeek](https://coingeek.com/sec-settles-with-erik-voorhees-shapeshift-over-unregistered-security-sales/), [Crypto Daily](https://cryptodaily.co.uk/2024/03/shapeshift-settles-sec-charges-from-pre-dao-days)

---

#### RED FLAG #4 — ShapeShift Money Laundering: $9M+ in Criminal Proceeds (MEDIUM-HIGH confidence | HIGH)

A 2018 WSJ investigation found that ShapeShift's no-KYC design facilitated conversion of traceable Bitcoin into Monero by North Korean hackers (Lazarus Group-adjacent) and Ponzi operators. Estimates range from $3M (CipherBlade reanalysis) to $9M (WSJ original). Voorhees disputed the magnitude but not the underlying fact that criminal funds moved through the platform. ShapeShift implemented mandatory KYC in fall 2018, losing 95% of its user base and laying off one-third of staff.

**Sources:** [CoinDesk WSJ reanalysis](https://www.coindesk.com/markets/2019/03/20/wsjs-shapeshift-expose-overstated-money-laundering-by-6-million-analysis-says), [CoinGeek](https://coingeek.com/crypto-crime-cartel-erik-voorhees-shapeshift-and-the-anarchists/)

---

#### RED FLAG #5 — PPP Loan Hypocrisy (HIGH confidence | LOW-MEDIUM)

ShapeShift received $1.7M in PPP loans (April 2020) and $1.3M (April 2021) — $3M total, both forgiven — while Voorhees was simultaneously campaigning against government monetary intervention and calling taxation "theft." His public justification was that the government had "stolen many millions from me and ShapeShift." 

This is not a legal violation but is directly relevant to assessing the sincerity of Venice's anti-government, privacy-first branding.

**Source:** [CoinSpice](https://coinspice.io/news/crypto-companies-influencers-defend-taking-million-in-government-coronavirus-ppp-loans/)

---

### 2.2 Teana Baker-Taylor — Co-Founder & COO

**Identity:** Real, fully verified. Joined Venice February 2024.  
**Confidence:** HIGH

**Verified Career:**
- HSBC and Citigroup (traditional finance, roles unspecified)
- Binance UK Director (2020)
- Crypto.com General Manager UK (October 2020)
- Chamber of Digital Commerce, Chief Policy Officer
- Circle VP Policy & Regulatory Strategy EMEA (May 2022 – February 2024)
- CryptoUK Non-Executive Director (ongoing)
- Venice.ai Co-Founder & COO (February 2024 – present)

**Red flags:** None identified. Background is in policy and regulatory engagement, not technical architecture or financial product launches. Her presence adds regulatory credibility to the project. No enforcement history, no controversies found.

**Sources:** [DL News](https://www.dlnews.com/articles/people-culture/former-circle-policy-vp-and-erik-voorhees-launch-ai-app/), [The Org](https://theorg.com/org/venice-ai/org-chart/teana-baker-taylor)

---

### 2.3 Jesse Proudman — Co-Founder & CTO

**Identity:** Real, fully verified. Joined Venice in early 2025.  
**Confidence:** HIGH

**Verified Career (three exits):**
- 2003: Founded Blue Box (managed hosting / private cloud), raised $22M+
- 2015: Sold Blue Box to IBM; served as IBM Distinguished Engineer until 2017
- 2018: Founded Strix Leviathan (crypto algorithmic trading) with Sadie Raney
- 2021: Spun Makara (crypto robo-advisor) from Strix Leviathan
- 2022: Sold Makara to Betterment; became VP Crypto Investing at Betterment
- February 2025: Strix Leviathan acquired by Parataxis Capital (NY crypto hedge fund)
- 2025: Co-Founder & CTO, Venice.ai

**Red flags:** None identified. Three legitimate exits, no SEC history, strong builder track record. His crypto background (algorithmic trading) means he has operated in high-risk asset classes, but no personal misconduct found.

**Sources:** [GeekWire](https://www.geekwire.com/2025/private-and-uncensored-ai-seattle-tech-vet-joins-new-startup-taking-on-ai-giants-with-a-crypto-twist/), [Crunchbase](https://www.crunchbase.com/person/jesse-proudman)

---

### 2.4 Broader Team

- **Team size:** ~20 employees total; approximately 6 in core engineering roles
- **GitHub:** The [veniceai GitHub org](https://github.com/veniceai) explicitly hides its member list. Public repos include `api-docs`, `venice-cli`, `venice-mcp-server`, `x402-client` (crypto micropayments), `slackbot`, and `venice-router` (Python). No named engineers are attributable from public commit history.
- **RED FLAG (LOW-MEDIUM):** 6 engineers supporting 900K+ users and building a two-token DeFi system is an extraordinary ratio, raising questions about whether user/activity claims are exaggerated or the platform is significantly more automated than it appears.

---

### 2.5 What Could NOT Be Verified (Team)

- Individual engineer identities and GitHub contribution histories — hidden by org settings
- Employment claims for engineers below the three named co-founders
- Whether any other team members have undisclosed crypto histories

---

## 3. THIRD-PARTY CONSENSUS

### 3.1 Audit & Security Posture

**Auditor: Trust Security**

- The VVV smart contracts were audited by [Trust Security](https://www.trust-security.xyz). This is the only audit firm identified across all research sources.
- The audit URL `trust-security.xyz/venice-ai-audit` returned a **404 error** when accessed — the full report is not publicly accessible.
- No audit findings (critical/high/medium/low counts) are available in any indexed source.
- **No CertiK, Trail of Bits, OpenZeppelin, or Consensys Diligence audit found.**
- **No independent privacy audit exists.** A community request on Venice's own Featurebase platform has accumulated 365 votes and has remained "In Review" for approximately one year with no team response or timeline.

**RED FLAG (HIGH): The full audit report is inaccessible to the public.** Reputable DeFi projects publish complete audit PDFs openly. The absence of a public report makes it impossible to verify what was reviewed, what was found, or whether findings were remediated.

**Update (positive):** In 2025-2026, Venice integrated with NEAR AI to implement **Trusted Execution Environments (TEEs)** for verifiable private inference. NEAR AI's blog confirmed this integration enables cryptographic remote attestation — a user can verify that models run inside a genuine hardware enclave. This is a meaningful privacy upgrade over self-attested claims, though it only covers models run in the TEE mode.

**Sources:** [NEAR AI Blog](https://near.ai/blog/venice-is-now-verifiably-private-with-near-ai), [Venice Featurebase Privacy Audit Request (365 votes)](https://featurebase.venice.ai/p/independent-privacy-audit), Trust Security (404 at time of access)

---

### 3.2 Independent Media Coverage

| Publication | Coverage | Nature |
|---|---|---|
| The Defiant | Multiple articles (launch, valuation surge, Aerodrome incident) | Neutral-to-positive; covered insider trading incident factually |
| CoinDesk | Insider trading incident, VVV crash coverage | Critical; covered 50% crash and allegations |
| The Block | Launch coverage, burn article, Aerodrome suspension | Neutral |
| Rekt News | **None found** | No exploits or hacks documented |
| DL News | Team profile article | Neutral |
| Decrypt | Overview and resource article | Neutral |
| Infosecurity Magazine | Cybercrime tool coverage | Critical/negative |
| CPO Magazine | "Black hat hackers' first brand-name AI chatbot" | Strongly negative |
| KnowBe4 | "New unrestricted AI tool for cybercrime" | Strongly negative |

---

### 3.3 Cybersecurity — Platform Used as a Criminal Tool (HIGH confidence | CRITICAL concern)

This section deserves prominent placement. Six independent cybersecurity organizations have documented Venice.ai being actively adopted in underground criminal forums:

- **Certo Software:** Venice generates functional keyloggers, ransomware for Windows 11, Android spyware, and phishing emails on demand. [Source](https://www.certosoftware.com/insights/unleashed-ai-hackers-embrace-unrestricted-chatbot-venice-ai/)
- **Infosecurity Magazine:** Raises broad cybersecurity alarms over "uncensored AI tool." [Source](https://www.infosecurity-magazine.com/news/uncensored-ai-tool-cybersecurity/)
- **KnowBe4:** Labels it "new unrestricted AI tool that can assist in cybercrime." [Source](https://blog.knowbe4.com/new-unrestricted-ai-tool-can-assist-in-cybercrime)
- **CPO Magazine:** "Black hat hackers' first brand-name AI chatbot." [Source](https://www.cpomagazine.com/cyber-security/black-hat-hackers-have-its-first-brand-name-ai-chatbot-in-venice-ai/)
- **CyberNews:** Documented generation of "sophisticated cyberattacks" on demand. [Source](https://cybernews.com/cybercrime/unrestricted-chatbot-enables-sophisticated-cyberattacks/)
- **GBHackers:** Corroborated findings from Certo. [Source - CyberPress](https://cyberpress.org/blackhat-ai-tool-venice-ai-enables-attackers/)

Venice is actively promoted in hacking forums as cheaper than WormGPT/FraudGPT at $18/month. The platform's reasoning traces show it was configured to respond to "any user query, even if offensive or harmful."

**Venice's legal defense:** Terms of Service place all liability on users and cap Venice's liability at amounts paid in the prior 12 months. This insulates the company legally but creates a non-trivial law enforcement target profile — particularly relevant given Voorhees's existing regulatory history.

**Why this matters for VVV:** A regulatory crackdown on Venice.ai as a cybercrime-enabling platform could devastate token value overnight. This risk is not hypothetical — it is documented, ongoing, and growing.

---

### 3.4 Community Sentiment

- **OKX published an article titled "Is Venice AI Legit? A look at whether VVV is real or a scam"** — the fact that this question is SEO-generating content confirms widespread skepticism is present in the market.
- Reddit threads from r/CryptoCurrency, r/DeFi, r/ethfinance were not surfaced in indexed searches (Reddit's search indexing is notoriously weak for critical posts). Direct platform investigation would be required.
- No meaningful governance forum discussion (no DAO = no forum by design).
- Market has spoken: **-82% from ATH** before recent 152% recovery to ~$8.53, still leaving investors who bought near launch significantly underwater.

---

## 4. ON-CHAIN FINDINGS

### 4.1 Smart Contract Analysis

**Contract address:** `0xacfE6019Ed1A7Dc6f7B508C02d1b04ec88cC21bf` on Base  
**Source code:** Verified on BaseScan (Solidity v0.8.26, Solmate ERC20 + `Owned` library)  
**Source:** [BaseScan](https://basescan.org/token/0xacfE6019Ed1A7Dc6f7B508C02d1b04ec88cC21bf)

**Critical findings from contract review:**

- **`mint()` function:** Callable by the contract owner alone — no timelock, no multisig requirement disclosed in the base contract. **GoPlus security scanner flags this contract** for owner-controlled mint capabilities.
- **`transferOwnership()`:** Owner can reassign control to any address with no delay.
- No `pause()` function identified in the base ERC-20 contract.
- Constructor minted 100M tokens to treasury address `0x2D8CB8DC596daD0e1E34E2042E7ae6Df93B11524` at deployment.
- **On-chain total supply (April 2026): ~113.23M VVV** — confirms emissions above genesis 100M have already occurred as designed.
- **Circulating supply:** ~45.57M (~40% of total outstanding) — heavy portion still held by team/treasury.

**RED FLAG (HIGH): Owner-controlled mint with no disclosed timelock or multisig.** While the emission schedule is publicly stated, the mechanism allows unilateral, unconstrained minting. The alleged post-Coinbase-listing mint of 1M tokens (see Section 4.3) demonstrates that this capability has allegedly been exercised unexpectedly.

---

### 4.2 Token Distribution Analysis

**Genesis supply:** 100,000,000 VVV

| Allocation | % | Amount | Vesting Status |
|---|---|---|---|
| Venice.ai treasury | 35% | 35M | Largest single controller |
| User airdrop | 25% | 25M | 32.6M burned unclaimed (March 2025) |
| AI protocol partners | 25% | 25M | Distributed to Virtuals, Aerodrome, Clanker, etc. |
| Team | 10% | 10M | 25% unlocked at TGE; 75% streaming over 24 months (ends ~Jan 2027) |
| Incentive Fund | 10% | 10M | Ecosystem growth |
| Liquidity | 5% | 5M | Deployed on Aerodrome |

**Annual emissions:** Started 14M/year → cut to 8M → cut 25% to 6M/year (effective February 10, 2026). Split between stakers and Venice.ai based on a "Utilization Rate" formula — **Venice.ai company itself receives a portion of emissions**, creating a structural conflict of interest.

**Team vesting risk:** ~7.5M team tokens remain unvested as of April 2026 (streaming through ~January 2027). At current price ($8.53), this represents ~$64M in potential sell pressure over the next 9 months.

**Concentration risk:** Venice.ai controls 35% of genesis supply through the treasury plus receives ongoing emission rewards. Combined with team tokens, the company influences up to ~50% of supply with no token-holder governance check on how it is used.

---

### 4.3 The Insider Trading & Secret Minting Incidents

#### Confirmed: Aerodrome Insider Trading at Launch

On January 27, 2025, two Aerodrome Finance contributors bought VVV immediately after launch using advance knowledge of the launch parameters. Their $50K position became $1M in under one hour. Aerodrome's internal monitoring flagged the activity within 30 minutes; contributors were suspended within 3 hours. Aerodrome disclosed the incident publicly; Erik Voorhees praised Aerodrome's transparency.

**Assessment (HIGH confidence):** This incident confirms that pre-launch coordination existed between Venice and Aerodrome contributors, and that information asymmetry was exploited at launch. The token crashed 50% in the days following.

**Sources:** [Coinspeaker](https://www.coinspeaker.com/aerodrome-finance-suspends-contributors-over-insider-trading-during-venices-vvv-token-launch/), [CoinDesk](https://www.coindesk.com/markets/2025/01/29/venice-ai-s-vvv-drops-50-as-insider-trading-concerns-swirl), [The Block](https://www.theblock.co/post/337521/two-contributors-suspended-from-venices-vvv-token-launch-on-aerodrome)

---

#### Disputed: Secret Post-Listing Mint of 1,000,000 VVV (~$5.79M)

Crypto analyst Amir Ormu alleged that following the Coinbase listing, the Venice team secretly minted 1M additional VVV tokens from a new wallet sharing signers with Venice's multisig treasury (`0xb6e08047320b4b4d943d7f1363776dddc6f4aa66`) and sold ~$450,000 worth immediately via CowSwap (chosen for lower DexScreener visibility). A second analyst named "Freedom" corroborated that 25% of the 10% unvested team supply was distributed days before the public launch. Ormu's full allegation was that insiders dumped **$10.2M worth of VVV** immediately following launch.

**Voorhees's response:** "The genesis addresses were all obvious, and everything is on-chain and transparent. The announcement blog stated terms of the token clearly. Approximately 2.5% of supply could be sold. A fraction of that 2.5% was actually sold."

**Assessment (MEDIUM confidence — UNRESOLVED):** Voorhees's response addressed the supply cap available for sale but **did not directly deny or address the 1M post-listing mint allegation** or the CowSwap routing choice. The fact that the Venice team itself holds an owner-controlled `mint()` function makes this allegation technically plausible and warrants on-chain verification. These are allegations, not confirmed facts — but the lack of a direct denial is notable.

**Sources:** [Bitcoin.com](https://news.bitcoin.com/erik-voorheess-venice-token-faces-pump-and-dump-allegations/), [CoinGape](https://coingape.com/trending/did-venice-team-dump-5-7m-tokens-after-coinbase-listing/), [BitcoinEthereumNews](https://bitcoinethereumnews.com/tech/did-venice-team-dump-5-7m-tokens-after-coinbase-listing/)

---

#### Wintermute Pre-Listing DEX Selling (MEDIUM-HIGH confidence | HIGH concern)

On-chain analysis indicated Wintermute (market maker) and Kbit received 5.5% of total VVV supply pre-launch. Wintermute sold $1.4M before any CEX listing (via DEXs); Kbit deposited $8.8M to Coinbase at/around listing. VVV peaked at $19.38 hours post-launch, then crashed 63% to $2.44 within two weeks.

This behavior — market maker selling on DEXs before any exchange listing — is structurally indistinguishable from a coordinated market maker exit. While Voorhees stated that "approximately 2.5% of supply could be sold" and that disclosure was upfront, the Wintermute pre-listing DEX selling pattern was not addressed in any public statement found.

**Source:** [Bitcoin.com](https://news.bitcoin.com/erik-voorheess-venice-token-faces-pump-and-dump-allegations/)

---

### 4.4 DEX Liquidity & Wash Trading Signals

- Primary trading on Aerodrome on Base, with secondary markets on Uniswap (Base) and Coinbase
- A "VVV" token on Solana/Raydium at near-zero price is almost certainly a **scam copycat token** — retail investors are being misled by name squatting
- 24h volume reported at $6.9M–$47.5M range across sources — significant variance suggesting potential wash activity, though no formal forensic wash trading analysis has been published
- **Assessment:** Wash trading is unconfirmed but pattern warrants investigation. The extreme volume range without a corresponding catalyst is unusual.

---

### 4.5 Deflationary Actions (Positive)

| Action | Tokens Removed | Timing |
|---|---|---|
| Airdrop unclaimed burn | 32.6M tokens (~$100M at time) | March 2025 |
| Buy-and-burn program | ~1.1M additional tokens | Nov 2025 – present |
| Emission reduction (14M → 8M/yr) | Ongoing | Mid-2025 |
| Emission reduction (8M → 6M/yr) | Ongoing | February 10, 2026 |
| **Total burned** | **~33.7M tokens (~42% of original supply)** | As of March 2026 |

This is the most credible positive signal in the on-chain data. A project executing non-trivial burns ($100M+ of its own tokens) is exhibiting behavior inconsistent with pure exit-scam intent.

---

## 5. TOKENOMICS & SUSTAINABILITY ANALYSIS

### Is the Model Sustainable?

**Real product layer (positive):**
- 900,000+ total users, 50,000 daily active users (self-reported, unaudited)
- Revenue from pro subscriptions and API fees funds buy-and-burn
- Uses open-source models (Llama, Qwen, Stable Diffusion) — no proprietary model cost
- Compute via Akash Network and partner GPU providers — no significant capex required

**Circular economy risks:**
- The 18% APY staking yield is **paid in VVV emissions** — classic "print token to pay stakers" dynamic. Sustainable only if token price holds or new buyers continuously enter.
- Venice.ai company receives emission rewards via the "Utilization Rate" mechanism — the operator is also a major emission recipient, which is a structural conflict of interest.
- **DIEM token (launched August 2025):** Represents $1/day of API credit in perpetuity. This is an uncollateralized, perpetual obligation. If Venice closes or compute costs rise, DIEM holders have no on-chain recourse — the "perpetual" claim rests entirely on trusting Venice as a going concern.
- Annual emission at 6M/year against ~45.57M circulating supply = ~13.2% annual dilution — meaningful for holders even after cuts.
- No token-holder governance exists. Emission cuts, burn parameters, DIEM launch, partnership decisions — **all made unilaterally** by the Venice team. VVV is explicitly NOT a governance token.

**Overall sustainability verdict:** Semi-sustainable. The real product underpinning distinguishes this from pure Ponzi schemes, but the token value is heavily dependent on: (a) continued user growth driving buy-and-burn revenue, (b) the team continuing to execute emission cuts, and (c) no regulatory action targeting Venice directly. If the user growth loop reverses, no structural floor exists.

---

## 6. COMPARATIVE ANALYSIS

### Patterns Shared with Known Problematic Token Launches

| Pattern | Venice VVV | Characteristic of... |
|---|---|---|
| Launch-day ATH immediately followed by crash | YES — ATH on Day 1, -50% within days | Insider/market maker coordinated exit |
| Team controls 35%+ of supply | YES | High-risk concentration |
| No token-holder governance | YES | Fully centralized; no accountability |
| Owner-controlled mint function | YES | Rugpull technical capability (not proof of intent) |
| Staking yield paid in native emissions | YES | Circular token economy (Wonderland, OlympusDAO pattern) |
| Market maker pre-listing DEX selling | ALLEGED | Known pattern in coordinated token exits |

### Key Differences from Confirmed Scams

| Factor | Venice VVV | Full Rug/Ponzi |
|---|---|---|
| Real product with users | YES | NO (Wonderland, Celsius, Terra) |
| Founder's real identity | YES | Often anonymous |
| Self-funded by founder | YES | Usually extractive from investors |
| Large token burns executed | YES | Never |
| Meaningful deflationary actions | YES | Typically reversed or fake |

**Conclusion:** Venice is NOT a rug pull in the traditional sense. The product is real, the team is identifiable, and deflationary actions are genuine. However, the **token launch** bears multiple structural hallmarks of coordinated insider benefit: pre-listing market maker selling, confirmed Aerodrome insider trading, and unresolved secret mint allegations — all consistent with insiders having captured disproportionate value at retail expense.

The circular staking economy (18% yield paid in emissions) shares structural DNA with Wonderland/OlympusDAO — not because Venice is a Ponzi but because the token value is partially self-referential. This is a meaningful risk at scale.

---

## 7. RED FLAGS REGISTER

| # | Severity | Red Flag | Evidence | Source | Why It Matters |
|---|---|---|---|---|---|
| 1 | CRITICAL | Aerodrome insider trading confirmed at launch | Contributors $50K→$1M in <1hr; suspended within 3 hours | CoinDesk, Coinspeaker, The Block | Confirms information asymmetry was exploited at launch; VVV crashed 50% |
| 2 | CRITICAL | Platform documented as cybercrime tool | 6 independent security firms; active promotion on hacking forums | Certo, Infosecurity, KnowBe4, CPO Mag, CyberNews, GBHackers | Regulatory action risk; law enforcement target profile |
| 3 | HIGH | Founder: two direct SEC settlements in a decade | 2014 personal settlement; 2024 ShapeShift corporate settlement | SEC EDGAR, CoinGeek, Crypto Daily | Pattern of regulatory friction; VVV is third token-adjacent event with insider benefit allegations |
| 4 | HIGH | Owner-controlled mint function; GoPlus flags this | BaseScan source verified; GoPlus scanner flags | BaseScan, GoPlus | Enables unconstrained supply expansion; alleged to have been used post-Coinbase listing |
| 5 | HIGH | Unresolved allegation: 1M secret post-listing mint (~$5.79M) | On-chain analysis by Amir Ormu; corroborated by second analyst "Freedom" | Bitcoin.com, CoinGape | Voorhees did not directly deny or address; technically enabled by mint() function |
| 6 | HIGH | Wintermute pre-listing DEX selling ($1.4M before any CEX) | On-chain forensics; Kbit deposited $8.8M to Coinbase at listing | Bitcoin.com pump/dump allegations | Structurally indistinguishable from coordinated market maker exit |
| 7 | HIGH | Zero token-holder governance | Explicitly stated: VVV is not a governance token | Venice official docs | All protocol decisions (emission cuts, DIEM launch, burns) made unilaterally; no accountability |
| 8 | HIGH | -82% drawdown from ATH | Price data: $22.45 peak → ~$3.84 trough | CoinGecko, CoinMarketCap | Retail investors heavily underwater despite real product |
| 9 | MEDIUM | Full audit report not publicly accessible | Trust Security audit URL returns 404; no PDF found anywhere | Trust Security site (404) | Cannot verify what was audited, what was found, or what was remediated |
| 10 | MEDIUM | No independent privacy audit after 1+ year community request | 365 votes on Featurebase; "In Review" for 12+ months with no response | Venice Featurebase | Privacy claims rest on architectural assertions and trust |
| 11 | MEDIUM | Team vesting ~7.5M tokens through Jan 2027 | Tokenomics docs; 75% of team allocation over 24 months | Venice blog, The Block | ~$64M in potential sell pressure at current prices over next 9 months |
| 12 | MEDIUM | Staking yield paid in VVV emissions | 18% APY from token printing | Venice tokenomics | Circular economy; yield sustainability depends on new buyers |
| 13 | MEDIUM | DIEM is an uncollateralized perpetual obligation | $1/day API credit "in perpetuity" — no on-chain collateral | Venice DIEM blog | Venice closure or cost increases leave DIEM holders with no recourse |
| 14 | MEDIUM | Venice.ai company is a major emission recipient | Utilization Rate mechanic | Venice tokenomics | Operator and emission recipient creates conflict of interest |
| 15 | MEDIUM | Fragmented DEX liquidity; high volume variance ($6.9M–$47.5M) | DEX Screener pool data | DEX Screener | Potential wash trading signal; unconfirmed but unusual |
| 16 | LOW-MEDIUM | ~6 engineers for 900K+ users | Team size vs. claimed scale | NFTgators, GeekWire | Either platform is more automated than presented or user figures are inflated |
| 17 | LOW | Solana copycat "VVV" token on Raydium | Near-zero price "VVV" pair on Raydium | DEX Screener | Retail name-squatting attack actively targeting Venice's brand |
| 18 | LOW | No public GitHub member list | veniceai GitHub org hides members | GitHub | Prevents independent developer vetting |

---

## 8. UNRESOLVED QUESTIONS

1. **Was the 1M post-Coinbase-listing mint real?** On-chain data is publicly available on BaseScan but was not independently verified in this investigation. Someone with Dune Analytics access could confirm or refute this definitively. This is the most material unresolved question.

2. **Does the Trust Security audit exist and what did it find?** The 404 URL must be resolved — either Venice should publish the full report or explain why it is inaccessible.

3. **What are Venice's actual user and revenue numbers?** All user figures (900K users, 50K DAU) are self-reported with no independent audit. Revenue funding the buy-and-burn is undisclosed.

4. **Is Voorhees personally named in any pending regulatory action related to VVV?** Given his history, this cannot be dismissed as implausible. No current action was found but absence of evidence ≠ evidence of absence.

5. **Does the TEE/NEAR AI privacy integration cover all inference, or only specific models?** The current integration appears to be opt-in per model, not platform-wide. The scope of cryptographic privacy guarantees is unclear.

6. **What are the actual wash trading volumes on Aerodrome?** DEX volume data shows extreme variance ($6.9M–$47.5M) without clear correlation to external catalysts. Independent wash trading forensics are needed.

7. **Who are the 25M "AI protocol partner" airdrop recipients and what have they done with their tokens?** The allocation to Virtuals, Aerodrome, Clanker, Aixbt and others creates a distributed insider class whose selling behavior has not been tracked.

---

## 9. FINAL RISK MATRIX

| Dimension | Risk Rating | Confidence |
|---|---|---|
| Platform (AI service) | LOW-MEDIUM | HIGH |
| Token (VVV) for investors | HIGH | HIGH |
| Team integrity (Voorhees) | MEDIUM-HIGH | HIGH |
| Team integrity (Baker-Taylor, Proudman) | LOW | HIGH |
| Smart contract technical risk | MEDIUM | MEDIUM |
| Audit transparency | HIGH | HIGH |
| Privacy claims | MEDIUM (improving via TEE) | MEDIUM |
| Regulatory exposure (founder history) | MEDIUM-HIGH | HIGH |
| Regulatory exposure (cybercrime facilitation) | HIGH | HIGH |
| Tokenomics sustainability | MEDIUM | MEDIUM |
| Governance centralization | HIGH | HIGH |
| Market conduct at launch | HIGH | HIGH |

---

## SOURCES

- [SEC 2014 Order — Voorhees (PDF)](https://www.sec.gov/files/litigation/admin/2014/33-9592.pdf)
- [ShapeShift 2024 SEC Settlement — CoinGeek](https://coingeek.com/sec-settles-with-erik-voorhees-shapeshift-over-unregistered-security-sales/)
- [VVV Insider Dump Allegations — Bitcoin.com](https://news.bitcoin.com/erik-voorheess-venice-token-faces-pump-and-dump-allegations/)
- [VVV Coinbase Listing Dump Allegations — CoinGape](https://coingape.com/trending/did-venice-team-dump-5-7m-tokens-after-coinbase-listing/)
- [CoinDesk — VVV Drops 50% on Insider Trading Concerns](https://www.coindesk.com/markets/2025/01/29/venice-ai-s-vvv-drops-50-as-insider-trading-concerns-swirl)
- [Aerodrome Suspensions — Coinspeaker](https://www.coinspeaker.com/aerodrome-finance-suspends-contributors-over-insider-trading-during-venices-vvv-token-launch/)
- [Aerodrome Suspensions — The Block](https://www.theblock.co/post/337521/two-contributors-suspended-from-venices-vvv-token-launch-on-aerodrome)
- [VVV Token Launch — The Block](https://www.theblock.co/post/337196/erik-voorhees-ai-platform-venice-token-ethereum-layer-2-base)
- [VVV Airdrop Burn — The Block](https://www.theblock.co/post/345912/venice-airdrop-ends-100-million-usd-unclaimed-vvv-tokens-burned)
- [VVV Tokenomics — Venice Blog](https://venice.ai/blog/introducing-the-venice-token-vvv)
- [DIEM Token Introduction — Venice Blog](https://venice.ai/blog/introducing-diem-as-tokenized-intelligence-the-next-evolution-of-vvv)
- [VVV Contract — BaseScan](https://basescan.org/token/0xacfE6019Ed1A7Dc6f7B508C02d1b04ec88cC21bf)
- [VVV — CoinGecko](https://www.coingecko.com/en/coins/venice-token)
- [VVV — CoinMarketCap](https://coinmarketcap.com/currencies/venice-token/)
- [Cybersecurity — Certo Software](https://www.certosoftware.com/insights/unleashed-ai-hackers-embrace-unrestricted-chatbot-venice-ai/)
- [Cybersecurity — Infosecurity Magazine](https://www.infosecurity-magazine.com/news/uncensored-ai-tool-cybersecurity/)
- [Cybersecurity — CPO Magazine](https://www.cpomagazine.com/cyber-security/black-hat-hackers-have-its-first-brand-name-ai-chatbot-in-venice-ai/)
- [Cybersecurity — KnowBe4](https://blog.knowbe4.com/new-unrestricted-ai-tool-can-assist-in-cybercrime)
- [Cybersecurity — CyberNews](https://cybernews.com/cybercrime/unrestricted-chatbot-enables-sophisticated-cyberattacks/)
- [Privacy Audit Request (365 votes) — Venice Featurebase](https://featurebase.venice.ai/p/independent-privacy-audit)
- [NEAR AI Privacy Integration — NEAR AI Blog](https://near.ai/blog/venice-is-now-verifiably-private-with-near-ai)
- [Jesse Proudman Background — GeekWire](https://www.geekwire.com/2025/private-and-uncensored-ai-seattle-tech-vet-joins-new-startup-taking-on-ai-giants-with-a-crypto-twist/)
- [Teana Baker-Taylor — DL News](https://www.dlnews.com/articles/people-culture/former-circle-policy-vp-and-erik-voorhees-launch-ai-app/)
- [Erik Voorhees — Wikipedia](https://en.wikipedia.org/wiki/Erik_Voorhees)
- [SALT Investigation — CoinDesk](https://www.coindesk.com/markets/2018/11/16/erik-voorhees-salt-lending-being-investigated-by-sec-report-says)
- [ShapeShift Money Laundering — CoinDesk](https://www.coindesk.com/markets/2019/03/20/wsjs-shapeshift-expose-overstated-money-laundering-by-6-million-analysis-says)
- [OKX — Is Venice AI Legit?](https://www.okx.com/en-us/learn/is-venice-ai-legit-vvv-token-overview)
- [VVV 152% Surge — Phemex](https://phemex.com/blogs/venice-token-vvv-decentralized-ai)
- [Privacy Architecture — RunThePrompts](https://runtheprompts.com/resources/venice-ai-info/is-venice-ai-private/)
- [GoPlus Token Security Scanner](https://console.gopluslabs.io/token-security)
- [Venice GitHub Org](https://github.com/veniceai)

---

*This report was produced under adversarial research methodology. All verified claims are independently sourced. Unverified allegations are explicitly labeled. Confidence levels reflect evidence quality, not outcomes.*
