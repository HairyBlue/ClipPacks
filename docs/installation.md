# Install a Paperclip organization pack

This guide describes the first ClipPacks pack, [Paperclip ACON team](../packs/paperclip-acon-team/README.md). It has not been imported or runtime-tested here.

## 1. Download the pack asset

Open this repository's GitHub **Releases** page and download the release asset named `paperclip-acon-team.zip`. Use the ZIP attached under **Assets**, not GitHub's automatically generated **Source code (zip)** for the ClipPacks monorepository. The named asset is a package whose root contains `.paperclip.yaml`, `COMPANY.md`, 17 `agents/<slug>/AGENTS.md` files, and four support documents.

## 2. Preview a new organization

Use Paperclip's new-organization import flow; do not replace an existing organization. The captured Paperclip UI source describes these controls (UI source guidance only; labels can vary by version and were not exercised in a live instance):

1. Choose **Import source** → **Local zip** → **Choose zip**, then select `paperclip-acon-team.zip`.
2. Set **Target** to **Create new organization**.
3. Choose **Preview import**. Inspect the preview and confirm it contains the organization and all 17 agents. The pack has no projects, tasks, routines, or skills to import.
4. Before applying, ensure **Start imported agents and routines paused** is checked. At the captured source pin, that option sends `pauseAutomations: true`; verify the option in the actual target UI/request rather than assuming the ZIP pauses agents.
5. Apply only after reviewing the preview and confirming it targets a new organization.

The package is authored against captured Paperclip master commit `fd057f6ac4e9148bb4055883ae1d0e7f49242692` and schema 7. The comparison recorded for release `v2026.1012.0` is not a complete compatibility audit. Confirm the installed Paperclip build/importer and consult the pack's [validation record](../packs/paperclip-acon-team/VALIDATION.md); do not infer compatibility from the schema number alone.

## 3. Verify before activating

From authoritative Paperclip records, verify:

- exactly 17 registered agents, with one orchestrator and 16 direct reports;
- each registered identity, organization membership, reporting link, and task ownership;
- imported agent statuses and automation state are actually paused;
- effective permission grants, including defaults such as task-assignment rights, rather than relying on empty manifest declarations;
- the intended `pi_local` adapter, host-side Pi authentication, and `openai-codex/gpt-6-luna`/high-thought configuration are supported in this instance;
- project/repository context, execution workspace, credential scope, and session/reviewer isolation are independently appropriate before assigning work.

The pack declares heartbeat disabled, but that is not a paused status or proof that every wakeup path is disabled. Role prompts, reporting links, and project labels do not enforce permissions or provide ACL/workspace isolation. The package's [README](../packs/paperclip-acon-team/README.md), [roster](../packs/paperclip-acon-team/TEAM.md), and [validation record](../packs/paperclip-acon-team/VALIDATION.md) detail these limits. No company import, live model request, or runtime behavior is claimed by ClipPacks.
