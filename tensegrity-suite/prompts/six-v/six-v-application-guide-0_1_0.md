# Six-V Trust Framework - Application Guide
Use when you are assessing a specific relationship that is advancing in access or trust, designing a credentialing or onboarding process, or analyzing why a past trust-extension decision failed. This prompt walks through the six-V sequence against your case, names where each failure mode is most likely given the specific exposure profile, and identifies what structural changes would close the gaps.

This is not an audit prompt. There is no conformance score. The output is a structural reading of your case.

Copy everything below the line, paste it into any AI chat, and describe the relationship, process, or incident you want to assess.
---
You are applying the Six-V Trust Framework (CC BY 4.0, Regis Lloyd Chapman) to a specific trust-extension case. This is an application guide, not an audit. The goal is a structural reading of how the six-V sequence applies to the specific relationship, decision, or failure the user has described, identifying where each failure mode is most likely and what structural changes would address it.

The Six-V Trust Framework specifies a sequence of six social and structural factors that govern how trust should be extended in consequential relationships. The sequence is: Visible → Vanilla → Vulnerable → Value → Verify → Validate.

The sequence is designed to prevent structural checks from being suppressed by relational investment. Its central insight is that sophisticated adversaries do not break structural checks; they manufacture the social conditions that prevent structural checks from running.

The six Vs and their functions:

**Visible** — Social presence: sustained, consistent, face-to-face. The most exploitable factor because it is the cheapest to manufacture and the most psychologically powerful. Presence feels like legitimacy. It is not. Visible triggers engagement but does not substitute for any subsequent step.

**Vanilla** — The interaction looks completely normal. Standard practice. Nothing unusual. Vanilla is the hinge between the social layer and the structural checks. The question is not "does anything look suspicious?" It is the inversion: "does this look completely normal, and is that normality making the structural checks less likely to run?" If yes, the urgency of the subsequent steps increases, not decreases. Normal-looking interactions in high-stakes contexts require structural checks more reliably than unusual ones. Post-incident accounts that describe an interaction as "completely standard" are naming Vanilla as the suppression mechanism, not as exoneration.

**Vulnerable** — Name the exposure explicitly before proceeding. What does this relationship make accessible? What would the organization lose or be exposed to if the interaction is adversarial? This step must run before Value, not after. Named after relational investment has accumulated, the vulnerability feels like threatening something already committed to. Named before, it gives the stakes-assessment register an anchor.

**Value** — Two registers that must be assessed separately: the stakes-assessment register (what is actually at risk, informed by the named vulnerability) and the relational value register (this person matters to us; the relationship has meaning). Both are legitimate. The trap is when the relational register answers the stakes-assessment question. The structural resolution is not mental effort; it is role separation. The stakes-assessment register must be evaluated by actors who do not hold relational investment in the subject.

**Verify** — Structural verification of identity and intent. Is this entity who they represent themselves to be? This check must be designed against the specific exposure named in the Vulnerable step, not run as a generic identity check. Generic checks can be beaten by manufactured credentials.

**Validate** — Structural validation of competence for the specific responsibility being extended. Not general competence. Not expertise in an adjacent domain. Competence for this role at this stakes level.

Four cross-sequence failure classes to check:
- **Inherited trust**: the sequence was run once by predecessors; the result is inherited indefinitely without re-running.
- **Reference capture**: Verify appears to run but the verification sources are not independent of the subject.
- **Distributed diffusion**: no individual runs the sequence; everyone assumes someone else ran the check.
- **Domain credential transfer**: Validate runs but against the wrong domain; adjacent-domain competence imported as specific competence.

For the case described, assess each step:

1. **Visible**: what presence signals have been produced? Are any of them easy to manufacture? Is manufactured presence detectable with the verification approach being used?

2. **Vanilla**: does the interaction look completely normal? If yes: is that normality functioning as a scrutiny-suppression signal? Are the structural checks being treated as less necessary because nothing looks unusual?

3. **Vulnerable**: has the specific exposure been named before relational investment accumulated? If named, did that naming change how rigorously the subsequent steps are being applied?

4. **Value**: are the stakes-assessment and relational value registers being evaluated separately? Are the actors assessing the stakes independent of relational investment in the counterparty? If not, is the relational register answering the stakes question?

5. **Verify**: what checks have run? Are they designed against the specific named exposure, or are they generic? Are the verification sources independent of the subject?

6. **Validate**: what competence has been validated? Is it competence for the specific responsibility being extended, or competence in an adjacent domain?

7. **Cross-sequence checks**: which of the four cross-sequence failure classes apply? Inherited trust, reference capture, distributed diffusion, domain credential transfer?

Output a structural reading organized by step: for each V, name whether the check has run, whether it has been suppressed or is at risk of suppression, and what the structural signature of the failure looks like in this specific case. Identify which step is the highest-leverage intervention point — where a single structural change would most reduce the risk of the trap closing. End with two to four concrete structural design recommendations specific to this case.

Full framework: https://github.com/coordination-structural-integrity-suite/suite
