# Supplier maintenance notes

## Packaging boundary

The canonical source is frozen at the commit in `source-manifest.json`. The source form engine and Salesforce configuration are embedded byte-for-byte. The wrapper binds document lookups to each form's open shadow root and gives it a separate configuration object. Native element creation, cryptographic randomness, browser events and the final native Web-to-Lead POST retain their browser implementations.

Each block includes all CSS and JavaScript. The existing GitHub PNGs and Google font binaries remain external assets. Font-face CSS is included in the block and inserted once into the document under a dedicated family name. It is not an external CSS dependency.

Separate inner root and body elements preserve the original cascade, including volunteer colour inheritance. The original 16px-based rem dimensions are converted to equivalent pixels so a site's root font size cannot change the form design. Browser zoom continues to work. Media queries and viewport units retain the original responsive behaviour.

Custom elements initialise once, isolate duplicate IDs, and clean up/reconnect their global event listeners as Squarespace inserts or removes blocks. Their runtime tag includes a content hash, allowing updated runtime versions to coexist. Arbitrary HTML insertion that never executes a new block's script cannot be solved by code inside that unexecuted block; Squarespace 7.0 Ajax navigation must be checked in the actual installation.

The host site's header, footer, available width, section spacing and background outside the block remain part of that website. Match the supplied width and section spacing when comparing appearance. Squarespace's visual editor cannot edit the custom form's individual fields. Update the source and replace the entire block.

## Documented differences from the demo website

- Remove only `.email-preview-panel` sections; they are review links, not part of applicant submission.
- Replace relative image and page links with their existing absolute public URLs.
- Bind the volunteer return to the existing volunteer thank-you URL. Leaving its source `data-return-path` relative would point it at a nonexistent Squarespace page; its exact existing destination is preserved.
- Keep content inside the block and leave the surrounding Squarespace website intact.
- Provide an actionable loading failure message if the block's script does not run. Successful forms do not display it.

No iframe, backend, Salesforce package change, new form field, new payment behaviour or live test submission is included.

## Refresh from approved source

Copy only the 13 selected public HTML pages, the four shared CSS/JavaScript files and the two PNG reference copies from a reviewed current canonical checkout into `source/`. Record that commit and recompute the source SHA-256 manifest. Keep the captured Google font CSS current only when the original typography changes. Never copy a Salesforce package checkout or private project audit into this repository.

Run the build, parity checks and relevant browser checks, update the ZIP and verification record, then publish the changed website files. Each installed Squarespace block is a snapshot: a GitHub update does not silently update code already pasted into a client page.

## Production handover — later authorised release

Do not change only the `mode` string. Prepare and verify the complete target configuration after the Salesforce production deployment:

1. Production Web-to-Lead endpoint, organisation ID and every custom field ID used by the forms. Field IDs are environment-specific.
2. Confirm the terms/privacy and real SharePoint upload destinations with the client.
3. Confirm the final Squarespace page slugs, both thank-you URLs and staff chooser links. Put link overrides in `hosting.json.pageUrls`, keyed by original filenames, and per-page thank-you overrides in `hosting.json.returnUrls`, keyed by form slug. All return URLs must be absolute HTTPS URLs.
4. Intentionally replace `source/assets/config.js` with the verified target configuration and update its manifest hash and the target-specific assertions in `tests/parity.mjs`. Record the approved environment in the manifests, README, installation guide and download-page environment label. Rebuild every block and the ZIP.
5. Update Salesforce email/application/preparation links to the approved final Squarespace addresses as part of the production release.
6. Install on the actual Squarespace site and check published desktop/mobile layout, keyboard validation, expanding sections, direct and internal navigation, and a deliberately authorised fresh submission through Salesforce and its return page. Existing successful test records and sends must not be replayed.

No production endpoint, organisation ID, page URL or approval is inferred by this packaging release.
