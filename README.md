# Xean skill

An Agent Skills instruction package for source-bound independent mathematical
and primary-source reviews, usable from **GitHub Copilot CLI, Codex CLI, and
Claude Code** as the controlling host.

The skill covers fresh guarded inputs, host/backend selection,
Windows/WSL process ownership in the qualified example,
retrieval and context qualification, recovery, exact source evidence, report
grading, and evidence sealing. It distinguishes validated report delivery
from mathematical or human approval.

**Client compatibility is not backend qualification.** The recorded working
review integration uses Xean's public kernel and a Copilot adapter. A Codex or
Claude Code host can coordinate that integration when its tools, permissions,
and external runtime are available. This package does not supply or claim a
qualified native Claude reviewer.

## Install and invoke

Clone or download the repository. Authenticate if repository access requires it:

```powershell
git clone https://github.com/andyzengmath/xean-skill.git
Set-Location .\xean-skill
```

The canonical skill source is `.github\skills\xean`. Copilot can discover it
directly when working in this clone. To use the skill in another project,
copy the complete `xean` folder into the location for that host:

| Host | Project directory | Personal directory | Invocation |
| --- | --- | --- | --- |
| Copilot CLI | `.github\skills\xean` | `~\.copilot\skills\xean` | `/xean` |
| Codex CLI | `.agents\skills\xean` | `~\.agents\skills\xean` | `$xean` or `/skills` selector |
| Claude Code | `.claude\skills\xean` | `~\.claude\skills\xean` | `/xean` |

Inspect any existing installation first; do not overwrite or duplicate it
silently. Preserve the `references` directory. On other operating systems,
use the equivalent directory hierarchy.

For a **Copilot** session whose installed help supports them, run:

```text
/skills reload
/skills info xean
```

Then request the skill, for example in Copilot or Claude Code:

```text
Use /xean to prepare a fresh, source-bound review of the changed proof.
```

For Codex, use:

```text
Use $xean to prepare a fresh, source-bound review of the changed proof.
```

Codex normally detects skill updates automatically; restart if it does not
appear. In Claude Code, inspect the `/` skill selector and installed help.
Do not use Copilot's reload command in another host.

Alternatively, extract the `xean.skill` ZIP and install its `xean` directory
at the relevant location above. The same standard `name`/`description`
frontmatter and instruction package are used by all three; no client-specific
plugin or permission pre-approval is required.

## Contents and prerequisites

- [SKILL.md](.github/skills/xean/SKILL.md): reusable review procedure and safeguards.
- [Client compatibility](.github/skills/xean/references/compatibility.md):
  installation, invocation, controlling-host and review-backend distinctions.
- [Operations](.github/skills/xean/references/operations.md):
  backend changes, guarded retries, UTF-8/LF parsing and completion handoff.
- [Workflow reference](.github/skills/xean/references/workflow.md): the qualified
  example, provenance, and detailed operational workflow.
- [xean.skill](xean.skill): the portable four-file skill package.

This repository contains instructions and references, not an Xean runtime,
Copilot SDK, qualified adapter implementation, or generic installer.
Inspect available adapter sources and installed declarations, bind the actual
runtime, and qualify it before starting a review. Follow applicable local
mathematical research requirements.

For native Codex or another review backend, locate its actual supported
adapter and qualify it separately. The host name, discovery of this skill,
or a successful Copilot review is not proof that another backend works.
Missing local tools/authentication/runtime must be reported explicitly; do
not substitute the current host conversation for an independent review.

Treat the reference's versions, machine paths, capacities and dated campaign
IDs as historical example data. Do not replay a sealed campaign or change
global settings to imitate it. Preserve failed attempts and require analytic
proof checks; an AI review does not establish authorship, exhaustive novelty
or submission approval.

See the compatibility reference for official client documentation and the
distinction between package validation, host discovery, and actual execution
qualification.
