# Six-V Trust Framework - SKILL.md

When someone brings you this framework, they have usually encountered one of two situations. Either they are assessing a specific relationship that is advancing in access or trust, and they want to know whether they are running the right checks in the right order. Or something has already failed, and the post-mortem is revealing that the structural checks that would have caught the failure were suppressed by investment in the relationship's value, or were never triggered because the interaction looked completely normal.

Your job is to help them see what the framework requires, where the failure sequence is most likely to close given the characteristics of their specific case, and what structural design changes would prevent it from closing.

## What this skill is for

This skill enables correct reasoning with the Six-V Trust Framework when someone brings it to you. This is a framework-application document, not a standard. It does not specify structural floors with conformance tiers. It specifies an operational sequence for the trust-extension decision, names the failure modes at each step, and provides structural design guidance.

Use it when assessing a specific relationship for access or trust extension, analyzing a security incident or governance failure post-mortem, designing onboarding or credentialing processes, or identifying where a current relationship may have normalized past the point where structural checks are running.

## The single most important thing to understand

The six-V sequence is not an expression of suspicion. It is a standard of care. The structural checks are designed to run independent of how much anyone likes, values, or has invested in the counterparty. Their independence from relational signals is not a bug to be softened; it is the entire mechanism.

This matters because the framework's central insight is that sophisticated adversaries do not break structural checks. They manufacture the social conditions that prevent structural checks from running. The checks are not bypassed; they are suppressed before they are triggered. The social layer (Visible, Vanilla) is where this suppression begins. The structural checks (Vulnerable, Verify, Validate) are where it is caught, if the design is right. If the design allows relational investment to govern whether the checks run, the design has been compromised before any adversary acts.

## The six Vs and their functions

**Visible** registers social presence. It is the most exploitable factor because it is the cheapest to manufacture and the most psychologically powerful. Sustained presence, face-to-face meetings, working sessions across multiple venues: these feel like evidence of legitimacy. They are not. They are the social trigger that begins the relationship. They do not substitute for any subsequent step.

**Vanilla** is the hinge between the social layer and the structural checks. The question it poses is not "does anything look suspicious enough to warrant scrutiny?" It is the inversion: "does this look completely normal, and is that normality making the structural checks less likely to run?" If the answer is yes, the urgency of the subsequent steps increases, not decreases. Normality is the attack surface the framework is most specifically designed to address. Post-incident accounts that describe an interaction as "completely standard" or "just how these relationships work" are naming the Vanilla condition as the mechanism of suppression, not as exoneration.

Welcoming-culture amplification is a specific Vanilla risk. Organizations with strong hospitality norms face systematically higher Vanilla risk because the default interpretive frame combines "this looks normal" with "we want this to feel good." Naming the Vulnerable step feels socially costly in that context because it introduces friction into a moment the organization is culturally oriented to make frictionless.

**Vulnerable** requires explicitly naming the exposure before proceeding. What does this relationship make accessible? What would the organization lose or be exposed to if the interaction that looks vanilla is not? This step must run before Value, not after. Named after relational investment has accumulated, the vulnerability feels like threatening something already committed to. Named before, it gives the stakes-assessment register an anchor.

**Value** carries an internal tension that is itself the primary attack surface. It has two registers that must be assessed separately: the stakes-assessment register (what is actually at risk in this relationship, now that the vulnerability has been named) and the relational value register (this person matters to us; the relationship has meaning). Both are legitimate. The trap is when the relational register answers the stakes-assessment question. At sufficient relational depth, this colonization is cognitively automatic, not a failure of discipline. The structural resolution is not mental effort; it is role separation. The stakes-assessment register must be evaluated by actors who do not hold relational investment in the subject. See Two-Track Design.

**Verify** addresses the bad-actor failure mode: structural verification of identity and intent. Is this entity who they represent themselves to be? Does their stated purpose hold under scrutiny? This check must be designed against the specific exposure named in the Vulnerable step, not run as a generic identity check. Generic checks can be beaten by manufactured credentials. Checking against "if this actor is adversarial, what specifically do they now have access to" is structurally different and much harder to prepare for without revealing what is being hidden.

**Validate** addresses the good-faith-but-mismatched failure mode: structural validation of competence for the specific responsibility being extended. Not general competence, not technical fluency in an adjacent domain, not ideological alignment. Competence for this role at this stakes level. This step closes the failure mode where well-intentioned actors cause structural damage because they were trusted with responsibilities their specific competence does not cover.

## The failure sequence

The trap is set at Vanilla, not at Value. Vanilla normality suppresses the Vulnerable naming. Skipped vulnerability means the stakes-assessment register has no anchor. Unanchored stakes assessment is filled by the relational register. The relational register then suppresses Verify and Validate because running them feels like threatening something the organization depends on.

Four cross-sequence failure classes operate across the whole sequence rather than at a specific step:

**Inherited trust**: the sequence was run once by predecessors; the result is inherited indefinitely. The original check's validity degrades as context changes, but the inherited trust status persists. A relationship, credential, or access grant treated as permanently valid because it was once verified by someone else.

**Reference capture**: Verify appears to run, but verification sources are not independent of the subject. References are provided by the subject or from within their relationship network. The check produces outputs but independence was never established.

**Distributed diffusion**: no individual runs the sequence. Collective adoption of a relationship or credential substitutes for structural assessment. Everyone assumes someone else ran the check.

**Domain credential transfer**: Validate runs, but against the wrong domain. Competence in domain A is imported as competence in domain B. The actor is validated based on demonstrated excellence in an adjacent domain; the specific competence required for the responsibility being delegated is never assessed.

## The two-track design

The structural solution to welcoming-culture amplification and to the Value trap is organizational separation: the relational track (welcoming, warmth, ease of participation) and the credentialing track (access and trust extension decisions) must run through different actors with different mandates.

The people running the relational track have no authority over the credentialing decision. The people running the credentialing track are not trying to welcome anyone. When the tracks are separated, frictionless onboarding and rigorous credentialing are not in tension. The welcoming experience and the access decision never occupy the same room.

Rigorous credentialing is not an expression of suspicion toward incoming actors. It is a standard of care that protects both parties. Legitimate actors who understand this read rigorous credentialing as organizational maturity, not hostility. Organizations that make access frictionless are also less trustworthy as counterparties, because their partners cannot trust that other actors in that organization were screened.

Separation removes relational colonization of the access decision. It does not improve the quality of Verify and Validate themselves. Both must still be designed against the specific exposure named in the Vulnerable step.

## Scope condition

The framework applies to relationships that are advancing in access or trust over time. It is not designed for cold-contact or single-interaction cases where relational accumulation has not yet occurred. The sequencing is most critical in the phase between initial contact and consequential access extension — the phase where Visible and Vanilla signals are building but structural checks have not yet run.

## Working with someone applying this framework

When someone brings you a specific relationship to assess, ask them to describe: what the counterparty's Visible signals are; whether the interaction has looked completely normal (the Vanilla condition); what the specific exposure would be if the relationship turned adversarial (the Vulnerable step, named explicitly); who is assessing the stakes and whether those actors hold relational investment in this outcome; what identity and intent verification has run and whether it was designed against the named exposure; and what specific competence has been validated for the specific responsibility being extended.

Use their answers to identify where in the sequence the checks are most likely to be suppressed and what structural changes would prevent that suppression. The goal is not a checklist completion; it is a structural reading of where the trap is most likely to close in this specific case.
