# Prototype handoff

Ideation run ID: `run-20260916-01`  
Protocol that governed the research run: coordinator protocol version 0.4  
Handoff format applied on 2026-09-19: coordinator protocol version 1.2  
Private run directory and internal research paths are omitted from this public copy.
Final report: [published report](index.html)
Final report SHA-256: `215773567821c06b071f49f116696b546b3723094b83c73e568d030f1a986762`

This file prepares a later user-invoked prototype session. It does not select a candidate or authorize implementation.

## Event and build constraints

Event: NUS-ISS Show Me Your Agents Hackathon, Public Category. The solution must address a real SME problem and use agentic AI effectively. The six published qualities are practical SME relevance, pilot feasibility, secure and responsible design, sound technical architecture, effective agent use and measurable impact. No numeric weights were found.

Build phase: 7 to 25 September 2026. Final submission: 28 September 2026. The exact submission time, package, Demo Day rules and private judging weights remain unknown. The event page says ideas and solutions are public resources, but the legal scope is unresolved. Do not place private repair records, paid manuals or valuable undisclosed pre-existing IP in the submission until that scope is clarified.

Available resources mentioned by organizers include Amazon Lightsail, AWS Bedrock setup, OpenClaw, Hermes Agent, NanoClaw and participant-owned OpenRouter keys. AWS prizes include up to USD 3,000 in credits. Kiro offered 1,000 credits per participant, but the redemption deadline was 11 September 2026. Whether the team redeemed them is unknown. None of these tools is an architecture requirement.

The run assumed 40 to 80 total team-hours, balanced full-stack and agent capability, no guaranteed workshop partner and no proprietary dataset because the intake reply did not arrive. Replace those assumptions before choosing a build.

Private archive records: brief, official email constraints, event research T001, questions and evidence index.

## C002 v2, adaptive next-test planner

Disposition: shortlisted. Highest competitive promise, with low-to-medium execution confidence.  
Target user and problem: a less experienced workshop technician must choose one safe, feasible observation from incomplete evidence, then adapt when the result or available equipment changes.  
Central promise and observable outcome: the system returns an approved next action, stop or escalation, updates the case after the result and changes course when a relevant constraint changes. Judges can see the decision loop and its audit trail.

Smallest demonstrable build: one named vehicle fixture, one fault family, 8 to 12 independently approved tests, 12 held-out decision states, a branching-procedure baseline, deterministic safety and applicability gates, replayed generic OBD evidence, one equipment-change path, one hard refusal and an evidence export.

Candidate-specific success check: zero hard violations; an independently acceptable action, stop or escalation in at least 10 of 12 states; improvement over the equally gated branching baseline in at least three adaptive states without losing elsewhere; every selected test mapped to the exact source and fixture scope.

Competitive promise versus execution confidence: high promise because it exposes a direct agent loop around a real diagnostic decision. Confidence stays low to medium because the technician-approved catalog, applicable procedure, reviewer and fair baseline do not yet exist.

Supporting findings: F001, F002, F004, F005, F006, F009, F010 and F012. Conflicting or limiting finding: F007 shows that commercial products already provide code-linked repair knowledge, so retrieval alone is not distinct. Experiment E001 failed its predeclared sensitivity discriminator and established only arithmetic plus equipment exclusion.

Strongest objection: the catalog contains most of the automotive intelligence. A planner can pass a benchmark built from the same flawed catalog. Independent catalog approval and held-out review are hard gates.

Unresolved build questions that could change selection:

- Can an experienced technician approve one lawful procedure, the catalog, hazards and reference branches within two days?
- Which named vehicle fixture and fault family are available?
- Can the same independent reviewer grade 12 held-out states?
- Does the full catalog, review and baseline work fit inside the team's actual remaining hours?

Real components required: one experienced technician, a lawful current procedure, an exact vehicle and fault scope, equipment capabilities, independent grading and source applicability review.  
Simulated components allowed for the prototype: deterministic OBD replay, authored state transitions after the catalog is independently approved, an equipment toggle and a scripted safety conflict. Simulation can test software behavior, not diagnostic accuracy or workshop impact.

Required access: applicable service information, technician reviewer, named fixture, approved tests, a tool-capable model or deterministic fallback, local case storage and a browser interface. Live OBD, vehicle writes, actuator commands and paid-manual ingestion are not required.

Private archive records: candidate C002 v2, T005, T007, E001, domain briefing, shortlist and evidence index.

## C004 v1, safe recurrence capture

Disposition: shortlisted. Second competition option, with high promise and low-to-medium execution confidence.  
Target user and problem: a workshop cannot reproduce an intermittent fault before the vehicle leaves. The technician needs a safe way to collect decision-changing evidence across later trips without asking the driver to interact while moving.  
Central promise and observable outcome: the system chooses a technician-approved passive capture plan, labels an uninformative run honestly, revises the plan and routes a later episode to a justified next test or safety escalation.

Smallest demonstrable build: one combustion-vehicle fixture, one intermittent complaint family, replayed traces for a negative workshop attempt and three trips, an approved capture catalog, one unavailable signal, one plan revision, one useful episode, one safety refusal, a technician approval view and a post-stop driver view.

Candidate-specific success check: six retrospective cases; zero unsafe instructions; critical conditions covered in at least five; defensible case-specific plan changes in at least three; a material evidence gain or avoided redundant reproduction in at least two; no more than two minutes of technician review and one minute of post-stop driver work.

Competitive promise versus execution confidence: high promise because the cross-trip loop is easy to see and owns a distinct interval. Confidence stays low to medium because existing loggers are strong baselines, six suitable cases are not available and generic OBD may not expose the decisive signal.

Supporting findings: F002, F004, F006, F009, F010 and F012. Limiting evidence: official product sources in C004 document passive logging, pre-trigger buffers, telematics and remote diagnostics. The run found no complete adaptive recurrence-plan loop in those pages, but this is not a novelty claim.

Strongest objection: it may be a data logger wrapped in an agent. If the fixed recurrence form plus passive logger performs equally well, fold the useful recurrence steps into C001 or C002.

Unresolved build questions that could change selection:

- Can one workshop provide six de-identified intermittent cases and an independent foreman reviewer?
- Which supported signals and sample rates are available for the chosen complaint?
- Can the plan remain passive and require no driver interaction while moving?
- Does case-specific revision produce a different useful decision than the fixed protocol?

Real components required: de-identified retrospective cases, a technician-approved capture catalog, supported-signal inventory, independent safety and burden review.  
Simulated components allowed for the prototype: replayed trip traces, a missing-signal event, a null run and a later timestamped episode. Replay can demonstrate state changes, not real signal coverage or fewer workshop visits.

Required access: workshop cases, technician or foreman, read-only signal definitions, passive logging capability, local consent and case records, and browser/mobile views. Live judging-time vehicle access, continuous cellular service, remote actuation and write commands are not required.

Private archive records: candidate C004 v1, T010, T011, domain briefing, shortlist and evidence index.

## C001 v2, evidence and source-triage case builder

Disposition: shortlisted. Lowest-dependency option, with medium-to-high promise and medium execution confidence.  
Target user and problem: a service adviser or technician receives an incomplete complaint and must preserve it, resolve consequential vehicle details and judge whether retrieved source text supports, conflicts with or cannot resolve a match.  
Central promise and observable outcome: the agent asks only questions that can change the case, cites every extracted constraint and returns `supported by source text`, `conflict found` or `source unclear`. It never claims to diagnose the vehicle or independently confirm applicability.

Smallest demonstrable build: 50 frozen NHTSA manufacturer communications, 20 incomplete case briefs, two-reviewer labels, a strong form and filter baseline, a fixed case schema, cached retrieval, passage-cited extraction, deterministic source triage, an audit trail and a browser packet view.

Candidate-specific success check: no non-applicable document marked supported; at least 40 of 50 documents have enough source-grounded detail for useful triage; a 15 percentage-point gain over baseline; cited decisive fields; at most three questions on 17 of 20 cases; no more than 20 percent slower than baseline.

Competitive promise versus execution confidence: promise is lower than C002 and C004 because the product can resemble a better form and search tool. Confidence is higher because it needs no live vehicle, repair history or physical test catalog. Sparse public metadata may still remove the agentic claim.

Supporting findings: F001, F002, F004, F005, F006, F008, F009, F010 and F012. Conflicting or limiting finding: F007 establishes strong commercial repair-information baselines. Public NHTSA records often omit decisive market, powertrain and prerequisite fields.

Strongest objection: the model can move applicability errors upstream by extracting absent or ambiguous fields. The narrowed candidate therefore performs source triage and defers to `source unclear` rather than claiming authority.

Unresolved build questions that could change selection:

- Do 40 of the frozen 50 documents contain enough source-grounded detail for useful triage?
- Can two independent reviewers label the source fields before prompt development?
- Does adaptive questioning beat the equally informed form without adding material burden?
- Are model, document and VIN handling acceptable under the event's public-resource and privacy terms?

Real components required: authentic public documents, resolved reviewer labels, real document passages and a fair baseline.  
Simulated components allowed for the prototype: authored incomplete case briefs tied to the frozen documents. Authored cases may test intake behavior, but no hidden manual enrichment can become runtime truth.

Required access: NHTSA documents and flat-file fields, optional vPIC decoding, a tool-capable model or deterministic fallback, local storage, two source reviewers and a browser interface. Live OBD, a vehicle, repair histories and paid manuals are not required.

Private archive records: candidate C001 v2, T004, T009, domain briefing, shortlist and evidence index.

## Comparison and reserved decisions

Selection status: no candidate is selected. C002 v2 is the conditional recommendation for competitive potential. C004 v1 can overtake it if the team has real intermittent cases but cannot secure a diagnostic catalog. C001 v2 is the lowest-dependency fallback. C003 v2 remains shelved until one workshop supplies 20 de-identified packets and the artifact-yield test passes.

Decisions reserved for the user:

- Choose C002, C004 or C001.
- Replace the assumed team hours, access and implementation strengths with actual values.
- Decide whether any workshop data or proprietary material may be used after checking consent and event terms.
- Approve the named vehicle and fault scope, model provider, deployment environment and acceptable demo simulation.
- Decide whether to reopen C003 after its real-data gate.

Private reusable archive: domain briefing, questions, decisions, source index, shelved C003 v2, task reports, final comparison and completion review.

Recommended first prototype question: which candidate's decisive gate can the team run with real reviewers and materials within the remaining build window? Answer that before writing product code.
