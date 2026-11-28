## Engagement Objective

A read-only incident investigation system that helps junior engineers diagnose incidents faster and with more consistent, evidence-backed recommendations.

## Current Alignment

The system will initially be optimized for junior engineers.

To establish a reliable initial system, the pilot will focus on low-complexity incidents before expanding to higher-complexity cases.

The system is intended to speed up incident investigation by gathering relevant incident evidence and producing reviewable recommendations for the engineer. It will not take action or mutate enterprise systems.

The customer is aligned on the need for measurable improvement in incident investigation speed and consistency, with detailed success thresholds to be validated during follow-on discovery.

## In Scope

- 2-3 selected incident categories
- Low-complexity incidents only
- Defined pilot group
- Evidence-backed recommendations for engineer review

## Out of Scope for V1

- High-complexity incidents
- Broad rollout across the whole engineering org
- Autonomous remediation actions
- Incident categories outside the selected pilot set

## Out of Scope for This Document

- Detailed architecture
- Implementation plan
- Final cost model
- Detailed API contracts

## Provisional Success Metrics

These targets are provisional and need validation against pilot scope, measurement method, and baseline data.

- Reduce junior-engineer MTTD toward about 31 minutes
- Reduce junior-engineer MTTR toward about 95 minutes
- Improve consistency and quality of evidence-backed incident diagnosis

## Outstanding Questions

- Pilot scope: finalize supported incident categories, low-complexity definition, and pilot users
- Integration and security constraints: confirm accessible systems, auth/network controls, and API limitations
- Evaluation and release criteria: define sample size, review method, and thresholds for progressing beyond discovery

## Next Steps

- Follow-on technical discovery to resolve pilot scope, integration/security constraints, and evaluation/release criteria
- Use the follow-on discovery output to finalize the initial architecture and implementation plan.
