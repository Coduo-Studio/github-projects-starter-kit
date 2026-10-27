# Preserve a draft after a failed save

Status: Ready · Priority: High · Size: Small

## Current behavior

In the fictional Pocket Notes app, enter a new note, disconnect the network, and
choose Save. The error appears, but the editor clears and the unsaved text is lost.

## Outcome

A failed save leaves the user's draft available to retry.

## Acceptance criteria

- [ ] A refused save preserves the title and body in the editor.
- [ ] The UI explains that the save failed and offers a retry.
- [ ] Retrying after reconnecting saves one note with the original content.
- [ ] A successful first save still follows the existing completion behavior.

## Scope and context

Change the editor's save and error handling. Offline persistence across a reload
and background retries are separate work. Start with the fictional editor module
`src/notes/editor.tsx` and its existing save tests; locate the equivalents in your app.

## Verification

Exercise successful, refused, and retried saves in the editor tests. Manually
repeat the disconnected-network reproduction. Run the repository's required checks.
