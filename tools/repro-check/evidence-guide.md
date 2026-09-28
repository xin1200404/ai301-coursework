# Evidence guide: where proof lives in a reproduction package

<!--
THIS IS THE PART YOU WRITE (new this week: Unit 1 handed you this file
finished; the scaffolding fades). The skill uses this guide as its map:
for every kind of proof a rubric check names, this file says WHERE to
find it in a package and WHAT GOOD LOOKS LIKE when you do.

Under each family heading below, write:

- Where it lives: the exact places to look. In an eval bundle (which
  section of the package: the issue context, the repo-facts block, the
  claim comment, the repro report and its parts). In live mode (where
  on GitHub or in the draft: the issue thread, the repo's docs, the
  student's draft comment).
- What good looks like: one or two sentences someone else could apply.
  Prefer observable conditions ("the versions named match what the
  issue targets, or the difference is called out") over adjectives
  ("environment is thorough").

A rubric check whose evidence this guide cannot locate is a check
nobody else can execute; the rubric swap showed you what that feels
like. Write the map you wish your grader had.
-->

## Environment

Where it lives: The "Environment:" line at the top of the candidate's repro report, read against the repo-facts block's latest release field and against the issue's own stated version/OS. In live mode, this is the equivalent line in draft comment, checked against the version noted in the GitHub issue.

What good looks like: The version, OS, and install method are named explicitly and specifically. The tested version either matches what the issue names, or the report says outright that it's testing a different version and why. A vague or missing environment line fails this check.

<!-- Where the environment record lives, and what a sufficient one
looks like against the issue's stated target. -->

## Steps

Where it lives: The "Preparation" or "Execution" part of the repro report. The exact commands run and the exact input file contents, shown as code blocks. In live mode, this is whatever setup and command sequence you're about to post, checked against the repo's own README or CONTRIBUTING for the "how to build" instructions.

What good looks like: Commands and input are shown verbatim, not summarized. A stranger with no other context could copy-paste them, starting from a fresh clone or a stated starting state, and land in the same place you did before running the command that triggers the bug.

<!-- Where the reproduction steps live, and what makes them followable
by a stranger, starting state to trigger. -->

## Behavior shown

Where it lives: The terminal output, logging, or screenshot pasted into the report's "Actual" section, compared directly against the issue's own pasted error message. In live mode, this is the artifact you're about to attach, checked against the issue body's original output.

What good looks like: The artifact shows the same kind of failure as the issue. Before trusting a match, diff the input/command that produced the artifact against the issue's input/command. If they differ even slightly, the resulting failure is probably a different bug wearing the same "it errored" clothing. An artifact that shows the wrong failure fails this check even if the report calls it correct.

<!-- Where the artifacts live (output excerpts, logs, screenshots),
and what it means for an artifact to show the issue's behavior rather
than an adjacent one. -->

## Honesty

Where it lives: The stated conclusion "Expected" or "Actual," or an equivalent verdict sentence. In live mode, this is the tone of your draft's closing line versus what your own attached log shows.

What good looks like: The stated outcome doesn't outrun the evidence. A clean environment record, followable steps, and a log showing no failure is a pass. If the attached artifact shows a different error class than the issue, no matter how confident the wording. Confidence is not evidence. Only the artifact is.

<!-- Where claims and their backing meet: how to tell a report that
says exactly what happened (including an honest cannot-reproduce) from
one that claims more than its evidence shows. -->

## Comms

Where it lives: The candidate's claiming comment, read against the issue's specific version/behavior and against the repo's CONTRIBUTING.md / AGENTS.md for any stated conventions. In live mode, this is your own draft comment before it posts, checked the same way.

What good looks like: The comment names the specific version and specific behavior from the issue that could sit under any issue is boilerplate, not comms. It promises a concrete next artifact rather than a timeline. It doesn't assert understanding or a root cause that the report's own evidence hasn't independently shown. If the repo's contribution policy requires AI-use disclosure, the comment states it plainly rather than omitting it.

<!-- Where the words meet the repo: the claim comment against the
issue, the comments against the repo's stated templates and
contribution policy (including AI-use disclosure requirements), and
what specific-and-honest looks like next to boilerplate. -->
