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

https://github.com/codepath/pathreview-ai301-fa26-s3/issues/60

**Verdict output**

[Your skill's live-mode output for this issue, pasted verbatim and ending with the
fenced JSON verdict block. A summary does not satisfy this field.]

**The verdict must record `accept` for this issue.** Choose an issue your own skill
accepts. If your skill rejects every candidate you try, that is a signal about your
rubric rather than about the issues: revise it and re-run — retries are unlimited and a
partial re-run costs about $0.20 — or run the skill on different candidates. Output
recording `reject` for the issue you chose earns no credit for this field.

```
 {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/60",
    "checks": [
      {"name": "maintainer-alive", "grade": "pass", "evidence": "Last 5 main commits: 2026-09-16 x3, 2026-08-24 x2 (Andrew Burke); newest is 12 days before today 2026-09-28, within 60 days"},
      {"name": "repo-in-use", "grade": "pass", "evidence": "No release published and no tags; commit 2026-09-16 is within 60 days of 2026-09-28"},
      {"name": "unclaimed", "grade": "pass", "evidence": "assignees: none; open PR #80 'Fixes #60' is by classmate pakmultilinks-dot (author_association NONE), set aside under the Path Review house rule on classmate claim signals"},
      {"name": "scope-fits", "grade": "pass", "evidence": "One bug with repro steps and a named failing test test_none_context_chunk_text; no umbrella, no TBD, no closed unmerged PRs"},
      {"name": "ai-policy", "grade": "pass", "evidence": "docs/CONTRIBUTING.md, README and PR template contain no AI-use clause; silence passes"},
      {"name": "responsive-maintainer", "grade": "fail", "evidence": "All 5 comments are author_association NONE; zero maintainer comments repo-wide in the last 100 and zero reviews on 9 open PRs"}
    ],
    "verdict": "accept"
  }
```

---

## Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

**Run history**

[The agreement score of each run you did, in order. A single run is a complete answer if
only one run occurred. **The last score in your list must match the agreement line in the
`eval-run.txt` you committed** — that file is the record of your final run.]

First Run: 12/20
Second Run: 17/20
Third Run: 20/20

**Issue analysis**

[One scored issue, identified by id (`issue-01` through `issue-20`; the `calib-`
issues are not scored). State your rubric's decision, the gold label, and the
reasoning that produced your rubric's result.]

issue-06: the rubric accepted it and the gold label is accept, because the repo-facts line says "latest release: none published" and a default-branch commit is dated 2026-07-14, within 60 days of the 2026-08-05 capture date, so repo-in-use passes on "no release published and a commit within 60 days of that date."


**Check rationale**

[One check from the `rubric.md` uploaded to `tools/issue-select/`, quoted as it is
currently written, with the reasoning behind its current form.]

| ai-policy | The contribution policy line in the repo-facts block | Fail only on an outright ban of AI-generated code or documentation. No policy, or a policy that allows AI if the author reviews the change, passes | required |

This check exists because an outright ban, such as "we do not accept AI-generated code," makes the issue unusable, while silence or a "review it yourself" policy does not. Only the ban fails the check.


**Trade-offs**

[What the quoted check gives up. Any one of these is a complete answer: an issue whose
result it changes, a canary you re-ran with `--only`, a case you accept it will miss, or a
stated reason nothing changed elsewhere. "Nothing changed, and here is how I know" earns
the point in full when the reason follows.]

The check changes issue-12: that issue passes liveness, scope, and claim, and the gold label is reject only because the policy line says "We do not accept AI-generated code or documentation." It gives up softer wording. A line like issue-10's "strongly discourages generative AI" still passes this check.

---

## Selection rationale

Graded on whether all three are answered, in your own words. Not on how good the
reasoning is, and not on length — a short honest answer to each earns the full marks.
This is also the basis for the claim comment you write in Unit 2.

**Selection rationale**

[Answer all three:

1. The issue's fit to your interests and to the time available.
   --> The issue is a python bug in a RAG problem. I want to do ML and have heard of RAG a lot so seems like it will be a fun thing to do. Plus, I like working in python.  
2. What the verdict identified correctly, and what you weighed that the rubric could
   not.
   --> The verdict saw that there waas no AI ban. I weighed the personal interest in AI/ML concepts that the rubric could not.
   
3. The anticipated difficulty in claiming it.]
   --> Medium because I have only worked on smth RAG related once and it was a very small issue. Claiming the issue should not be difficult. 

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
