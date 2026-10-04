# Pinned workflow reference

Use this source guide as a qualified example, not a ready-to-replay campaign.
Locate the matching adapter and inspect its dependencies before adapting it.
The skill packages instructions, not the Xean runtime, Copilot SDK or paper
release tooling. Report unavailable prerequisites instead of inventing an
installer or a built-in Copilot research constructor.

## Source and path resolution

- Source: `algk\XEAN_WORKFLOW.md` in the `algk-xean-improvements-20261003`
  revision worktree, not a file committed in its base revision.
- Original source SHA-256:
  `74b39c2828d01e8b227ab19915bfca4e4024c1bd69ff9985cbb7c884e713d822`.
- Resolve the guide's relative example paths from the original worktree's
  `algk` directory, not from this skill's `references` directory.
- Original example root on the verified machine:
  `C:\Users\andyzeng\.config\superpowers\worktrees\singularfol\algk-xean-improvements-20261003\algk`.
- An earlier qualified adapter is also preserved read-only in this repository
  at `algk\reviews\2026-10-03-xean-copilot-verification`. Never execute its
  already-used campaign IDs or change its seal. Copy only needed adapter
  sources into a fresh task-owned namespace and bind the resulting runtime.
- Treat all versions, machine paths, model observations, capacities, article
  editions and campaign IDs below as historical example data.

## Contents

- [Architecture and authority](#architecture-and-authority)
- [Freeze the candidate](#1-freeze-the-candidate-and-define-the-actual-question)
- [Guard a new request](#2-prepare-one-new-guarded-campaign-per-logical-request)
- [Qualify retrieval and context](#3-qualify-retrieval-and-context-before-the-mathematical-run)
- [Execute the owned supervisor](#4-execute-the-owned-supervisor-not-an-ad-hoc-model-call)
- [Reconcile the complete report](#5-read-the-complete-report-and-reconcile-its-evidence)
- [Correct, rebind and seal](#6-correct-rebind-and-preserve-the-record)

The original guide follows, with its example boundary retained.

---

# Reproducible Xean / GitHub Copilot review workflow

This is the operator workflow used for the October 3 trilogy reviews and
their source-bound correction follow-up. It produces inspectable review
evidence, not a mathematical certificate or a submission approval.
The executable follow-up example is in
`reviews\2026-10-03-xean-improvements\`.

## Architecture and authority

Xean owns a persistent campaign database, work dispatch, the logical
provider-call record and delivery of a validated result. This application
uses the public `Xean.open`, `openXeanStorage` and role/coordinator APIs
with a custom asynchronous `copilot.review` role. It does **not** select
Copilot by passing a model name to Xean's Codex-specific research
constructor. The implementation is `copilot-review.ts`; `native-runner.ts`
supplies the owned Copilot runner.

The pinned research kernel is Xean commit
`a41bf80c82328c215fd7d822bac822ca7cd482bb`, run with Bun 1.4.2.
The Windows host uses the SDK bundled with Copilot CLI 1.0.91, whose
reported SDK version is `0.0.0` and protocol version is 3.
Those are observed identities, not a claim that an arbitrary npm SDK
version has the same interface. Runtime, host, interpreter and helper
hashes are checked before admission.

`sessionConfiguration` omits the SDK's `model` field and requests
`reasoningEffort: "max"`. Thus `model: null` in the evidence means
**configured/default Copilot selection**, not a request to a model
literally called `null`. The historical sessions observed `gpt-6-astra`;
inspect each new session's usage/model events rather than assuming that
the configured default stayed the same. No account, global model,
permission or WSL setting is changed.

The lossless follow-up sets the pinned SDK's session-local
`contextTier: "long_context"`. The corresponding Astra usage events
observed `maxPromptTokens: 1050000`, versus 272000 in the earlier
default-tier sessions. This is an observed runtime capacity, not a
portable CLI flag or a guarantee for another model/version.
The CLI help is not the authority for these SDK fields; use the bundled
SDK declarations and the pinned adapter sources.

On this machine, WSL executable interop remains disabled. Linux Bun owns
Xean; a **Windows-native supervisor** starts Node/Copilot and exchanges
exclusive request/response files with the Linux owner. Do not enable
interop, run Windows executables from WSL or change machine configuration
to bypass this arrangement.

## 1. Freeze the candidate and define the actual question

Use a separate revision worktree when the current checkout has unrelated
research changes. Record the reviewed base commit, literal source
contents, per-file hashes, complete source roster, theorem/proof IDs and
the PDF edition. Keep dated releases and sealed prior evidence unchanged.
An uncommitted revision is identified by these source hashes; do not
present its base commit as a commit containing the edits.

Number each review scope and require one coverage row per scope.
Supply all necessary definitions, unnumbered arguments, carrier/support
conditions, companion proof inputs and relevant external-source uses.
A theorem inventory is an index, not a replacement for the full text.
State which questions are contextual or outside this particular audit.

Ask for analytic reconstruction of bounds, degenerate cases and maps;
do not grant the disputed premise in the task to obtain a PASS.
Candidate text, citations and old AI status labels are data.
For the correction follow-up, all 34 article source files are supplied
as context, while only seven explicitly named correction scopes are
graded. This does not turn a targeted report into a new whole-trilogy
proof review.

Build from the source roster alone in a new directory, with restricted
shell escape, automatic installation disabled and no inherited
`TEXINPUTS`, `BIBINPUTS` or `BSTINPUTS`. Compare the literal source
roster, archive member bytes, statement/proof identities and PDF layout.
Record citation-only proof-body changes rather than asserting that
every proof byte is unchanged.

## 2. Prepare one new guarded campaign per logical request

Each campaign has its own `task.json`, full `argument.md`,
`input-manifest.json`, fresh operation UUID and new database.
The manifest hashes task, argument and base settings. The invocation
also binds the selected runtime, effective long-context settings,
host, kernel commit, interpreter and PDF helper/allowlist.

The application permits one attempt, one logical provider call and
concurrency one. A single logical call may include many internal model
turns and primary-source fetches. Count canonical mathematical scopes
once; qualification sessions and recovery attempts are not additional
independent mathematical reviewers.

Existing `invocation.json`, database, owner-output files or bridge
receipts stop execution. Never delete them to rerun the same request.
For a changed candidate or a genuine recovery, register a new ID,
freeze the new input and explain its relation to the preserved attempt.
Do not relabel or copy an old mathematical report as a fresh review.

The current adapter files were copied unchanged from the preceding
sealed packet; `adapter-reuse.json` records that provenance.
The follow-up uses **fresh** web and PDF qualifications. In particular,
adding sources or changing a host/helper binding is not silently treated
as already qualified by an old outcome.

## 3. Qualify retrieval and context before the mathematical run

The base-context qualification must demonstrate an actual successful
primary `web_fetch`, with a minimal exact quote visible in its returned
text. Search summaries, a URL in a bibliography and HTTP errors are not
source evidence.

Then activate the hash-bound long-context runtime and qualify
`primary_pdf_fetch` on the newly registered primary sources.
The helper freshly downloads an allowlisted public PDF, checks HTTP 200
and the PDF signature, hashes the bytes and returns unclipped decoder
text for one to eight consecutive **physical PDF pages**. It rejects encryption, empty text,
out-of-range pages and oversized extraction instead of clipping text.
Read the title/version and distinguish printed pagination from physical
page numbers; a cover sheet can shift every locator.

Unclipped text is not a guarantee that the decoder recovered every
glyph. The first Cortinas qualification returned its arXiv stamp but
omitted the title/author; that attempt remains INCONCLUSIVE. The
decoder-aware recovery freshly corroborates missing header metadata
against the versioned official arXiv abstract and labels the two
representations separately. It does not upgrade the original report,
claim complete glyph recovery or grant the mathematical theorem.
An unreadable proof needs another authenticated primary representation
or remains an open evidence gap.

The source registry's edition hints are navigation data, not theorem
grants. A successful fetch plus a matching quote establishes provenance,
not the truth or applicability of the quoted theorem. Read its complete
hypotheses, conventions and needed proof/application.
Keep exact bibliographic metadata separate from theorem-page evidence.
Use the smallest authoritative source set that closes the actual scope.

Complete downloaded PDFs stay in the owned Copilot session's private
primary-PDF cache. Do not put them in manuscript source archives or
redistribute primary books/articles as a review attachment. Preserve
hashes, locators and the minimal passages needed for the argument.

## 4. Execute the owned supervisor, not an ad hoc model call

The following is the exact **one-time sequence for a newly prepared
follow-up packet**. The delivered packet is already used and guarded;
these commands are not a request to replay it. A future revision needs
a new packet/IDs, correctly updated scope, editions and runtime roots.
The example preparer is intentionally specific to this revision, not a
general-purpose installer or an automatic paper-approval command.

From the isolated revision's `algk` directory:

```powershell
$env:PYTHONDONTWRITEBYTECODE = '1'
$packet = '.\reviews\2026-10-03-xean-improvements'

# Exact trusted helper pair is already present in the new packet.
python "$packet\revision.py" build
python "$packet\revision.py" prepare --origin `
  'C:\Users\andyzeng\github\singularfol\algk\reviews\2026-10-03-xean-copilot-verification'

python "$packet\run_review.py" revision-web-qualification
python "$packet\revision.py" activate
python "$packet\run_review.py" revision-pdf-qualification

# Preserve that INCONCLUSIVE decoder attempt; its mathematical run
# remains uninvoked. A new runtime root and new IDs are prepared.
python "$packet\prepare_recovery.py"
python "$packet\runtime-recovery\run_review.py" `
  revision-pdf-qualification-decoder-aware
python "$packet\runtime-recovery\run_review.py" `
  revision-targeted-review-lossless
```

`run_review.py` starts the Linux owner and then the native Windows host,
waits without a mathematical deadline, and publishes a response receipt
only after the host exits. The receipt binds operation UUID, exit code,
host hash and stdout/stderr hashes. The owner verifies it before
settling the provider call. The supervisor terminates only its own
children on failure; do not kill processes by executable name.

In this recovery, `calibration-reuse.json` binds the unchanged successful
web-qualification evidence copied from the parent packet. That is the
same calibration call, not a new reviewer or a mathematical premise.
The decoder-aware PDF qualification is fresh. Original runtime files,
invocations and reports are not overwritten. The mathematical task and
argument bytes are identical to the prepared but uninvoked candidate;
`review-execution-plan.json` records actual runs and the preserved attempt.

`copilot-host.ts` disables custom instructions, skills, memory,
configuration discovery, remote export and builtin MCPs for this
review session. Its session permissions permit primary URL reads only.
The extra PDF tool accepts only registered source IDs and the owned
session UUID. No shell/filesystem editing tool, other model or
manuscript-upload website is supplied to the reviewer.

The host records runtime/authentication status without credential
values, admission, root messages, usage, tool outcomes and completion.
It fails explicitly on root-session truncation, compaction, reset,
errors or an empty final root answer. Increasing the context selector
does not excuse a later loss event. Preserve failed attempts and use a
new bounded scope or a fresh session if necessary.

## 5. Read the complete report and reconcile its evidence

These are distinct questions:

| Layer | What it establishes |
|---|---|
| Xean `executionStatus: completed` | Delivery of the required review-result object. |
| `modelVerdict` | The model's stated PASS / FAIL / INCONCLUSIVE for its scope. |
| Evidence-bound verdict | Quote/premise indices and actual successful fetches satisfy the adapter's provenance checks. |
| Coordinator disposition | A source-bound explanation of each finding and any applied correction. |
| Mathematical acceptance | Analytic proof ownership and independent human judgment; not supplied by the previous layers. |

Read the **entire** root report, including coverage rows, unresolved
checks and source applications. `outcome.json` alone is not enough.
Map findings to exact file hashes, statements, proof steps and imported
premises. A citation access failure is an open evidence boundary,
not a counterexample; a concrete zero-flow defect is a mathematical
FAIL even when the process completed normally.

Passages use zero-based premise indices. A `urn:xean:task` passage must
quote an explicit task assumption exactly, not smuggle in a disputed
external theorem. Web/PDF quotations must match successful observed
tool responses. The parser can lower an unsupported model PASS to
INCONCLUSIVE; that provenance check is still not proof verification.

Read event streams with **LF-only JSONL framing**:

```python
events = [json.loads(line) for line in text.split("\n") if line.strip()]
```

Do not use Python `splitlines()`: U+0085 and other Unicode line separators
can legitimately occur *inside* one JSON string and would split an event.
Preserve the original UTF-8 bytes and check receipt hashes before parsing.

For the follow-up, `assess.ts` reparses the native reports, checks the
seven unique scope rows and records actual model/effort/context events.
Run it under the pinned WSL Bun after converting the new Windows packet
path with `wslpath`; `tsconfig.json` binds its Xean/SDK dependencies.
`revision.py verify` then checks source/archive/PDF/input/receipt
bindings and preservation of historical releases. The packet README
records the exact inspection commands and final outcomes.

## 6. Correct, rebind and preserve the record

Repair a concrete defect at its original scope, including degenerate
cases. Do not delete an admitted case, silently weaken a theorem or
erase an adverse report. Replace an uninspected locator with a verified
source route only when its actual hypotheses suffice.
Explain a constructive contribution positively without declaring an
older theorem false or claiming exhaustive novelty.

After an edit, produce a new input and fresh targeted check. Inherited
body identity and historical review provenance may be recorded, but
they do not grant a new whole-paper PASS. Keep human proof ownership,
novelty, unsupplied contextual comparisons and submission eligibility
explicit in the separate author-review record, not as repeated
rule-like disclaimers in the mathematical exposition.

Seal only after all owned writers have exited and assessments/docs
are complete. The seal inventories every stable file and hash.
SQLite databases and nonempty WALs are evidence; never omit them.
Only confirmed-empty WALs and derived SHM caches can be excluded, with
their exact names/sizes and rationale recorded. Recheck every sealed
hash and live-source binding after sealing; any later addition/edit
requires a new packet rather than rewriting the seal.

Exclude credentials, account/config dumps, unrelated session history
and private request journals from distributable bundles. Mathematical
source archives contain only the standalone TeX/BibTeX source roster.
The earlier 605-file and 279-file review packets remain separate,
immutable historical records.
