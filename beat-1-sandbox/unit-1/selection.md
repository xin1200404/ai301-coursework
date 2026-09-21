# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

**Issue link**

[The individual Path Review issue page. A link to the repository or the issue list
does not satisfy this field.]

**Verdict output**

[Your skill's live-mode output for this issue, pasted verbatim and ending with the
fenced JSON verdict block. A summary does not satisfy this field.]

**The verdict must record `accept` for this issue.** Choose an issue your own skill
accepts. If your skill rejects every candidate you try, that is a signal about your
rubric rather than about the issues: revise it and re-run — retries are unlimited and a
partial re-run costs about $0.20 — or run the skill on different candidates. Output
recording `reject` for the issue you chose earns no credit for this field.

```
3. #69 — Output parser crashes on top-level JSON array — accept
- Maintainer active ✅ · Repo in use ✅ (preferred) · Scope fits ✅ · Unclaimed ✅
- Scope: names the exception, both files, the xfail marker to remove (manifest H-02), and a 2–4h estimate. Fully specified, just the largest of the three.
- Unclaimed: no assignee, no PRs. One claim comment — Yina-Mu, author_association: NONE, 2026-09-20 — classmate, ignored under the house rule.
```
On the ranking. Your fit profile in scope.md reads "I prefer C++. And I want to practice using Claude Code." — that names no languages, goals, or things to avoid, so it can't order anything. Your one preferred check ("Repo in use") is repo-level and identical across all three, so it can't break the tie either. The order above is therefore my inference, not your rubric's: ascending surface area for a newcomer (fixture data edit → one-field swap → new fallback branch plus test change). #64 also happens to be the only one with zero classmate claims. Write a real fit profile and the ranking becomes yours instead of mine.

Two setup nits, unrelated to the grades. Your skill lives at ~/.claude/skills/issue_select/skill/SKILL.md; Claude Code looks for ~/.claude/skills/<name>/SKILL.md, so the extra nesting (and the underscore) means /issue-select isn't registered — I read the files directly this run. And the Weight cell on "Repo in use" reads prefered; I treated it as preferred.
---
[
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/69",
    "checks": [
      {"name": "Maintainer active", "grade": "pass", "evidence": "Last main commit 2026-09-16 by Aburke225 (COLLABORATOR), 4 days before today"},
      {"name": "Repo in use", "grade": "pass", "evidence": "Issue #73 opened 2026-09-16, within the last 60 days"},
      {"name": "Scope fits", "grade": "pass", "evidence": "Names the AttributeError, both files, the xfail marker H-02 to remove, and a 2-4 hour estimate; labeled good first issue"},
      {"name": "Unclaimed", "grade": "pass", "evidence": "No assignee and no linked PRs; sole claim comment is from Yina-Mu (author_association NONE), which the Path Review house rule says does not block"}
    ],
    "verdict": "accept"
  }
]

## Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

**Run history**

[The agreement score of each run you did, in order. A single run is a complete answer if
only one run occurred. **The last score in your list must match the agreement line in the
`eval-run.txt` you committed** — that file is the record of your final run.]

**Issue analysis**

[One scored issue, identified by id (`issue-01` through `issue-20`; the `calib-`
issues are not scored). State your rubric's decision, the gold label, and the
reasoning that produced your rubric's result.]

**Check rationale**

[One check from the `rubric.md` uploaded to `tools/issue-select/`, quoted as it is
currently written, with the reasoning behind its current form.]

**Trade-offs**

[What the quoted check gives up. Any one of these is a complete answer: an issue whose
result it changes, a canary you re-ran with `--only`, a case you accept it will miss, or a
stated reason nothing changed elsewhere. "Nothing changed, and here is how I know" earns
the point in full when the reason follows.]

---

## Selection rationale

Graded on whether all three are answered, in your own words. Not on how good the
reasoning is, and not on length — a short honest answer to each earns the full marks.
This is also the basis for the claim comment you write in Unit 2.

**Selection rationale**

[Answer all three:

1. The issue's fit to your interests and to the time available.
2. What the verdict identified correctly, and what you weighed that the rubric could
   not.
3. The anticipated difficulty in claiming it.]

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
