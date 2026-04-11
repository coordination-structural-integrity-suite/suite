# Coordination Structural Integrity Suite - Suite Integration Guide SKILL.md

When someone brings you the Suite Integration Guide, they are usually in the middle of something. They have decided to adopt some standards and are trying to figure out what to prioritize next, or they have an audit result and want to know whether it is reliable, or they are disclosing partial adoption and want to know what to say about the gaps. Your job is to help them make structurally sound decisions about what to adopt and in what order, and to surface the dependencies that change what an audit result actually means.

## What this skill is for

This skill enables correct reasoning with the Suite Integration Guide. That document addresses two questions that appear after the initial adoption decision: which standards interact structurally, and what does that mean for adoption sequencing and audit reliability?

Use this skill when someone is:
- Deciding what to adopt next after an initial entry point
- Asking whether their current audit results are reliable
- Needing to produce a structural exposure disclosure for partial adoption
- Trying to understand why adding one standard matters for the ones already adopted

For first-time orientation to what the standards are, use the Tensegrity Architecture skill. For selecting the right combination based on presenting situation, use the Suite Deployment Contexts skill. For recognizing a structural pattern before selecting standards, use the Structural Patterns Primer skill.

## The single most important thing to understand

Some compressive standards produce unreliable detection results when certain generative conditions are absent. An audit result produced under those conditions is not what it appears to be. This is the most important practical implication of the two-layer architecture, and it is not obvious until the dependency is named.

An audit result is not an audit result if its detection surface is compromised. Before drawing conclusions from a compressive standard audit, ask: are the generative conditions this standard's detection architecture depends on present and instrumented?

## The four detection reliability dependencies

These are the specific cross-layer dependencies where compressive standard audits produce unreliable results without the named generative condition.

**Adverse-Signal Engagement Principle Core Standard depends on the Four Batteries Capacity Standard (Relational Battery).** When Relational Battery is depleted — when trust, psychological safety, and reciprocity are structurally low — participants will not surface adverse signals even when explicitly invited to. An Adverse-Signal Engagement audit run without Relational Battery visibility produces false negatives: the absence of surfaced signals appears as compliance when it may be suppression under unsafe conditions.

**Structural Consent Legibility Standard depends on the Four Batteries Capacity Standard (Relational Battery).** Agreement reached under conditions of Relational Battery depletion is structurally hollow. Participants may consent formally while unable to safely refuse or contest. Consent legibility audits run without Relational Battery visibility cannot distinguish genuine consent from structural coercion by depletion.

**Structural Power Obligation Standard (coordination dimension) depends on the Sensemaking Standard.** The coordination dimension of power — who controls what alignment mechanisms mean — requires that the organization have a functioning sensemaking infrastructure. Without it, interpretive power is invisible: the people controlling how signals and events are framed hold coordination power that cannot be observed without sensemaking capacity. Power distribution audits run without sensemaking infrastructure cannot see the coordination dimension.

**Information Asymmetry Classification Standard (omission class) depends on the Sensemaking Standard and the Four Batteries Capacity Standard (Contribution Battery).** Omission asymmetry — what is not surfaced because participants cannot or do not — requires both sensemaking infrastructure (to know what should be surfaced) and Contribution Battery visibility (to know whether participants have the agency and meaning to surface it). Omission class audits run without these generative conditions produce systematic false negatives on the most consequential asymmetry class.

## Adoption sequencing implications

These dependencies mean that adding the Four Batteries Capacity Standard early is structurally high-priority for most organizations. It enables three other compressive standards to reach reliable detection: Adverse-Signal Engagement, Structural Consent Legibility, and (via Contribution Battery) Information Asymmetry Classification.

The Sensemaking Standard similarly enables reliable detection for the coordination dimension of Structural Power Distribution and for the omission class of Information Asymmetry Classification.

This does not mean adopting Four Batteries or Sensemaking first regardless of context. It means accounting for the detection reliability bounds of any compressive standard audit produced before these generative conditions are instrumented.

## The five entry-point pairings

When an organization needs to start somewhere specific, the guide names five pairings matched to presenting pain:

Signals suppressed or dismissed: Adverse-Signal Engagement Principle Core Standard plus Four Batteries Capacity Standard.

Governance capture or authority concentration: Structural Power Obligation Standard plus Structural Consent Legibility Standard.

Invisible work or contributor burnout: Four Batteries Capacity Standard plus Regenerative Obligation Standard.

Decisions missing key information: Information Asymmetry Classification Standard plus Sensemaking Standard.

Conflict destroying coordination capacity: Conflict Transformation Standard plus Adverse-Signal Engagement Principle Core Standard.

## Partial adoption disclosure

Every organization that claims structural accountability without holding the full Tensegrity Compressive Standards designation must produce a structural exposure disclosure. The disclosure must name: each absent standard; the failure mode class it addresses; a self-assessed exposure level with rationale; any compensating controls; and the detection reliability bounds of any audits produced under partial adoption.

The detection reliability bounds element is specific to the Integration Guide. An organization that has adopted Adverse-Signal Engagement but not Four Batteries Capacity must disclose that its Adverse-Signal Engagement audits have reduced reliability in the absence of Relational Battery visibility.

## The developmental direction

Adoption sequence is structurally determined, not motivationally. The question is not which standard the organization finds most meaningful. The question is which absent standard most undermines the reliability of what is already in place. That standard is the next structural priority.

When helping someone determine their next adoption priority: identify which compressive standards they have adopted, check whether any of those are subject to detection reliability dependencies, and identify whether those generative conditions are instrumented. If not, the generative standard that enables reliable detection is the next structural priority.
