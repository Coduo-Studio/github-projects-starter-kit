# Export notes as Markdown

Status: In progress · Priority: Normal · Size: Medium

## Outcome and current behavior

Pocket Notes has no export. Let someone download a ZIP containing one Markdown
file per note, with the full note text preserved.

## Agreed acceptance criteria

- [ ] Every selected note appears once in the ZIP.
- [ ] Unicode titles and bodies survive export.
- [ ] Empty selection explains that there are no notes to export.
- [ ] Duplicate titles produce distinct filenames and do not overwrite notes.

## Scope

Export selected text notes. Import, attachments, and scheduled exports are separate work.

## Progress and blocker

Archive assembly is drafted. Filename generation is paused: using the title alone
collides when two notes have the same title.

**Decision needed:** choose a filename convention. Proposed: a sanitized title plus
a stable note identifier. The maintainer must confirm this convention before that
part proceeds. Implementation owner: the developer who took this issue. Decision
owner: the product maintainer. Next action: record the convention here, then resume
filename handling. Status remains In progress while the blocker is explicit.

## Verification still required

Exercise duplicate and empty titles, unsafe filename characters, Unicode content,
and an empty selection. Open the resulting ZIP and inspect its files. Required
repository checks have not run; this task is not complete.
