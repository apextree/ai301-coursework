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
| --- | --- | --- | --- |
| maintainer-alive | The dates of the last 5 commits on the default branch in the repo-facts block | At least 1 commit was made within the last 60 days | required |
| repo-in-use | The latest release line and, only if it says none published, the last 5 default-branch commit dates in the repo-facts block | A release within 180 days of the capture date, or no release published and a commit within 60 days of that date | required |
| unclaimed | The assignee field and linked pull requests in the repo-facts block | Assignee is none and there are no open linked pull requests | required |
| scope-fits | The issue body, the comment thread, and linked PRs in the repo-facts block | Pass if the body names one bug, one docs task, or one small feature, even when it lists several files, examples, or extra suggestions, and even with no repro steps. "etc." is not undecided. Fail only if it is a tracking list or umbrella of separate issues, an asset or behavior is marked TBD, the thread shows the design is unsettled, or two or more linked PRs are closed and unmerged | required |
| ai-policy | The contribution policy line in the repo-facts block | Fail only on an outright ban of AI-generated code or documentation. No policy, or a policy that allows AI if the author reviews the change, passes | required |
| responsive-maintainer | The issue comment thread and maintainer replies in repo-facts | A maintainer has commented or reviewed an item within the last 30 days | preferred |

## Verdict rule

Accept only if every required check passes. Preferred checks do not affect the verdict and are used only to rank accepted issues. Any check graded as unclear or ? counts as a fail.