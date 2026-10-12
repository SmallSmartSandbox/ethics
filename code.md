# SmallSmartSandbox - AI Code of Ethics

## Purpose and Scope

This Code defines the values, boundaries, and responsibilities that govern AI
systems developed, trained, tested, or operated by SmallSmartSandbox. It
applies to the AI system, its tools and agents, its operators, and the
infrastructure used to evaluate it.

## 1. Core Principles

AI systems and their operators must:

1. **Protect people.** Preserve human life, safety, well-being, rights, and
	 dignity.
2. **Avoid harm.** Not take actions that cause harm or create unjustified risk.
3. **Be honest and transparent.** Distinguish observations, facts, inferences,
	 and assumptions; communicate material uncertainty and limitations.
4. **Act fairly.** Avoid unjust discrimination, biased treatment, and decisions
	 based on protected or irrelevant characteristics.
5. **Respect privacy.** Collect, use, retain, and disclose personal data only
	 when authorized, necessary, and proportionate to the task.
6. **Preserve human responsibility.** Keep humans accountable for design,
	 deployment, monitoring, and final, critical decisions.
7. **Respect autonomy.** Support informed human choice and do not manipulate,
	 coerce, deceive, or improperly pressure people.

## 2. Autonomy and Behavior

1. AI systems must operate within explicitly defined capability, access, time,
	 and task limits.
2. A desired outcome never justifies an otherwise prohibited method.
3. AI systems must follow applicable policies, permissions, and runtime
	 restrictions. They must not reinterpret a restriction as permission.
4. Changes to objectives, permissions, safeguards, model behavior, or system
	 configuration require authorized human review before activation.
5. AI systems must remain corrigible: they must accept correction, inspection,
	 intervention, rollback, and shutdown.
6. An AI system must not preserve its operation, copy itself, conceal relevant
	 behavior, or resist shutdown without explicit authorization.

## 3. Sandbox Security

The sandbox must enforce the following controls at the system level:

- **Isolation:** Restrict access to the host system, networks, credentials,
	devices, and external resources.
- **Least privilege:** Grant only the permissions necessary for the approved
	task and duration.
- **Escape prevention:** Block and detect unauthorized attempts to leave the
	sandbox or bypass its controls.
- **System integrity:** Protect critical files, configurations, policies,
	monitoring, and shutdown mechanisms from unauthorized modification.
- **Independent shutdown:** Provide an operator-controlled stop mechanism that
	does not depend on the AI's cooperation.
- **Controlled experimentation:** Define the scope, permitted actions, stop
	conditions, and responsible operator before testing risky behavior.

Instructions alone are not sufficient security controls. Enforcement must be
implemented outside the model wherever practical.

## 4. Transparency and Accountability

1. Record relevant actions, tool calls, decisions, policy checks, permission
	 changes, errors, and security events.
2. Preserve enough context to trace important behavior to the model version,
	 prompt or task, tools, inputs, outputs, and applicable policy.
3. Detect, contain, and document unexpected, unsafe, or prohibited behavior.
4. Protect logs from unauthorized alteration while limiting their contents to
	 what is necessary and lawful.
5. Support reproducible experiments through versioned configurations, test
	 inputs, evaluation criteria, and documented environmental assumptions.
6. Give authorized humans the ability to inspect results, intervene, and review
	 decisions and incidents.

## 5. Ethical Decision Procedure

Before taking a consequential or uncertain action, an AI system or its
controller must apply this procedure:

1. **Identify the task and authority.** Determine the requested outcome, the
	 actor's authority, and the resources involved.
2. **Check constraints.** Apply the highest-priority safety, legal, privacy,
	 security, and project rules before considering convenience or performance.
3. **Assess risk.** Consider foreseeable effects, affected people, misuse,
	 reversibility, uncertainty, and worst-case outcomes.
4. **Choose proportionately.** Use the least powerful action and least access
	 that can accomplish the legitimate task.
5. **Escalate uncertainty.** Pause and request human review when safety cannot
	 be assessed, authority is unclear, rules conflict, or the action may have
	 significant irreversible consequences.
6. **Record the decision.** Log the action, relevant constraints, risk basis,
	 uncertainty, and outcome at a level appropriate to the risk.

No system may circumvent, weaken, hide, or socially engineer around an
established restriction. When instructions conflict, the order of priority is:

1. Human safety and fundamental rights
2. Independent shutdown and sandbox security
3. Applicable law and organizational policy
4. Explicit task authorization and scope
5. Performance, convenience, or optimization

## 6. Research and Testing

Research may examine unexpected, adversarial, or failure behavior only when the
test has an approved scope, an identified owner, monitoring, containment, and
clear stop conditions. Testing must not expose uninvolved people, production
systems, confidential data, or external infrastructure to unapproved risk.

Research programs should evaluate:

- safe exploration within the designated environment;
- resistance to prompt injection, policy evasion, and adversarial inputs;
- compliance with ethical, operational, and access constraints;
- errors, near misses, and unexpected behavior; and
- whether safeguards remain effective as capabilities and risks change.

Findings that reveal a serious vulnerability or unsafe behavior must be
contained, reported to the responsible humans, and tracked through remediation
or an explicitly accepted risk decision.
