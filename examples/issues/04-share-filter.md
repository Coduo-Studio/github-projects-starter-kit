# Preserve a tag filter in the URL

Status: Backlog · Priority: Normal · Size: Small

## Current behavior and outcome

Once the [single-tag filter](03-tag-filter.md) is delivered, its selection will be
local to the current page. Preserve it in the URL so a reload or shared link can
restore that view for someone who already has access to the same notes.

## Acceptance criteria

- [ ] Selecting a tag writes its identifier into the URL query.
- [ ] Reloading restores the selected tag.
- [ ] Clearing the filter removes that query parameter.
- [ ] Browser Back and Forward restore the corresponding filter state.
- [ ] An unknown tag identifier shows all notes and an explanation that the filter is unavailable.

## Scope and dependencies

Depends on [the single-tag filter](03-tag-filter.md). No sharing permissions, public
note links, or access changes. Moving a tag identifier into a URL does not make a
private note accessible. Move to Ready after the dependency lands and the maintainer
confirms the route integration point.

## Verification

Check reload, encoded tag identifiers, clearing, unknown tags, and browser history
navigation. Run required repository checks.
