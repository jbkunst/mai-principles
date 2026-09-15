# Shiny for R

Reusable guidance for Shiny projects. These notes adapt the general mAI principles to Shiny; they are not a replacement for project-specific instructions or the official Shiny documentation.

## Prefer the framework before working around it

Use Shiny and bslib primitives before hand-rolling equivalent behavior.

- Use Shiny's reactive model instead of manually coordinating updates.
- Use bslib layout and navigation components before building custom HTML structures for the same purpose.
- Use companion packages such as DT, reactable, leaflet, plotly, shinychat, reactlog, or shinytest2 when they already solve the problem well.
- Introduce custom JavaScript, bespoke components, or framework workarounds only when the native or established approach does not meet the actual requirement.

The goal is not to avoid customization. It is to understand and exhaust the intended path before creating another one.

## Keep a clear hierarchy

Start from the user task or decision the app supports, not from the available widgets or data columns.

A useful default hierarchy for analytical apps is:

1. the main task, decision, or question;
2. a small set of headline information or controls;
3. one or two views that explain or support the main result;
4. detailed tables or secondary information for drill-down;
5. advanced or infrequently used controls behind progressive disclosure.

Avoid turning every variable into a filter, every metric into a card, or every possible view into a tab. Prefer one coherent workflow over a collection of disconnected widgets.

Centralize shared logic when several outputs depend on the same concept, such as a common filtered dataset. This keeps different parts of the app from silently disagreeing about the current state.

## Modularize when there is something to modularize

Do not create modules only to make the code look architected.

Use a Shiny module when a UI/server responsibility is genuinely reusable, repeated, independently understandable, or needs its own namespace. Keep one-off behavior local when extracting it would only add indirection.

When a module is justified, use Shiny's namespacing and module interfaces instead of manually constructing ids or reaching into internal inputs from the parent.

## Validate with the smallest test that proves the change

Follow the README's lightweight-script default: run the complete script after relevant code changes while it remains fast and self-contained. Add session, browser, or broader checks only when relevant behavior is not covered.

Use this escalation path:

1. **Local checks** for syntax, pure functions, transformations, and other logic that does not need a Shiny session.
2. **`testServer()`** for reactive/server/module behavior that can be proven without rendering a browser.
3. **Manual browser checks** when the change concerns rendered layout, CSS, JavaScript, widgets, responsive behavior, or interactions that only exist in the browser.
4. **`shinytest2` or broader end-to-end tests** when those browser behaviors need repeatable automated coverage.
5. **Full builds or wider validation** only when the change can affect the application or deployment beyond the touched area.

Choose the narrowest level that can fail if the change is wrong. Broader validation should add evidence, not merely ceremony.

## Sources

This guidance was distilled from Posit's Shiny for R agent skill and its references, especially the sections on dashboard design, modules, testing, and ecosystem choices:

- <https://github.com/rstudio/shiny/blob/main/inst/skills/shiny-for-r/SKILL.md>
- <https://github.com/rstudio/shiny/blob/main/inst/skills/shiny-for-r/references/dashboard-design.md>
- <https://github.com/rstudio/shiny/blob/main/inst/skills/shiny-for-r/references/modules.md>
- <https://github.com/rstudio/shiny/blob/main/inst/skills/shiny-for-r/references/testing.md>
- <https://github.com/rstudio/shiny/blob/main/inst/skills/shiny-for-r/references/ecosystem.md>
