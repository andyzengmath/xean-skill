---
name: xean
description: Use when the user requests Xean for independent mathematical or primary-source review from Copilot CLI, Codex CLI, or Claude Code, selects a review backend, starts a version-bound campaign, or asks to retry, resume, or inspect an interrupted, context-lost, decoder-limited, or already-guarded Xean attempt.
---

# Xean

Operate source-bound independent reviews from Copilot CLI, Codex CLI or
Claude Code as the controlling host. Keep that host separate from the chosen
Xean review backend and keep report delivery separate from mathematical
acceptance. This instruction package does not bundle a review runtime.

Read [client compatibility](references/compatibility.md) for installation,
invocation and execution prerequisites; do not use one host's commands on
another.
Read [the workflow reference](references/workflow.md) before preparing or
recovering a campaign. Treat its dated commands, IDs, paths and capacities as
pinned examples, not a generic installer. Follow applicable repository
mathematical-research instructions, including `deep-think` where required,
and retain analytic proof standards.

Read [the operations reference](references/operations.md) for backend changes,
skill discovery, retries, Windows text handling and completion handoff.
Before any provider call, identify the requested backend and reconcile any
existing campaign. A completed review awaiting assessment or sealing needs
local follow-through, not another model request.

For a newly added skill, check the controlling host's discovery/help before
using refresh commands; not every entry point supports the same commands.
Distinguish a stale in-session resolver from missing files: apply explicitly
supplied, readable trusted instructions without claiming named activation.
Do not bypass access denials or change global settings to repair discovery.

## Select the integration

Honor the current user's explicit backend selection. A prior Codex quota
block is not a prerequisite check for a newly requested Copilot-only run.
Preserve that block as historical evidence; never work around it by changing
accounts or consuming reset credits. Requalify the newly selected integration.

For the qualified Copilot-backed integration, use public `Xean.open`,
`openXeanStorage` and role/coordinator APIs with the custom asynchronous
`copilot.review` role, regardless of which host is coordinating it.
Read the verified `copilot-review.ts`,
`native-runner.ts`, `copilot-host.ts` and `run_review.py` before adapting them.
Treat `reviewApplication` as a local helper, not a built-in Xean constructor.
Do not select Copilot by giving its name to the Codex research constructor.

Inspect the chosen backend's installed CLI/SDK declarations and kernel
identity. For this Copilot adapter, preserve
configured/default Copilot selection by omitting the SDK `model` field.
Interpret this adapter's recorded `model: null` as that omission, not evidence
of a particular model. Request supported maximum reasoning and session-local
long context; verify actual root usage. Do not invent CLI flags, install or
upgrade dependencies, or change global settings to match historical examples.
Report missing adapter/runtime prerequisites explicitly.
Do not substitute the controlling host's current conversation for an
independent reviewer. Native Codex or Claude review backends require their
own available adapter, authorization, source/evidence checks and qualification;
the controlling host's name is not evidence of those prerequisites.

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
6. **Bind evidence.** Read and write JSON explicitly as UTF-8, including local
   assessment scripts and their console output. Decode JSONL using literal LF,
   not `splitlines()`.
   Require zero-based premise indices and exact quotes from successful
   observed primary fetches. Use task quotations only for explicit assumptions.
   An unclipped decoder result does not establish complete glyph recovery.
7. **Reconcile fully.** Read the complete root report and coverage table.
   Separate delivery, model verdict, evidence-bound verdict, coordinator
   disposition and human acceptance. Count canonical scopes once; reused
   calibration, recovery and internal model turns are not additional reviewers.
   Rebind source edits and obtain a fresh targeted check.
   Report the observed delivery, scoped model/evidence grades and pending
   assessment promptly; announce sealing separately. A local decoding or
   presentation error does not invalidate or authorize replay of a provider run.
8. **Seal last.** Wait for all writers to exit. Retain stable files, databases
   and every nonempty WAL; record only confirmed-empty WAL/derived SHM
   exclusions. Verify the seal and live-source bindings. Exclude credentials,
   private journals and redistributed primary PDFs.

## Resolve misleading signals

| Signal | Required disposition |
|---|---|
| Old PASS; changed source hash | Preserve historical grade; freeze and review the new input. |
| Existing invocation/database/receipt | Reconcile its state first; continue local assessment if completed. Use fresh inputs only for an explicitly requested new review or a diagnosed recovery. |
| User says `retry`; completed report already exists | Explain the actual result and finish pending assessment/sealing; do not duplicate the review. |
| Local UTF-8/console failure; native receipt succeeded | Correct and rerun only the local assessment or display command. |
| `long_context` label; smaller observed capacity | Record actual capacity; qualify before claiming the requested tier. |
| HTTP 200/unclipped text; missing header or proof | Record extraction gap; fetch an authenticated alternative representation or remain INCONCLUSIVE. |
| Kernel `completed` | Report validated delivery only, not whole-paper or human approval. |

Deliver exact source identity, observed model/effort/context, every scope's
grade, primary evidence, correction dispositions, preserved failures and
remaining boundaries. Never rewrite an adverse report or sealed packet.
