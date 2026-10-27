# Filter notes by one tag

Status: Ready · Priority: Normal · Size: Small

## Current behavior and outcome

Pocket Notes stores tags on notes but its list shows all notes together. Add a
single-tag filter so someone can view only notes tagged "work", for example.

## Acceptance criteria

- [ ] Choosing an existing tag shows only notes with that tag.
- [ ] Clearing the filter restores the full list.
- [ ] A filter with no matching notes shows an empty state and a clear-filter action.
- [ ] Choosing a tag keeps the existing sort order among matching notes.

## Scope and context

Use the existing tag data and list components. This slice does not create tags,
combine tags, change search behavior, or persist the filter across reloads.
The next slice is [URL persistence](04-share-filter.md), which can be reviewed separately.

## Verification

Check matching and nonmatching notes, empty results, clearing the filter, and sort
preservation. Manually use the filter with a keyboard. Run required repository checks.
