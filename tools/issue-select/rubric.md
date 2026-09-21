# Rubric: is this a good first issue?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever checks
you define here. It ships empty on purpose: the judgment is your work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where. Name the source
     (repo-facts block, issue body, comment thread, or the locations in
     references/evidence-guide.md). "The repo" is not a source; "the last
     5 default-branch commit dates" is.
   - Pass condition: a condition someone else could apply and get your
     answer. Prefer thresholds with numbers ("a maintainer commented
     within 30 days") over adjectives ("maintainer is responsive").
   - Weight: `required` (a fail here rejects the issue) or `preferred`
     (never changes the verdict; a nice-to-have that helps rank the
     issues you accept).

2. A verdict rule below the table: how the check grades combine into
   accept or reject, including how `unclear` is treated. The verdict
   space is binary. If you write no rule for `unclear`, the skill treats
   it as fail.

Cover what actually kills first contributions. The lecture named four
families: the maintainer is alive, the repo is in use, the scope fits a
newcomer, and nobody else is already on it. A rubric that ignores a family
will fail eval issues designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| Maintainer active | Repo-facts block: date of last commit on default branch | Last commit was within 60 days of today | required |
| Repo in use | Repo-facts block: stars, open issues count, recent issue/PR creation dates | At least 1 issues or PRs opened in the last 60 days | prefered |
| Scope fits | Issue body: description length, number of files/areas implied, presence of acceptance criteria | Fails if the issue leaves the correct end state genuinely open, or is too vague to identify any starting point. A task that is large or touches several files/areas still passes if it comes with a concrete, fully-specified plan. A short list of concrete, similar, small items within one feature/area is not open-ended under this clause, and it still passes. An issue labeled "good first issue", "help wanted", or equivalent is supporting evidence toward passing. Otherwise pass.| required |
| Unclaimed | Comment thread and issue metadata: assignee field, comments claiming the issue, linked opened PRs referencing this issue | An assignee is not currently set, no comment that claims the issue within roughly the last 6 months, and no open PR that claims to solve this issue | required |

## Verdict rule
Accept the issue if every required check passes. 
The preferred checks never change the accept/reject verdict.
The preferred checks are used to rank issues that already passed all required checks, with issues passing more preferred checks ranked higher.

<!-- State how the grades above combine into accept or reject, and how
unclear is treated. Example shape (write your own): "accept if every
required check passes; preferred checks never change the verdict, they
rank accepted issues; unclear counts as fail." -->
