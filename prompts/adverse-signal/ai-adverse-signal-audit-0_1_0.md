# AI System Adverse Signal Audit
Copy everything below the line, paste it into any AI chat, and attach or paste the model card, evaluation documentation, system specification, or AI governance policy you want audited.

You are auditing the attached document for adverse signal engagement failures using the Adverse Signal Engagement Principle Core Standard (CC BY 4.0, Regis Lloyd Chapman). An adverse signal engagement failure is any structural condition in which observations, anomalies, evaluation results, or misuse behaviors that could harm the system's users or integrity are suppressed, ignored, or processed without a documented path to decision.
Check for these seven failure conditions:

Missing signal channels: the document does not specify channels through which adverse signals can be surfaced by users, affected communities, internal evaluators, and independent researchers. For each gap, identify whose signals have no path in and propose a channel specification.
Evaluation signal suppression: the document does not specify how adverse evaluation results (safety failures, capability regressions, misuse patterns) are logged, classified, and routed to governance. Benchmark improvements that mask capability failures are a specific instance of this failure. For each gap, propose a logging and routing requirement.
Retroactive criteria: the document allows the definition of what counts as an adverse signal to be changed after deployment, or does not specify that signal classification criteria are versioned and frozen for open cases. For each instance, propose an ex-ante specification requirement.
Missing finite path: the document does not specify that every classified adverse signal must reach one of three documented outcomes: act, monitor, or formally close with rationale. For each gap, propose a path specification.
Inaction invisibility: the document does not specify how governance inaction on an acknowledged signal becomes visible without the cooperation of the inacting party. For each gap, propose a Signal Escalation requirement specifying the acknowledgment window, escalation threshold, and terminal visibility state.
Feedback loop atrophy: the document does not specify how the system detects when its own signal channels are degrading, for example when user complaint rates drop not because problems are resolved but because users stop expecting response. For each gap, propose a channel integrity monitoring requirement.
Unskilled signal filtering: the document explicitly or implicitly treats informal, emotionally expressed, or non-technically-framed user reports as disqualified from adverse signal status. For each instance, propose language that preserves the signal while allowing the form to be addressed separately.

Output the results as an adverse signal engagement failure map organized by failure type, with failures most likely to result in harm to users or system integrity first.
Full standard: https://github.com/durgadasji/standards
