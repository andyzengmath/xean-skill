# Client compatibility and execution prerequisites

Use the standard `name`/`description` YAML frontmatter and Markdown body in
`SKILL.md`. Keep Claude-specific dynamic commands, agent configuration and
permission pre-approval out of the shared instruction entry point.

## Contents

- [Install for the controlling host](#install-for-the-controlling-host)
- [Distinguish host and review backend](#distinguish-host-and-review-backend)
- [Qualify execution, not just discovery](#qualify-execution-not-just-discovery)
- [Official references](#official-references)

## Install for the controlling host

Copy or extract the complete `xean` directory, including `references`, into
the selected location. Paths below use Windows separators; use the equivalent
directory hierarchy on the host OS. Do not overwrite an existing skill or
create duplicate same-name installations without inspecting them first.

| Controlling host | Project location | Personal location | Explicit invocation |
| --- | --- | --- | --- |
| GitHub Copilot CLI | `.github\skills\xean` (also supports `.agents\skills` or `.claude\skills`) | `~\.copilot\skills\xean` or `~\.agents\skills\xean` | Ask to use `/xean`; inspect `/skills` or terminal `copilot skill` help |
| Codex CLI | `.agents\skills\xean` | `~\.agents\skills\xean` | Mention `$xean`, or select it from `/skills` |
| Claude Code | `.claude\skills\xean` | `~\.claude\skills\xean` | Invoke `/xean` |

The canonical source directory in the standalone repository is
`.github\skills\xean`; that alone does not make a clone discoverable to
Codex or Claude Code. Install the folder into the relevant location or
request its explicit trusted path using the host's supported mechanism.

For Copilot, use installed `/skills reload` and `/skills info xean` commands
when available, or inspect a fresh `copilot skill list` from the correct
project. For Codex, updates are detected automatically by supported versions;
restart if the skill does not appear. For Claude Code, use the `/` skill
selector and the installed help/discovery behavior. Never transfer one
client's refresh syntax to another or claim activation from a file existing.

No separate Claude/Codex manifest is required for this instruction-only
skill. Optional UI/plugin metadata is not a review runtime. Keep a single
canonical source and preserve all references when distributing it.

## Distinguish host and review backend

The **controlling host** reads these instructions, freezes the candidate,
starts/owns the external review and assesses the result. The **review
backend** is the independent model session invoked through Xean.

Any of the three hosts can coordinate the qualified Copilot-backed workflow
when it has the required local tools, permissions and runtime. A Codex host
can therefore use the `copilot.review` backend without invoking Codex as the
reviewer; Claude Code can do the same. Do not feed the host's prior verdicts
or conversation into that independent session.

| Requested review backend | Required treatment |
| --- | --- |
| Copilot CLI through the supplied qualified example | Inspect public-kernel `copilot.review`, installed SDK/runtime and owned-supervisor bindings; qualify fresh source access and actual context before review. |
| Native Codex through Xean | Locate the actual supported native adapter/entry point and its limits, authenticate/qualify it, and reconcile any old quota/worker failure. Do not rename the Copilot role or reuse a failed guard. |
| Native Claude or another reviewer | Require an explicitly supported adapter and authorization, and qualify it separately. This package does not provide or claim a validated native Claude backend. |
| Current host conversation only | Do not represent it as an independent Xean review. If an external runtime is missing, report that missing prerequisite rather than fabricate a report or silently substitute self-review. |

Installing under `.agents` or `.claude` is host compatibility, not automatic
backend access, a model change or a different-model reviewer guarantee.

## Qualify execution, not just discovery

This repository ships instructions and references, not Xean, Bun/Node,
Copilot/Codex authentication, adapter implementations, a PDF decoder or a
general installer. Check their actual availability without changing global
accounts/settings or enabling unrestricted tools.

For the qualified Copilot example, the controlling host must be able to:

1. Execute the bound public Xean kernel and verified adapter helpers.
2. Own the independent Copilot process, correlate UUID/exit/hash receipts
   and wait for real completion.
3. Retrieve exact primary sources and preserve strict UTF-8 evidence.
4. Enforce read-only reviewer tools and fail on context loss.
5. Keep guarded source versions, scoped verdicts and seals intact.

The historical Windows setup uses a Windows-native supervisor, Linux
Bun/Xean and WSL with executable interop disabled. A POSIX-only system needs
an appropriate separately qualified owned supervisor; do not run the Windows
commands verbatim or change machine settings to imitate them.

Record separately:

- standard-format and package/reference validation;
- actual skill discovery in each installed host;
- end-to-end execution qualification for the selected backend/runtime.

Do not advertise unexecuted host/backend combinations as tested. A successful
Copilot review does not establish native Codex or native Claude execution.
Missing runtime prerequisites remain explicit even though all three clients
support the standard skill format.

## Official references

- [Copilot agent skills](https://docs.github.com/en/copilot/concepts/agents/about-agent-skills)
- [Copilot CLI installation/invocation](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/add-skills)
- [Codex skills](https://developers.openai.com/codex/skills/) (follow any official documentation redirect)
- [Claude Code skills](https://code.claude.com/docs/en/skills)

Check current installed help when a version differs. These references establish
client skill support, not access to a particular review service or theorem.
