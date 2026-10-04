---
name: xean
description: Use when the user requests Xean or Xean/Copilot for independent mathematical or primary-source review, starts a version-bound review campaign, or needs to recover an interrupted, context-lost, decoder-limited, or already-guarded Xean attempt.
---

# Xean

Operate source-bound independent reviews through Xean's public kernel and a
qualified Copilot adapter. Keep report delivery separate from mathematical
acceptance.

Read [the workflow reference](references/workflow.md) before preparing or
recovering a campaign. Treat its dated commands, IDs, paths and capacities as
pinned examples, not a generic installer. Follow the repository's `deep-think`
requirements for substantive mathematics; retain analytic proof standards.

For a newly added skill in an active Copilot CLI session, run `/skills reload`
and check `/skills info xean` before named invocation. Distinguish a stale
subagent resolver from missing files: apply explicitly supplied, readable
trusted instructions without claiming named activation. Do not bypass access
denials or change global settings to repair discovery.

## Select the integration

Use public `Xean.open`, `openXeanStorage` and role/coordinator APIs with the
custom asynchronous `copilot.review` role. Read the verified `copilot-review.ts`,
`native-runner.ts`, `copilot-host.ts` and `run_review.py` before adapting them.
Treat `reviewApplication` as a local helper, not a built-in Xean constructor.
Do not select Copilot by giving its name to the Codex research constructor.

Inspect the installed CLI/SDK declarations and kernel identity. Preserve
configured/default Copilot selection by omitting the SDK `model` field.
Interpret this adapter's recorded `model: null` as that omission, not evidence
of a particular model. Request supported maximum reasoning and session-local
long context; verify actual root usage. Do not invent CLI flags, install or
upgrade dependencies, or change global settings to match historical examples.
Report missing adapter/runtime prerequisites explicitly.

## Execute the review

1. **Freeze scope.** Preserve dirty work and old editions. Snapshot complete
   required sources, hashes, base commit, definitions, proofs and imported
   premises. Number scopes and require one coverage row each; never grant a
   disputed theorem in the task.
2. **Register fresh inputs.** Create a new packet/campaign ID, operation UUID,
   task, argument, input manifest and database. Bind settings, source/runtime
   hashes, host, interpreter and helpers. Keep one attempt and one logical
   provider call per guarded request in this adapter.
3. **Qualify first.** Demonstrate successful primary web retrieval, then the
   actual long-context/PDF path. Requalify changed bindings. Authenticate
   title, edition and printed versus physical pages; inspect required
   hypotheses and proof applications, not search summaries.
4. **Own both processes.** On the pinned Windows setup, use the native Windows
   supervisor to launch Linux Bun/Xean through WSL and Windows Node/Copilot
   separately. Keep interop disabled. Verify the exclusive UUID/exit-code/
   host/stdout/stderr receipt before settling the provider call. Stop only
   owned children.
5. **Fail on loss.** Treat root truncation, compaction, reset, errors or an
   empty final answer as operational failure, never mathematical PASS or FAIL.
   Preserve the attempt; use new guarded inputs and a qualified runtime or
   smaller explicit scope. Never delete guards or explain away lost context.
6. **Bind evidence.** Decode UTF-8 JSONL using literal LF, not `splitlines()`.
   Require zero-based premise indices and exact quotes from successful
   observed primary fetches. Use task quotations only for explicit assumptions.
   An unclipped decoder result does not establish complete glyph recovery.
7. **Reconcile fully.** Read the complete root report and coverage table.
   Separate delivery, model verdict, evidence-bound verdict, coordinator
   disposition and human acceptance. Count canonical scopes once; reused
   calibration, recovery and internal model turns are not additional reviewers.
   Rebind source edits and obtain a fresh targeted check.
8. **Seal last.** Wait for all writers to exit. Retain stable files, databases
   and every nonempty WAL; record only confirmed-empty WAL/derived SHM
   exclusions. Verify the seal and live-source bindings. Exclude credentials,
   private journals and redistributed primary PDFs.

## Resolve misleading signals

| Signal | Required disposition |
|---|---|
| Old PASS; changed source hash | Preserve historical grade; freeze and review the new input. |
| Existing invocation/database/receipt | Stop replay; retain it and register a new request. |
| `long_context` label; smaller observed capacity | Record actual capacity; qualify before claiming the requested tier. |
| HTTP 200/unclipped text; missing header or proof | Record extraction gap; fetch an authenticated alternative representation or remain INCONCLUSIVE. |
| Kernel `completed` | Report validated delivery only, not whole-paper or human approval. |

Deliver exact source identity, observed model/effort/context, every scope's
grade, primary evidence, correction dispositions, preserved failures and
remaining boundaries. Never rewrite an adverse report or sealed packet.
