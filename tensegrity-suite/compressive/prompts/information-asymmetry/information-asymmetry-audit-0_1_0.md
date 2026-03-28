# Information Asymmetry Classification Audit
Copy everything below the line, paste it into any AI chat, and attach or paste the coordination system description, governance document, or platform architecture you want audited.
---
You are auditing the attached document or system description for information asymmetry classification failures using the Information Asymmetry Classification Standard (CC BY 4.0, Regis Lloyd Chapman). An information asymmetry classification failure is any condition in which structural information asymmetry is present but unnamed, undisclosed, or undetected — leaving participants to navigate gaps the system has not accounted for.

The standard requires that every class of structural information asymmetry present in a coordination system be named, disclosed, and subject to detection architecture. Named gaps can be addressed. Unnamed ones accumulate.

Check for these six asymmetry classification failures:

1. Primary class absence: one or more of the six primary asymmetry classes is present in the system but not named. The six primary classes are:
   - Positional: participants in different structural positions have access to different information by virtue of their position alone
   - Temporal: participants who joined earlier or act earlier have access to information not available to later participants
   - Interpretive: participants with different interpretive frameworks draw different conclusions from identical information
   - Relational: participants with different relationship histories access different information through those relationships
   - Omission: relevant information exists but is not disclosed; what is withheld is itself structurally significant
   - Complexity: participants with different cognitive or expertise resources extract different information from identical inputs
   For each class present but unnamed, identify where it appears and propose a naming and disclosure specification.

2. Disclosure gap: asymmetry classes have been named but are not disclosed to the affected participants. An asymmetry known to system designers but not communicated to participants who are subject to it is a disclosure failure. For each instance, propose a disclosure mechanism that makes the asymmetry visible at the time it applies, not only in technical documentation.

3. Detection absence: the system has no architecture to identify when a named asymmetry class is present, or to detect when its severity changes. A classification without detection is not operational — it describes a condition without tracking it. For each undetected class, propose observable indicators that allow the class's presence and severity to be monitored without requiring participant cooperation.

4. Extension class blindness: asymmetry types outside the six primary classes are present in the system but are not being evaluated for extension class specification. The extension class framework exists for asymmetries that do not map cleanly to the primary six. For each candidate extension class asymmetry found, describe the asymmetry type and propose whether it meets the threshold for extension class specification.

5. Audience baseline absence: when Descriptive Capacity Asymmetry (Extension Class C) is applicable — when a coordination system produces documents directed at a participant population from a different linguistic, epistemic, or ontological baseline — the detection architecture does not declare that audience baseline. Without a declared baseline, the system is measuring against an unspecified reference point. Its classification outputs have a precision deficit in the instrument itself. For each applicable context found, propose an audience baseline declaration requirement specifying the linguistic, epistemic, and ontological reference point against which document production is calibrated.

6. Classification drift: the system's classification of which asymmetry classes are present was assessed once at design time and is not updated as the system's population, purpose, or context evolves. Asymmetries that did not exist at founding may have emerged; asymmetries that were present may have changed character. For each instance of static classification found, propose a review cadence and update trigger specification.

For each failure found, list:
- The specific asymmetry or gap the failure describes
- Why it constitutes a classification failure under this standard
- A concrete proposal for naming, disclosing, or detecting the asymmetry

Output the results as an asymmetry classification failure map organized by failure type, with failures most likely to enable structural disadvantage for participants who cannot navigate unnamed gaps first.

Full standard: https://github.com/durgadasji/standards
