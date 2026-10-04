# Xean skill

A GitHub Copilot agent skill for source-bound independent mathematical and
primary-source reviews using Xean's public kernel and a qualified Copilot
adapter.

The skill covers fresh guarded inputs, Windows/WSL process ownership,
retrieval and context qualification, recovery, exact source evidence, report
grading, and evidence sealing. It distinguishes validated report delivery
from mathematical or human approval.

## Use

Clone with an authenticated account that has repository access:

```powershell
gh repo clone andyzengmath/xean-skill
Set-Location .\xean-skill
```

Copilot CLI discovers the project skill in `.github\skills\xean`.
In an already-running CLI session, run:

```text
/skills reload
/skills info xean
```

Then request the `/xean` skill, for example:

```text
Use /xean to prepare a fresh, source-bound review of the changed proof.
```

For another project, copy the `xean` folder into that project's
`.github\skills` directory without overwriting an existing skill.
Alternatively, extract the portable `xean.skill` ZIP and install its `xean`
directory following the
[official Copilot CLI skill instructions](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/add-skills).

## Contents and prerequisites

- [SKILL.md](.github/skills/xean/SKILL.md): reusable review procedure and safeguards.
- [Workflow reference](.github/skills/xean/references/workflow.md): the qualified
  example, provenance, and detailed operational workflow.
- [xean.skill](xean.skill): the portable two-file skill package.

This repository contains instructions and references, not an Xean runtime,
Copilot SDK, qualified adapter implementation, or generic installer.
Inspect available adapter sources and installed declarations, bind the actual
runtime, and qualify it before starting a review. Follow applicable local
mathematical research requirements.

Treat the reference's versions, machine paths, capacities and dated campaign
IDs as historical example data. Do not replay a sealed campaign or change
global settings to imitate it. Preserve failed attempts and require analytic
proof checks; an AI review does not establish authorship, exhaustive novelty
or submission approval.
