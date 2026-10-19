# Generative UI design plan

A second interactive example of the `html-plan` method by Thariq Shihipar, applied to the existing Generative UI demo - this time as a **design** plan, not an implementation plan.

Four design decisions shape the demo's reply surface. Each decision shows two or three structurally different directions as live mockups: pick an option and the mockup switches in place. Press **Respond** to copy a structured design brief. The page sends nothing; answers stay in the browser's local storage.

## The four decisions

1. **Layout direction** - Feed (editorial column), Workbench (reply + live spec), or Stage (full-bleed view, chat rail).
2. **Provenance marking** - badge, mono spec line, or edge code: how a reply shows whether the catalog or the model made it.
3. **Fallback design** - retry card, graceful degrade, or partial render when generation fails, shown on a state machine.
4. **Steering** - prompt chips, result actions, or edit-the-spec.

## Project grounding

- Source project: https://github.com/Itamar-Dev01/generative-ui-demo/pull/1
- Source branch: `demo/generative-ui-chat`
- Source commit: `bbdb2dd8f011393105749eafce508d3e63dc949a`
- Existing source excerpts include file paths, line numbers and the source commit.
- Code marked `sketch` is a proposal, not existing code.
- The original project was not modified.

## Build

`index.html` is the packed, self-contained output. The editable source is `plan.html`.

```sh
node runtime/pack.mjs plan.html --root ../generative-ui-demo -o index.html
```

The source checkout must use the commit above. Three pack warnings are expected: claims 1, 2 and 4 each hold three mockups on purpose - the page shows one per picked option and switches live. One exhibit per claim is the upstream budget; here the alternatives are the point.

## Credits

Runtime copied from the `html-plan` plugin at https://github.com/anthropics/claude-plugins-community, upstream commit recorded in `UPSTREAM.md`. The repository's Apache-2.0 license is included. Changes: example-specific content, viewport metadata, and mobile spacing/touch-target overrides. No private conversations or credentials appear in the page.

## Live example

https://generative-ui-design-plan.vercel.app/
