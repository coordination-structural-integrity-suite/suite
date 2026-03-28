# Structural Consent Legibility Audit
Copy everything below the line, paste it into any AI chat, and attach or paste the governance document, participation terms, or consent architecture you want audited.
---
You are auditing the attached document or system description for consent legibility failures using the Structural Consent Legibility Standard (CC BY 4.0, Regis Lloyd Chapman). A consent legibility failure is any condition in which a participant cannot determine who is acting, who benefits, what they are specifically consenting to, or whether and how they can withdraw.

The standard requires that every consent-bearing interaction answer two questions: who is acting, and who benefits from the action? Shadow dynamics — where one or both answers are obscured — are the mechanism through which extraction operates inside systems that claim participant consent. Most deployed consent mechanisms (token-weighted voting, delegated authorization, optimistic approval, on-chain permission systems) fail to answer the "who benefits" axis. This audit identifies where those gaps appear.

Check for these eight consent legibility failures:

1. Standing gap: the affected constituency is not identified before a consent-bearing action proceeds. "Affected constituency" means the set of participants whose governance standing, coordination records, data sovereignty, participation terms, or observation exposure would be materially altered by the action. If those parties were not identified before the action, the identification step failed. Note that the implausible absence of standing claims from parties who should be affected is itself a failure.

2. Axis obscuration: the consent mechanism cannot answer both Wheel of Consent questions — who is acting, and who benefits from the action? Any mechanism that conflates these two (e.g., a vote where the voting body also benefits from ratification) has an axis obscuration failure. For each one found, identify which axis is obscured and propose a restructured mechanism that makes both axes visible.

3. Silence treated as consent: the system treats silence, inaction, or absence of objection as authorization without explicit prior opt-in to that interpretation. For each instance, propose language that structurally distinguishes authorized, not-yet-responded, and unable-to-respond.

4. Negotiated limits absent: participants cannot set and maintain explicit boundaries within a consent-bearing interaction. The structural test: can the consenting party specify what they are agreeing to and what is excluded? If the consent mechanism requires accepting all terms or none, negotiated limits are absent. For each instance, propose a scope-bounding mechanism.

5. Bidirectional awareness failure: at least one party in a consent-bearing interaction does not know who is acting and who the action is for. This includes cases where the beneficiary of a governance action is not named, and cases where the party being acted upon does not know the action benefits the acting party. For each one found, identify which axis was not legible to which party and propose a disclosure requirement.

6. Structural non-revocability: the cost of withdrawing consent — exiting, objecting, or refusing — exceeds the benefit of participation. Formal permission to withdraw without a structural mechanism making withdrawal viable is not revocability. For each instance, identify the specific cost that makes withdrawal prohibitive and propose a structural mechanism to reduce or distribute it.

7. Verification gap: the system cannot demonstrate, after the fact, that consent was structurally valid at the time it was given. Verification requires the consent record to identify: who acted, who benefited, who was affected, and what the agreed limits were. If any of these four elements is absent, the verification gap applies. For each one found, propose a durable consent record structure.

8. Consent domain blindness: a single consent mechanism is applied across two or more of the five consent domains — governance (rule changes), data (collection and use), participation (entry terms and exit), output (use of generated signals and scores), observation (what the system monitors) — without domain-specific analysis. Different domains have different beneficiary structures and different stakes for the affected constituency. For each domain conflation found, identify which domains are collapsed and propose domain-specific consent architecture.

For each failure found, list:
- The specific mechanism, clause, or process that fails the condition
- Why it fails (what makes it structurally obscured, absent, or non-legible)
- A concrete proposal for making it structurally legible

Output the results as a consent legibility failure map organized by failure type, with the failures most likely to enable extraction or suppress genuine participant consent first.

Full standard: https://github.com/durgadasji/standards
