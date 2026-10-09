# Verification — 9 October 2026

## Reviewed volunteer Code of Conduct refresh

The volunteer form is refreshed from canonical commit `ef5e4c7921e72995213fa21d19f020f60c90cd72`. It contains the approved October 2026 policy, eight source links and v4 acknowledgement. Draft/proposed labels, paper-signature fields and the implementation note are excluded. The engine, configuration, styles and other twelve blocks retain their preceding bytes. The ZIP includes the replacement volunteer block.

All 13 packaging parity checks pass. The canonical and inline volunteer reader pass exact text/link checks at 1280px and 375px, including disabled/unchecked initial state, partial-scroll blocking, end-of-document unlock, explicit acknowledgement, October version, reset and no horizontal overflow. No runtime error or external POST occurred. The existing form-engine suite passes 152 checks/21,196 combinations. The new volunteer block is 126,886 bytes. These focused checks supplement the dated initial two-reviewer report below; that full independent review was not repeated for this text replacement. Installed client blocks must be replaced to receive the update.

**Pass for the recorded source and local browser comparisons. Actual client Squarespace installation remains to be checked.** No Salesforce submission, email, payment or SharePoint upload was made.

Baseline: canonical public NTE forms commit `48f850b85ae7643be6657e0045e1c15391e7e944`. The copied HTML, engine, configuration, styles and PNGs match that baseline. Every delivered block embeds the unchanged engine and configuration; the preview includes the exact delivered block.

## Two independent reviews

| Check | Implementing agent | Independent reviewer |
| --- | --- | --- |
| All ten forms, desktop | 1280px, zero differing pixels | 1440px, zero differing pixels |
| All ten forms, mobile viewport | 375px, zero differing pixels | 390px, zero differing pixels |
| Captured native POSTs | 20, matching ten source/inline pairs | 42, matching 21 source/inline pairs |
| Choice/option state comparisons | 341 sequential state comparisons | Targeted journeys, every package/space and additional branches |
| Host theme isolation | 23px root, conflicting important styles, all-element appearance/geometry comparison | 22px root, hostile type/controls/box sizing |
| Supporting pages | All three, two widths, zero differing pixels | All three, matching internal content/geometry |
| Multiple blocks and lifecycle | Static scoping review | Three blocks including duplicate IDs, detach/reconnect, no duplicate handlers |

These are intercepted requests, not live Salesforce receipts. The root tests freeze time/randomness; the reviewer normalizes only newly generated booking references. Both compare the existing volunteer return against its public canonical address when testing local copies.

Both reviews exercised validation and conditional content. The reviewer additionally checked transport exceptions, pageshow recovery, volunteer conduct gating, checkbox exclusivity, pricing, roster/top-up rules and reference normalization. Neither observed a runtime error in the final build. The existing unchanged form-engine suite also passed **152 checks and 21,196 catalogue/boundary combinations**.

Two issues identified independently during review were repaired before delivery: original html/body separation is preserved so volunteer inherited text colours match, and the NTE thank-you page retains its original non-Inter fallback. The implementing agent visually inspected paired renders for each form and reconciled the reviewer’s findings. Both final reviews agree: no remaining form-function or form-content appearance difference was found in the tested scope.

Supporting pages shorter than a viewport leave space belonging to the host website. The reviewer used a white surrounding host and recorded a fractional boundary row on two cropped supporting-page screenshots; internal content still matched. The supplied standalone previews reproduce the canonical mist background and pass complete pixel comparisons.

## Deliberate packaging differences

Nine demo-only email-preview panels are omitted. All applicant copy, fields and behaviour are retained. Relative links become their existing absolute URLs, and the volunteer thank-you binding explicitly preserves its existing destination. The forms appear inside the Squarespace page, whose outer header, footer and allocated width remain under that site's control.

The largest block is **117,401 bytes**, below the documented 400 KB limit. HTML, styles, configuration and JavaScript are in every text file; logo and font binaries continue to use their existing public hosts.

## Limits

Chrome desktop and mobile-sized viewports were used, not a physical device or assistive-technology matrix. Deterministic visual comparisons fulfilled PNG requests from the identical canonical reference bytes. Public asset and release URLs are checked separately during publication. No code was pasted or saved into the client's Squarespace account, so its plan, code-block execution, section sizing and published navigation are not qualified by this report. No new Salesforce/server-side acceptance or real SharePoint transfer is claimed.

[Squarespace Code blocks](https://support.squarespace.com/hc/en-us/articles/206543167-Code-blocks) documents the JavaScript-capable plans, HTML mode, Display Source setting, size limit and editor caveat. [Squarespace Ajax loading](https://support.squarespace.com/hc/en-us/articles/115000253288-Ajax-loading-in-version-7-0) explains the remaining version 7.0 navigation caveat. Both were checked on 9 October 2026.

Production configuration and installed-page acceptance belong to the later production handover described in [maintenance](MAINTENANCE.md).
