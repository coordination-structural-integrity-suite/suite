---
title: CROSS - Common Reporting Outcome Standards Schema - Worked Examples
version: 0.2.0
date: 2026-05-14
license: CC0
status: Working draft. Companion worked examples to CROSS-common-reporting-outcome-standards-schema-0_2_0.md. Supersedes version 0.1.0.
---

# CROSS - Common Reporting Outcome Standards Schema - Worked Examples

Version 0.2.0 | 2026-05-14 | CC0

---

## Introduction

These examples illustrate CROSS criteria through real grant evaluation cases. Each case identifies the criterion illustrated, states the finding from evaluation, specifies the CROSS assessment, and shows what a conformant approach would have looked like. Cases are drawn from Octant Epoch 12 grant evaluations conducted in May 2026.

All six cases in this edition are drawn from rounds operating in change-obligation mode or from the boundary between build and change obligation. Cases illustrating build-obligation and retroactive obligation rounds will be added as examples from those program types are evaluated and documented. The entry specification gate findings in these cases use the change-obligation vocabulary (FROM state classification) unless otherwise noted.

Each case can be read independently. The recommendation vocabulary throughout is: Fund / Fund with conditions / Do not fund.

---

## Case 1: Beneficiary Validation Failure

**Project:** Mushee Allocate
**Ask:** \$6,330
**Outcome:** Do not fund
**Criterion illustrated:** Coordinating party engagement and beneficiary validation; entry specification gate

### The Application

Mushee Allocate was proposed as a claim-and-allocation portal for Ethereum and Ethereum Virtual Machine-compatible chains. The stated workflow: a grant administrator creates a campaign, adds recipient wallet addresses, sets individual allocations, and publishes a claim page. Recipients visit the page, connect their wallet, and pull their tokens. The application framed the problem as grant distribution coordination requiring manual spreadsheets with no transparent on-chain record. The ask was \$6,330.

### The CROSS Finding

The FROM state named in the application is internally coherent: grant teams routinely distribute tokens in batches and the mechanics of moving tokens from a multisig to dozens of recipients is error-prone. A specific problem is visible. At that level, the entry specification gate passes: a condition is named in a defined operational context.

The application fails at the beneficiary validation dimension. Beneficiary validation requires that the FROM state be confirmed by parties outside the applicant's control, and that the applicant have named existing alternatives and explained why those alternatives do not address the stated population's specific need.

An independent check found that Hedgey Finance already addresses the stated problem: administrators upload a comma-separated values file of recipient addresses and allocations, Hedgey Finance generates a Merkle-tree-based claim, recipients connect a wallet and claim from a custom link, and a dashboard tracks participation rates and token volumes in real time. Hedgey Finance is deployed, audited, used by Arbitrum and other protocols, and free to use. Splits, Coordinape, and Drips Network fill adjacent parts of the same workflow.

The application did not name Hedgey Finance or any of these tools. This is a beneficiary validation failure in its most direct form: the applicant proposed a solution without first establishing that existing solutions do not serve the stated population. The FROM state exists as a claim but was not validated against the competitive landscape, and the tools that already fill the described gap are production-grade.

A second dimension failed: product readiness. The closest analogue to Mushee Allocate found in any public repository was ClaimFlowOS, committed in a single upload on April 12, 2026, two days after the Octant Epoch 12 application window opened. The repository's own README states: "This is a polished frontend demo with interactive mock workflows for product presentation, grant applications, and investor demos." The repository contains no smart contract code, no wallet connection logic, and no backend. The demo was produced to support the grant application rather than to represent genuine product progress. No Ethereum testnet deployment was found, no smart contract exists in any public repository, and the Mushee Allocate domain was unreachable at time of evaluation.

### CROSS Assessment

Entry specification gate: passes (a specific condition is named in a defined context).

Beneficiary validation: fails. The FROM state was not validated with intended beneficiaries and the applicant did not name existing alternatives, which is a required step under the coordinating party engagement and beneficiary validation dimension.

Product readiness: the single-commit demo explicitly self-described as built for grant applications does not constitute evidence of a working product. This is an institutional capacity finding, not a gate finding, but it reinforces the do not fund recommendation.

### What a Compliant Approach Would Have Looked Like

A conformant application would have named Hedgey Finance, Splits, and Coordinape, explained specifically why each does not address the applicant's stated population's need, and cited at least one source outside the applicant's control confirming that a gap remains. For example: evaluation results from grant programs using Hedgey Finance identifying specific limitations, interviews with grant administrators conducted before writing the application, or documentation of a problem that Hedgey Finance's architecture cannot accommodate.

The conformant application would then have specified what Mushee Allocate does that Hedgey Finance cannot, in the same operational terms used to describe the FROM state. If no such differentiation exists, the gap does not exist and the application should not proceed.

---

## Case 2: Indicator Specification Failure

**Project:** mev-commit (Primev)
**Ask:** \$100,000
**Outcome:** Do not fund
**Criterion illustrated:** Operational definition; Integrity

### The Application

mev-commit is a peer-to-peer network where block builders on Ethereum issue cryptoeconomic commitments ("preconfirmations") before a block is proposed. When a builder commits to including a transaction in the next block, the commitment is backed by slashable stake: if the builder breaks it, they lose collateral. Validators opt into this system by agreeing to accept only blocks from mev-commit builders. The protocol is live on Ethereum mainnet with 7,835 opted-in validators and \$116.5M in economic security across Symbiotic vaults. The application asked for \$100,000 toward an encrypted mempool milestone using the LUCID design and Shutter Network cryptography. The application's headline block coverage claim was "10-20% of Ethereum blocks."

### The CROSS Finding

The headline outcome indicator, "10-20% of Ethereum blocks," is an indicator name, not an operational definition. The claim does not specify which blocks count (mainnet only? testnets? any time window?), the measurement methodology, how partial inclusion is handled, or what data source an independent reviewer would use to replicate the figure.

An independent check using MEV-Boost relay data and a September 2025 research paper showed: single-day peak block coverage of 11.33% on August 20, 2025; a 5% sustained 24-hour figure documented in that period; and a February 2026 Dune dashboard showing 3.13% block value captured. The application presents "10-20%" as the current state of coverage; it is a cherry-picked range anchored to a single-day peak from nine months before the application date. Sustained coverage at time of application was 3-5%. The claim overstates current coverage by a factor of 3-6x.

This is an indicator specification failure under two sub-requirements. First, no operational definition exists: the indicator as stated does not meet the CROSS requirement for inclusion criteria, exclusion criteria, unit of analysis, or edge case determination. Second, no construction and aggregation methodology was provided: there is no named data source, no time window, and no replication path for an independent reviewer.

The integrity dimension also fails. All performance metrics in the application are sourced from applicant-controlled systems: the Primev validator dashboard, the Primev documentation, and the KarmaGAP profile created the same day as the application. No named independent corroboration was provided for the headline coverage claim. For a claim of this magnitude in a live infrastructure context, applicant-controlled data without independent corroboration does not satisfy the integrity standard.

A third legibility failure reinforces the finding: venture capital backing from a16z CSX, HashKey Capital, and Figment Capital was not disclosed in the application, despite concurrent funding disclosure being a required field for all CROSS-conformant applications.

### CROSS Assessment

Indicator specification: fails. The headline indicator is a name without an operational definition, a construction methodology, or a replication path.

Integrity: fails. All performance evidence is sourced from applicant-controlled systems. The independent data that exists contradicts the headline claim.

Concurrent funding disclosure: incomplete. Venture capital backing from named investors was not disclosed.

Entry specification gate: passes on the encrypted mempool milestone specifically (the FROM state for that milestone is that Ethereum's pre-consensus layer lacks a privacy-preserving transaction ordering mechanism, which is a specific, verifiable condition). The gate failure is not at the entry specification level; it is at the indicator specification and integrity levels, which are rigor-tier concerns.

### What a Compliant Operational Definition Would Have Looked Like

A conformant operational definition for the "blocks" indicator would specify:

Indicator name: Proportion of Ethereum mainnet blocks per calendar week with at least one mev-commit preconfirmation included.

Inclusion criteria: a block counts if it was proposed on Ethereum mainnet (chain ID 1) in the specified time window and contains at least one transaction whose inclusion was secured through a verified mev-commit preconfirmation commitment, as evidenced by a slashing record in the mev-commit settlement chain (chain ID 8855).

Exclusion criteria: testnet blocks, Ethereum testnets, blocks on other Ethereum Virtual Machine chains, and blocks containing transactions routed through mev-commit relays but without a recorded commitment are excluded.

Unit of analysis: individual Ethereum mainnet block.

Construction methodology: weekly block count sourced from a named public MEV-Boost relay data application programming interface (such as Relayscan or MEV-Boost.org), with preconfirmation matches verified against the mev-commit settlement chain. The data source and query are named so an independent reviewer can replicate them.

Baseline: as of February 2026, 3.13% of weekly Ethereum mainnet block value captured (source: named Dune dashboard uniform resource locator, accessed date).

Target: 10% of weekly Ethereum mainnet blocks with at least one preconfirmation by end of grant period.

Time window: 12-week rolling average at the time of each milestone report.

---

## Case 3: Privacy-Sensitive Context Accommodation

**Project:** MoaV (Mother of All VPNs)
**Ask:** \$30,000
**Outcome:** Fund with conditions
**Criterion illustrated:** Privacy and data sensitivity accommodation

### The Application

MoaV is a self-hosted censorship circumvention stack that deploys 16 or more distinct anti-censorship protocols from a single Docker Compose command. A server operator runs one installation script and the stack comes up with protocols spanning fundamentally different technical approaches: stealth Transport Layer Security proxies, QUIC-based tunneling, WireGuard variants, Domain Name System tunneling, content delivery network-fronted routing, and Telegram MTProxy. The protocol diversity is the core design argument: no single protocol survives every censorship environment. The project integrates with MahsaNet, which distributes operator-donated configurations to approximately 2 million users in Iran, Russia, and Myanmar. MoaV was built by Shayan Eskandari, a former ConsenSys Diligence security engineer with a 32-audit career in Ethereum smart contract security. The project launched January 28, 2026, weeks after Iran's January 8 shutdown.

### The CROSS Finding

MoaV ships with zero telemetry by design. This is the correct architectural choice for a tool serving users in high-risk jurisdictions: any telemetry collection that identifies user location, usage patterns, or protocol preferences creates data that an adversary could use to surveil, identify, or arrest the people the tool exists to protect. The absence of telemetry is a safety property, not a reporting gap.

Standard outcome measurement requirements for a public goods grant would typically ask for user counts, geographic breakdown, and usage frequency. Applied to MoaV without modification, these requirements would create a harm: satisfying them would require collecting the same data that, if obtained by Iranian or Russian authorities, would expose users to adversarial surveillance, detention, or worse.

CROSS specifies that when standard measurement would compromise the safety of the beneficiary population, privacy-preserving measurement methodologies are required in lieu of standard analytics. The accommodation is not an exemption from obligation; it requires specifying which obligation mechanisms are appropriate to the context.

The application partially addressed this: the zero-telemetry design is documented, the privacy rationale is implicit in the tool's architecture, and the Digital Public Goods Standard self-assessment correctly identifies telemetry absence as a design property rather than a gap. However, the application did not formally invoke the privacy-sensitive accommodation. It did not name the specific harm that standard measurement would create, did not name the alternative methodology that would be used instead, and did not identify an institutional partner who could validate the alternative methodology through an ethics-reviewed process.

The evaluation recommends funding with conditions, including that the applicant name the specific measurement harm and specify the alternative methodology before disbursement.

### CROSS Assessment

Privacy-sensitive accommodation: invoked implicitly through architectural design but not formally declared. The invocation is incomplete because it names the design property (zero telemetry) but not the harm avoided by that design, and names no alternative measurement methodology.

Entry specification gate: passes. The FROM state is specific and externally verifiable: Open Observatory of Network Interference probe data and multiple independent sources document that Iranian internet connectivity dropped to 1-4% of normal levels during February-March 2026. A specific measurable condition in a defined population exists.

Institutional capacity: mixed. The founder's background is directly relevant; the solo contributor structure and absence of independent security review are the primary risks.

### What a Compliant Accommodation Request Would Have Looked Like

A conformant formal invocation of the privacy-sensitive accommodation would do four things.

First, it would name the specific harm. "Standard outcome measurement for this grant would require collecting data on the number, geographic distribution, and usage patterns of users in Iran, Russia, and Myanmar. This data, if obtained by authorities in those jurisdictions through server seizure, subpoena of a hosting provider, or interception, would identify individuals who circumvented government-imposed internet restrictions. This constitutes a direct physical safety risk to the beneficiary population."

Second, it would name the alternative methodology. For example: "Impact will be assessed through aggregate, non-attributable measurement using Open Observatory of Network Interference probe data to confirm that the protocols MoaV deploys remain unblocked in the relevant networks. This is the same methodology used by Tor Project and Psiphon to assess protocol effectiveness without exposing users. The methodology produces a binary indicator (protocol reachable or not) rather than a user count. An ethics-reviewed study with a named institutional partner, such as the Citizen Lab at the University of Toronto or the Open Observatory of Network Interference, will be pursued during the grant period to provide independent validation."

Third, it would name the specific measurement harm the alternative avoids: user identification, location attribution, and usage fingerprinting.

Fourth, it would commit to at minimum one piece of independent validation that does not require user identification: a GitHub release changelog confirming protocol updates in response to documented blocking events, with timestamps cross-referenceable to Open Observatory of Network Interference measurement data showing those events.

---

## Case 4: Concurrent Funding Disclosure Failure

**Project:** The Interfold (formerly Enclave)
**Ask:** \$100,000
**Outcome:** Fund with conditions
**Criterion illustrated:** Concurrent funding disclosure; Adverse signal disclosure

### The Application

The Interfold is a protocol and distributed network that uses threshold Fully Homomorphic Encryption to compute over encrypted inputs and produce publicly verifiable outputs, without any single operator ever seeing the raw data. The cryptographic work is technically serious: BFV encryption allows arithmetic operations over ciphertexts; a threshold committee of independent nodes generates a joint key through Publicly Verifiable Secret Sharing; computation happens over encrypted inputs; outputs are decrypted only when a threshold of nodes cooperate; and recursive proof aggregation lets the final state be verified by a single proof on Ethereum. The project was previously known as Enclave, rebranded in March 2026. The ask of \$100,000 was directed primarily at an external security audit (approximately \$70,000) with the remainder as runway while the audit proceeds. The application listed Session and Taiko as organizations that had committed to using the protocol.

### The CROSS Finding

The application did not disclose a \$1M venture capital round recorded in KarmaGAP. It did not disclose a \$3.82M GnosisDAO treasury allocation under Gnosis Improvement Proposal 78, which covered the Gnosis Guild guild-wide operations including the Enclave project. It did not disclose a Zcash Community Grant application for \$130,000 for a CRISP-based coordinating instrument called Zecret Ballots, which was rejected by the Zcash Community Grants committee in April 2026, approximately one month before this application.

These are three independent disclosure failures under CROSS's concurrent funding disclosure requirement. The venture capital round and the GnosisDAO allocation together represent more than \$4.8M in related prior funding, none of which appeared in the application. The Zcash rejection is an adverse signal for a closely related CRISP application in an adjacent ecosystem, which must be disclosed under the Adverse-Signal Engagement Principle.

The application also misrepresented two claimed partnerships. The application stated that Session had "committed to using the protocol for aggregated user analytics." No Session-side corroboration exists: Session's blog post on user analytics makes no mention of The Interfold, fully homomorphic encryption, or any privacy-preserving analytics integration. The only evidence of a relationship is a co-marketing X Space appearance, which is not a technical commitment. The application stated that Taiko had "committed to using CRISP for program decisions on their existing Aragon mainnet instance." The Interfold's own blog post on the Taiko collaboration uses entirely aspirational language ("can be deployed," "can operate," "can rely on"), and CRISP is not named in the Taiko collaboration post. No Taiko-side publication confirms a commitment to deploy.

The core protocol work is genuine. The cryptographic implementation is real: Sepolia deployments are confirmed, 90% of protocol circuits were complete as of April 2026, and the Aragon integration is corroborated from Aragon's side. The disclosure failures are process failures, not fabrications about the technology itself.

### CROSS Assessment

Concurrent funding disclosure: incomplete. The \$1M venture capital round and the GnosisDAO Gnosis Improvement Proposal 78 allocation are both related to the scope of the application and both fall within the 24-month disclosure window. Neither appears in the application.

Adverse signal disclosure: incomplete. The April 2026 Zcash Community Grant rejection for Zecret Ballots, a CRISP-based coordinating instrument closely related to the application's scope, was not disclosed.

Partnership claim integrity: two claimed commitments (Session and Taiko) are contradicted by the available evidence. This is a rigor-tier finding rather than a gate failure; the gate passes on the strength of the Aragon integration and the cryptographic work. But the two uncorroborated "commitment" claims constitute material misrepresentation that must be corrected before disbursement.

Recommendation: Fund with conditions, not Do not fund, because the disclosure failures are addressable and the underlying work is real. But no disbursement occurs until all four concurrent funding sources are disclosed, the Zcash rejection is disclosed with explanation, and written confirmation from Session and Taiko replaces the uncorroborated "commitment" language.

### What Compliant Disclosure Would Have Looked Like

A conformant application would have listed in the concurrent funding disclosure field:

(1) Venture capital round: approximately \$1,000,000, investor not publicly named, closed prior to this application, no program decision rights over the protocol granted to investors. Relationship to this application: this funded the engineering work that produced the protocol now seeking audit funding.

(2) GnosisDAO Gnosis Improvement Proposal 78 allocation: approximately \$3,820,000 to Gnosis Guild operations guild-wide, covering Zodiac, Enclave, and other tooling. Portion attributable to Enclave/The Interfold is approximately [amount]. Relationship to this application: prior operating funding that has been substantially deployed; current request is for audit funding not covered by prior allocations.

(3) Zcash Community Grant: \$130,000 requested for Zecret Ballots, a CRISP-based secret ballot application for the Zcash ecosystem. Rejected by Zcash Community Grants committee, April 2026. Rejection rationale as provided by the committee: [summary]. Relationship to this application: the CRISP protocol being evaluated here is the same protocol proposed for Zecret Ballots. The rejection did not concern protocol soundness but [specific rationale].

With these disclosures complete, the evaluation would have proceeded directly to assessing whether the audit ask is appropriately scoped and whether the partnership claims are adequately corroborated, rather than surfacing the omissions through independent research.

---

## Case 5: Well-Specified Application with Hard Gates

**Project:** Gean (Go Lean Ethereum Consensus Client)
**Ask:** \$30,000
**Outcome:** Fund with conditions
**Criterion illustrated:** Entry specification gate passage; Institutional capacity; Conditional funding

### The Application

Gean is a Go implementation of the Lean Ethereum consensus client, targeting the Lean Consensus devnet infrastructure initiated by Ethereum Foundation researcher Justin Drake. The Lean Ethereum initiative, announced July 2025, proposes replacing Bonnet-Lynn-Shacham signatures with hash-based post-quantum signatures and compressing thousands of signatures into a single short proof via a recursive zero-knowledge virtual machine. A new consensus client implementation is the primary way teams contribute to this initiative's interoperability goals. Gean is the only Go client in the ecosystem; the other implementations are Rust, Zig, C++, C, and Rust fork variants. The project is MIT-licensed, targets Go 1.25+, passes 49 current leanSpec test fixtures, and integrates with the lean-quickstart multi-client devnet tooling. The \$30,000 ask covers approximately 6-8 months of additional runway, expanded contributor capacity, and continuous integration infrastructure. The application references an Ethereum Foundation Ecosystem Support Program grant identified as FY26-2432.

### The CROSS Finding

The entry specification gate passes on this application, and passes clearly. The FROM state is specific and externally verifiable: the Ethereum network has effectively zero production Go execution clients other than the reference client (go-ethereum/geth) following the deprecation of prior clients; the post-quantum Lean Ethereum initiative requires multiple independent consensus client implementations to achieve the interoperability testing that prevents a monoculture risk; and Go is underrepresented in the current Lean Ethereum client landscape (Rust, Zig, C++, C are all represented; Go is not). This condition is named in Ethereum ecosystem research and in the Lean Ethereum initiative documentation, not only in the applicant's own materials.

The evaluation confirmed: 344 commits on the main branch with activity through April 2026; 49 passing leanSpec spec fixtures; active devnet-4 migration work (Issue 208, filed April 12, 2026); inclusion in the lean-quickstart multi-client devnet tool alongside 9 other implementations; and leanroadmap.org listing of Gean as the Go implementation.

Two hard gate conditions apply before disbursement.

The first is the Ethereum Foundation Ecosystem Support Program grant FY26-2432. The grant identifier appears in Gean's own KarmaGAP profile and nowhere else in any searchable public source. The Ethereum Foundation Q1 2026 and Q4 2025 allocation reports do not name Gean individually. The KarmaGAP profile recording the grant was created on the same day as this evaluation. This is consistent with how the Ethereum Foundation handles individual Ecosystem Support Program grants (grant identifiers are not published in allocation reports), but it means the only external validation of the grant is the applicant's own filing. One email to grants-admin@ethereum.org resolves this, but it must happen before any funds move.

The second is devnet participation. Gean is listed in the lean-quickstart tool but does not appear in the pq-devnet-3 planning document or in the two most recent post-quantum Interop meeting notes (numbers 36 and 37), which name Ream, Zeam, Qlean, Lantern, and Lighthouse as the active cross-client participants. Whether Gean is running nodes in official Ethereum Foundation-coordinated cross-client devnets or only in the lean-quickstart local environment is a meaningful distinction for the milestone assessment. Direct confirmation from Thomas Coratger (the facilitator of the weekly post-quantum Interop calls at the Ethereum Foundation) resolves this.

### CROSS Assessment

Entry specification gate: passes. The FROM state is specific, externally corroborated, and names a real gap.

Institutional capacity: mixed. The project has a genuine development track record (344 commits, 49 passing fixtures, active devnet migration), a named Ethereum Foundation funding relationship, and multiple named contributors. The lead active contributor (dimka90) has no independently verifiable public profile beyond the GitHub username, which is a legibility gap for a three-person team. The legal status discrepancy (the application claims registered organization; the KarmaGAP profile describes an unincorporated working group) should be resolved.

Conditional funding: how it works in CROSS. The conditions are specific, verifiable, and time-bounded. Each has a named verification method: the Ethereum Foundation grant is confirmed by emailing grants-admin@ethereum.org; devnet participation is confirmed by contacting Thomas Coratger at thomas.coratger@ethereum.org. Both are verifiable within days, not months. If either check fails, the recommendation changes to Do not fund. This is the structure of conditional funding under CROSS: conditions are not aspirational guidance; they are binary gates with named verification paths that must be cleared before disbursement.

### What the Conditional Funding Structure Demonstrates

This case illustrates the distinction between a project that passes the entry specification gate and a project that is ready for unconditional disbursement. Gean passes the gate; the FROM state is real, the work is real, and the public goods character is unambiguous. The conditions exist not because the project is weak but because two specific factual claims (the Ethereum Foundation grant and the devnet participation) cannot be verified from public sources alone. The conditions protect the funder without punishing the applicant: if the claims are true, both conditions clear in less than a week.

---

## Case 6: Conditional Funding with Security Disclosure Requirement

**Project:** poidh ("pics or it didn't happen")
**Ask:** \$20,000
**Outcome:** Fund with conditions
**Criterion illustrated:** Adverse signal disclosure; Conditional funding

### The Application

poidh is an open-source, non-custodial, immutable bounty protocol deployed across Arbitrum, Base, and Degen Chain. Anyone can post a bounty, anyone can add funds to it, and anyone can claim it by submitting photo, video, or text proof minted as a non-fungible token. When the bounty creator selects a winning claim, contributors vote to approve or veto based on their proportional stake. Smart contracts handle escrow and automatic payout on approval. There is no coordinating token and no central treasury. The protocol charges a 2.5% fee on completed bounties. In September 2025, a crowdsourced poidh bounty of approximately 10 million DEGEN tokens (worth \$28,000-\$35,000 at peak) funded a successful attempt to break the Guinness World Record for most kickflips in one minute, independently corroborated by Decrypt and video documentation. The v3 contract is deployed at a consistent address across Arbitrum and Base. The \$20,000 ask, the smallest in this evaluation cycle, covers resumed development and promotional public goods bounties.

### The CROSS Finding

The application did not disclose a v2 protocol exploit that occurred on December 8, 2025. The v3 internal security report documents two reentrancy vulnerabilities that were exploited: a claim acceptance reentrancy, where safeTransfer callbacks invoked onERC721Received before bounty state was finalized, allowing re-entry while balances remained nonzero; and a refund-loop reentrancy, where Ether was pushed to participants via call{value} loops while participant accounting was not finalized, enabling double-refund attacks. The v3 rebuild addresses both through ReentrancyGuard, strict Checks-Effects-Interactions patterns, and pull-based payments. The amount drained in the exploit has not been publicly disclosed.

The application mentioned the exploit only as an explanation for where a prior Base Builder Grant was spent on the rebuild. It did not name the exploit date, the exploit vectors, the amount drained, whether affected users were compensated, or how the Base Builder Grant was spent on remediation. This is an incomplete adverse signal disclosure under the Adverse-Signal Engagement Principle.

A separate safety issue is the beginner guide at words.poidh.xyz/poidh-beginner-guide, last updated August 2024. At time of evaluation, the guide still listed the old v2 contract addresses on Arbitrum, Base, and Degen Chain. These are the addresses from the exploited version. A user following the guide would interact with the compromised v2 contracts. This is a live documentation safety hazard for protocol users.

The protocol's merits are genuine and independently corroborated. The Guinness World Record attempt is documented in third-party press. The public goods bounties album shows completed real-world civic actions globally: road mark repairs, community garden documentation, utility hazard reporting, public space cleanup. The 30 GitHub contributors and 1,966 commits reflect a real development community. The v3 fix is technically appropriate.

Under the Adverse-Signal Engagement Principle Core Standard, an adverse signal that can be disclosed and addressed is not automatically a disqualifier. The question is whether the conditions are addressable. They are.

### CROSS Assessment

Adverse signal disclosure: incomplete. The v2 exploit was referenced but not disclosed. Required disclosures include the date (December 8, 2025), the exploit vectors, the approximate funds at risk, whether affected users were made whole, and how the Base Builder Grant was spent on the rebuild.

Safety condition: the beginner guide still references exploited v2 contract addresses, creating a live hazard for users who follow it. This is not an adverse signal issue; it is a separate condition requiring documentation correction before disbursement.

Entry specification gate: passes. The FROM state for a deployed bounty protocol is specific and verifiable: existing onchain bounty coordination lacks a non-custodial, proof-verified mechanism where funders and claimants can coordinate without trusting a single operator.

Recommendation: Fund with conditions because the protocol's merits are real, the ask is modest, the conditions are addressable within days, and adverse signal disclosure failure with a clear remedy is a process error, not a disqualifier.

### What a Compliant Adverse Signal Disclosure Would Have Looked Like

The concurrent funding and adverse signal section of the application should have contained an entry along the following lines:

"On December 8, 2025, the v2 poidh contracts on Arbitrum and Base were exploited via two reentrancy vulnerabilities: claim acceptance reentrancy and refund-loop reentrancy. Approximately [amount] was drained. Affected users [were / were not] compensated [explain approach]. The Base Builder Grant of approximately \$15,000 received in November 2025 was directed entirely to the v3 rebuild, which addresses both vulnerabilities through ReentrancyGuard, Checks-Effects-Interactions patterns, and pull-based payment mechanics. The v3 contracts were deployed in January 2026. The v2 contracts remain deployed but are no longer promoted by the team. The beginner guide requires updating to remove v2 contract addresses."

This disclosure does not eliminate the grant application's eligibility. It demonstrates that the team understands what happened, what was done to address it, and what remains to be done. That is the information the committee needs to make a sound funding decision.

### The Conditions Before Disbursement

Under CROSS conditional funding, the conditions are:

Written disclosure of the v2 exploit by the applicant, including the date, the vectors, the approximate funds at risk, whether affected users were made whole, and the basis for the Base Builder Grant allocation. This replaces the incomplete reference in the application.

The beginner guide at words.poidh.xyz/poidh-beginner-guide must be updated to replace the v2 contract addresses with the correct v3 addresses before the allocation window opens.

KarmaGAP registration with specific milestones mapped to the stated development deliverables.

The embedded wallet milestone language must be revised to reflect the v3 contract's externally owned account constraint (the msg.sender == tx.origin requirement), which blocks standard ERC-4337 account abstraction wallets, or the applicant must explain how they intend to resolve that architectural conflict before disbursing funds toward that milestone.

At \$20,000 with clear, time-bounded, binary conditions, this is a high cost-effectiveness grant for a real deployed protocol with documented public goods impact.

---

## Summary Table

| Case | Project | Criterion Illustrated | Entry Gate Status | Outcome |
|------|---------|----------------------|-------------------|---------|
| 1 | Mushee Allocate | Beneficiary validation | Passes; fails beneficiary validation dimension | Do not fund |
| 2 | mev-commit | Operational definition; Integrity | Passes (on encrypted mempool milestone); fails rigor tier | Do not fund |
| 3 | MoaV | Privacy-sensitive accommodation | Passes | Fund with conditions |
| 4 | The Interfold | Concurrent funding disclosure; Adverse signal disclosure | Passes | Fund with conditions |
| 5 | Gean | Entry gate passage; Institutional capacity | Passes | Fund with conditions |
| 6 | poidh | Adverse signal disclosure; Conditional funding | Passes | Fund with conditions |

---

## Key Distinctions This Set Illustrates

Three distinctions recur across these cases and are worth naming explicitly for practitioners.

The first is the distinction between an entry specification gate failure and a rigor-tier failure. Cases 1 and 2 both result in Do not fund, but for structurally different reasons. Mushee Allocate fails at the beneficiary validation dimension: the FROM state exists but was not validated against the competitive landscape. mev-commit passes the gate on its encrypted mempool milestone (a specific condition is named) but fails at the rigor tier on indicator specification and integrity. These require different responses from a committee: a gate failure redirects the applicant to do foundational diagnostic work before reapplying; a rigor-tier failure identifies specific documentation deficiencies that could potentially be addressed in a revised application.

The second is the distinction between D1 and D2 failure modes in change-obligation rounds. These are Frame Language diagnostic categories that appear in the CROSS assessment rubric. A D2 failure (values aspiration without conditions) cannot name a FROM state at all; the application produces more values language when pressed for a diagnosis. A D1 failure (canonical vocabulary without structural grounding) can name a FROM state using recognized terminology but cannot support the specific measurable indicators claimed with sourced methodology. Both fail at the entry specification gate, but at different levels and for different reasons, and the appropriate response to each is different. Note that these failure modes apply specifically to change-obligation rounds; the entry specification gate for build-obligation rounds uses different failure vocabulary (direction specification without deliverable; underspecified completion criteria).

The third is the distinction between adverse signal disclosure failure and a disqualifying adverse signal. Cases 4 and 6 both involve incomplete adverse signal disclosure. In neither case does the disclosure failure automatically disqualify the application: The Interfold's cryptographic work is real and the Zcash rejection does not invalidate it; poidh's protocol merits are genuine and the v2 exploit was remediated. The Adverse-Signal Engagement Principle Core Standard requires disclosure; it does not treat disclosed adverse signals as automatic bars. The conditions in both cases are designed to produce the disclosure and allow the evaluation to proceed on complete information.
