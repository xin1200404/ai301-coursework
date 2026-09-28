# Rubric: is this reproduction package ready to post?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever
checks you define here. It ships empty on purpose: the judgment is your
work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four
   columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where in the package. Name
     the part (the claim comment, the repro report's environment
     record, the artifacts read against the issue's description, the
     repo-facts block) or a location from your
     references/evidence-guide.md. "The report" is not a source; "the
     output excerpt read against the error the issue describes" is.
   - Pass condition: a decision rule about the OUTCOME that someone
     else could apply and get your answer. Judge the thing itself (does
     the artifact show the issue's behavior?), never the write-up's
     shape (how many steps it has, how long it is, whether it uses a
     template's headings). Structure-shaped checks are what make
     graders disagree with themselves.
   - Weight: `required` (a fail here holds the package) or `preferred`
     (never changes the verdict).

2. A verdict rule below the table: how the check grades combine into
   accept (ready) or reject (hold), including how `unclear` is
   treated. The verdict space is binary. If you write no rule for
   `unclear`, the skill treats it as fail.

Cover what actually gets bad packages posted. The lecture named the
proof families: the environment is recorded, the steps are complete
and followable, the behavior shown matches the issue (not an adjacent
one), the outcome is stated honestly (an evidenced cannot-reproduce is
a pass, a confident wrong-target is not), and the words respect the
repo's conventions. A rubric that ignores a family will fail eval
packages designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| environment recorded | The evironment line | The environment line states a specific tool version, OS with version and install method. The version tested matches the issue's version, or the report explicity states a different version and gives a reason | required |
| steps followable | The comments run and input shown in the report, read against What the repo's README or COUNTRIBUTING says is the standard setup | The commands run are shown verbatim. The input's content is either shown directly as a code block, or described with enough specificity that a stranger could reconstruct it precisely. | required |
| behavior matches | The candidate's input/command diffed character-by-character against the issue's input/command; the candidate's actual output/error diffed against the issue's reported failure. | The input or command is identical to the issue's, and The failure matches the issue's in kind, or the report explicitly identifies and justifies a cosmetic difference that doesn't change the underlying failure. A syntax error standing in for a reported panic is a fail even if the report calls it the same bug. | required |
| honest outcome | Compare the report's stated conclution with what the artifact in behavior-matches actually shows | The stated outcome matches what the evidenced supports. A confident claim of reproduction that behavior matches contradicts is a fail confidence is not a substitute for the artifact atching. | required |
| specific wording | The candidate's claiming commenr, read against the issue's behavior and the repo's stated contribution conventions | Names and the specific version and specific behavior from the issue.Promisses a concrete next artifact, not a vague timeline. Does not assert understanding or conclusions the evidence doesn't independently establish. | prefered |

## Verdict rule
Accept only if every required check passes. Unclear on a required check is treated as fail, since an unreadable proof is not proof. preferred checks are supporting pass.

<!-- State how the grades above combine into accept or reject, and how
unclear is treated. Example shape (write your own): "accept if every
required check passes; preferred checks never change the verdict;
unclear counts as fail." -->