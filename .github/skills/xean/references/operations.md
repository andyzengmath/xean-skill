# Xean review operations

Use these rules with the qualified adapter in `workflow.md`. They describe
operational choices, not mathematical acceptance or a generic installer.

## Contents

- [Select the current route](#select-the-current-route)
- [Resolve skill discovery](#resolve-skill-discovery)
- [Reconcile before retrying](#reconcile-before-retrying)
- [Handle Windows text losslessly](#handle-windows-text-losslessly)
- [Report completion before sealing](#report-completion-before-sealing)
- [Keep review accounting source-bound](#keep-review-accounting-source-bound)

## Select the current route

Read the latest explicit backend request before inspecting old runtime state.
For a Copilot-only request, use the qualified public-kernel `copilot.review`
adapter. Do not invoke or recheck Codex merely because an earlier campaign
used it, and do not pass a Copilot model name to a Codex-specific constructor.

Keep old quota/authentication failures unchanged. An authorized backend
change requires a fresh operation, correct adapter/runtime bindings and
qualification; it does not authorize account changes, quota-reset
consumption, deletion of guards or an unannounced fallback.

Reuse verified adapter files, not used campaign IDs or prior verdicts.
Record changed roots, registries, helpers and settings. Recheck the installed
SDK declarations and actual root model, effort and context capacity.
Omit the model field when configured/default selection is requested;
`model: null` in the receipt is not an observed model.

## Resolve skill discovery

Select the host-specific location and invocation in `compatibility.md`.
Codex's `$xean` and Claude Code's `/xean` do not require Copilot's
`/skills reload` command.

Attempt the requested named skill first. If the resolver reports it missing:

1. Check the exact trusted repository skill path and read its complete
   definition. Do not search unrelated home directories or install a
   replacement when the requested file already exists.
2. Inspect installed CLI help/discovery from the correct repository root.
   For a Copilot host, a fresh command such as
   `copilot -C <repo-root> skill list` can demonstrate discovery independently
   of the active session's cached resolver. Use the actual Codex or Claude
   skill selector/help for those hosts, not this Copilot command.
3. Use interactive reload/info commands only when the installed help
   supports them. Never submit a paid review prompt merely to refresh skills.
4. Follow explicitly requested, readable trusted instructions when permitted,
   while saying that cached named activation did not occur.

A stale cache is not an access denial. Never use another tool to read
content whose access was denied by policy.

## Reconcile before retrying

Treat `retry` as a request to inspect the actual stopping point, not automatic
permission to duplicate an expensive call. Read the known campaign's guard,
bridge receipt, outcome and full report; correlate its UUID and owned process.

| Actual state | Safe next action |
| --- | --- |
| No invocation; preparation incomplete | Finish inputs and qualification, then perform the authorized first launch. |
| Preflight block; no model call | Record zero calls and no verdict. Check only the requested route; do not invent a reset date or silently fall back. |
| Known owned run still active | Retain its IDs and wait for its completion notification. Do not launch a parallel replacement. |
| Interrupted supervisor; remote or child state unknown | Reconcile the same request and owned processes. Keep uncertainty explicit until settled. |
| Completed delivery; assessment or seal pending | Read/reparse the existing result and finish local verification. No new reviewer or provider call. |
| Local decode, console, packaging or assessment command failed | Repair that local command and rerun it against unchanged receipts. Do not replay the provider attempt. |
| Provider/context/decoder failure established | Preserve the failed attempt. Register a fresh diagnosed recovery with exact changed bindings/scope and required qualification. |
| User explicitly requests another independent review | Register a distinct campaign and fresh session. Keep the earlier result, reviewer count and source version separate. |
| Sealed packet | Read and verify only. Any new input, report or addition belongs in a new packet; do not rewrite the seal. |

Kernel completion, a zero wrapper exit, or a file's presence alone is not
sufficient. Check the actual native exit, UUID, host/log hashes, root
completion, loss events and mathematical report. Preserve adverse and
inconclusive outcomes exactly.

## Handle Windows text losslessly

Configure local Python subprocess input/output without changing persistent
global settings:

```powershell
$env:PYTHONUTF8 = '1'
$env:PYTHONDONTWRITEBYTECODE = '1'
# Run the packet's actual local assessment command in this shell.
```

Explicit file decoding is still required:

```python
import hashlib
import json
import sys
from pathlib import Path

sys.stdout.reconfigure(encoding="utf-8")
receipt = json.loads(Path("bridge-response.json").read_text(encoding="utf-8"))
raw = Path("copilot.stdout.jsonl").read_bytes()
if hashlib.sha256(raw).hexdigest() != receipt["stdoutSha256"]:
    raise ValueError("Native stdout receipt mismatch")
text = raw.decode("utf-8")
events = [json.loads(line) for line in text.split("\n") if line.strip()]
```

Write new JSON/Markdown as UTF-8 explicitly. Do not use replacement decoding,
ignore invalid bytes, rewrite native stdout, or repair a quotation to hide a
decoder error. Use `utf-8-sig` only for separately identified BOM-bearing
metadata; hashes always bind the original bytes.

Use literal LF for JSONL, not `str.splitlines()`: U+0085, U+2028 and U+2029
may occur inside valid JSON strings. Parse completed receipts after writers
exit; an incomplete live final line is not a completed event.

## Report completion before sealing

As soon as the completed native outcome and basic receipt identity are
reconciled, give a concise scope/status update:

> Review delivered. Native grade: X; evidence-bound grade: Y. Scope: Z.
> Full assessment/sealing: pending. No manuscript change yet.

Do not claim the mathematical issue is settled before reading the complete
report and source applications. Do not leave a delivered result described as
still running throughout a long local assessment or seal. If an interim
update is unavailable, preserve these exact states in the handoff checkpoint.

Finish the full assessment, database snapshots and live-source checks before
sealing. Observe empty WALs and derived SHM files individually, retain every
nonempty WAL, and seal only after all owned writers have exited. A successful
result waiting for these steps is not a failed review to retry.

## Keep review accounting source-bound

Supply frozen candidate proofs and their required closure, not prior positive
reports or accepted proof-graph conclusions. Treat an independent session as
fresh and unprimed; it need not be a different model and is never human peer
review by implication.

Number canonical scopes and require exactly one coverage/grade row each.
Record qualifications and internal model turns separately; they are not
additional mathematical reviewers. Distinguish protocol qualification,
execution delivery, model verdict, evidence-bound verdict, coordinator
disposition and human acceptance.

Read all source applications and adverse findings even when the model and
evidence-bound grades both say PASS. No scoped grade upgrades excluded
claims, supplies novelty, or replaces analytic proof ownership.
