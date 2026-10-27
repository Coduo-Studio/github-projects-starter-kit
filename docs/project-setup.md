# Set up the project

Use one GitHub Project for the repositories that share a backlog. These steps
configure your own project; this repository does not provision one for you.
You need permission to create the project and edit its fields and views.

## 1. Create a project

Open **Projects** on your GitHub profile or organization, choose **New project**,
and start with a blank **Table**. Give it your product's name. Keep the project
private if it contains internal planning. An issue's visibility is still governed
by its repository; a private project does not make public issues private.

Add a description explaining the product and who maintains the backlog. Link the
project from the relevant code repository so people can find it.

## 2. Configure the fields

Use the built-in **Assignees** and **Labels** metadata. Configure **Status** and
add two custom single-select fields, **Priority** and **Size**.

### Status

| Value | Move an issue here when |
| --- | --- |
| Backlog | A request exists but its readiness or scheduling is undecided |
| Ready | Outcome, scope, acceptance criteria, dependencies, and verification are clear enough to begin |
| In progress | Someone has taken ownership and started work |
| In review | The implementation and verification evidence are available for review |
| Done | The agreed change is merged or otherwise delivered, and acceptance criteria are verified |

An incomplete form stays in Backlog. A blocked issue stays at its current stage
with a dependency and next action recorded in its body or a comment. When an
unstarted task gains an unresolved dependency, return it from Ready to Backlog.

Configure project workflows deliberately: disable any rule that would overwrite
these status decisions until you have checked it matches your process. In
particular, closing an issue as a duplicate or as not planned is different from
delivering it. Do not treat every closed issue as completed work.

### Priority

| Value | Meaning |
| --- | --- |
| Urgent | Interrupt current work; record why the interruption is justified |
| High | Take before Normal work once it is ready |
| Normal | Default ordering for useful planned work |
| Low | Worth considering after higher-priority work |

### Size

| Value | Meaning |
| --- | --- |
| Small | One bounded change with a clear verification path |
| Medium | Several related changes that can still be reviewed together |
| Large | Too broad or uncertain to start; clarify or split it |

Size measures reviewable scope, not a promise about hours. Leave it unset while
triaging an unclear request. Set new planned work to Normal unless there is a
reason to choose another priority.

## 3. Save three views

Create each view from the project's view menu, choose the layout, apply the
filter, and save the view configuration. Quoted filters handle spaces in status
names. Choose **Priority** as the sort field and put its options in the order
Urgent, High, Normal, Low.

| View | Layout | Filter | Grouping |
| --- | --- | --- | --- |
| Backlog | Table | `is:open status:Backlog,Ready` | Status |
| Active work | Board | `is:open status:Ready,"In progress","In review"` | Status |
| Review queue | Table | `is:open status:"In review"` | None |

Show Title, Assignees, Status, Priority, and Size in the tables. Keep the default
unfiltered view as **All items** so you can still find items with no status and
closed items that the working views hide. If a view is empty, add an open issue
and set its Status before diagnosing the filter.

## 4. Add the first issue

1. Add the issue forms to your code repository's default branch.
2. Open **Issues → New issue** and choose a form.
3. After creating the issue, use its **Projects** sidebar field to add it to this project.
4. Set Status to Backlog and Priority to Normal. Choose a Size when scope is understood.
5. Review it using the readiness checklist in the [agent workflow](agent-workflow.md).

The forms do not set project fields or create labels. They deliberately contain
no organization-specific project IDs, assignees, issue types, or default labels.
Labels are optional: create any you want before adding defaults to the forms.

Automatic issue intake is optional. After manual intake works, consider an
[auto-add workflow](https://docs.github.com/en/issues/planning-and-tracking-with-projects/automating-your-project/adding-items-automatically)
with a filter narrowed to the intended repositories and issues. Check your plan's
workflow availability before relying on it.

## References

- [Creating a project](https://docs.github.com/en/issues/planning-and-tracking-with-projects/creating-projects/creating-a-project)
- [Filtering projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/customizing-views-in-your-project/filtering-projects)
- [Issue form syntax](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms)
- [Creating a repository from a template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)
