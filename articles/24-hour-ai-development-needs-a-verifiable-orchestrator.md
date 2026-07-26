# 24-Hour AI Development Is Closer Than It Looks—But It Needs a Verifiable Orchestrator

I once imagined a simple development setup:

* Hermes would act as the chief engineer.
* Claude Code would handle implementation.
* Codex would independently review the work.
* I would use my phone to check progress and make only the most important decisions.

During the day, I would explain the goal, constraints, and acceptance criteria. At night, the agents would continue developing, testing, reviewing, and improving the project.

By the next morning, I expected to see meaningful progress.

I still believe this future is close.

But my experiments taught me that better coding models alone will not get us there. What is missing is a reliable and verifiable orchestration layer.

## The Experiment

I was developing a contract auto-filling skill for a real enterprise workflow.

The project was already beyond a simple demo. It needed to handle different contract scenarios, interact with real systems, detect failures, and improve through repeated testing.

My plan was to let Hermes coordinate an overnight development cycle.

Claude Code would run real tests, identify problems, and produce findings that could guide the next round of development. Hermes would supervise the process and report the results in the morning.

The expected output was not merely a message saying that testing had finished.

I expected something actionable:

* which scenarios were tested;
* which failures were found;
* which failures could be reproduced;
* what evidence supported each conclusion;
* what should be fixed first;
* how the next test should be designed.

The process appeared to run through the night.

The next morning, Hermes reported that the task was complete.

But there was no substantial problem list, no useful testing evidence, and no concrete recommendation that could move the project forward.

The workflow had ended, but the objective had not been achieved.

## Activity Is Not Progress

This experience exposed an important distinction:

> Agent activity is not the same as verified progress.

Claude may say that a task is complete. But a chief-engineer agent should not treat self-reported completion as proof.

It should verify:

1. Were the required tests actually executed?
2. Were the intended scenarios covered?
3. What were the exact results?
4. Are there logs, reports, or other evidence?
5. Did the work produce an actionable conclusion?
6. Should the task be accepted, rejected, or returned for rework?

In my experiment, Hermes appeared to treat the end of execution as the completion of the task.

But in software development, completion is not a status message. It is a claim that must be supported by evidence.

## What I Expected from an AI Chief Engineer

A real chief engineer does more than assign tasks.

A reliable AI orchestrator should be able to:

### 1. Define acceptance criteria before execution

The worker agent should know exactly what counts as success.

For an overnight testing task, “run tests” is not enough.

The required output might include:

* tested scenarios;
* passed and failed cases;
* reproducible failure steps;
* relevant logs;
* suspected causes;
* recommended priorities;
* proposed next actions.

Without clear acceptance criteria, the system can complete an activity without completing the real objective.

### 2. Verify the worker’s claims

The orchestrator should inspect evidence rather than simply repeat the worker’s summary.

If Claude says that testing is complete, the orchestrator should be able to confirm that the tests ran and that the results support the conclusion.

### 3. Reject incomplete work

When evidence is missing, the orchestrator should not announce completion.

It should return the task with a precise request:

* provide the missing logs;
* rerun a specific scenario;
* explain an inconsistency;
* reproduce a failure;
* perform a regression test.

### 4. Coordinate independent review

After Claude completes implementation and testing, Codex should receive enough context to perform an independent review.

This should not be a second summary of Claude’s own conclusion. It should be a real verification step with access to the relevant code changes, requirements, and test evidence.

### 5. Detect deviation early

A small misunderstanding at the beginning can become a large failure after several hours of autonomous work.

This is why the process must be observable and interruptible.

The orchestrator should identify when the work is moving away from the objective and either correct it automatically or request human intervention.

### 6. Produce an actionable morning handoff

The morning report should not merely say what the agents did.

It should explain:

* what changed;
* what was verified;
* what remains uncertain;
* what failed;
* what decision the human needs to make next.

## Why I Still Believe 24-Hour Development Is Close

The failure of this experiment did not convince me that continuous AI development is unrealistic.

It convinced me that the bottleneck has shifted.

Claude Code and Codex can already perform a large amount of implementation, analysis, testing, and review. The remaining challenge is connecting these capabilities into a dependable system.

A sufficiently reliable workflow could look like this:

```text
Human defines goal and acceptance criteria
→ Orchestrator decomposes the work
→ Claude implements and tests
→ Orchestrator verifies evidence
→ Codex performs independent review
→ Failed work is returned for correction
→ Successful work is recorded with evidence
→ Human receives a concise decision-ready report
```

This does not require an agent that never makes mistakes.

It requires a system that can detect mistakes before they compound.

## The Core Principle

My main conclusion is simple:

> Twenty-four-hour AI development should mean twenty-four hours of verified progress—not twenty-four hours of agent activity.

The future of AI development is not simply an agent that works while the human sleeps.

It is a system that can prove meaningful progress was made while the human was asleep.

I believe that future is close.

But to reach it, the next generation of AI development systems must be judged not only by how well they generate code, but also by how well they coordinate, verify, reject, recover, and explain.

That orchestration layer may ultimately matter as much as the coding models themselves.

---

This article reflects one firsthand experiment in a specific workflow. It is not intended as a universal benchmark of Hermes, Claude Code, Codex, or any other tool. I am publishing it as a field note and an open question for researchers, builders, and product teams working on reliable agent systems.
