# Agent instructions

## Caveman workflow

Use the applicable Caveman workflow for coding, debugging and code review. Investigate before editing, prepare a compact execution plan, make the smallest coherent change, review the diff and run relevant validation. Reuse unchanged passing evidence; avoid unrelated cleanup and repeated broad tests. Preserve required checks, safeguards and approval rules. If Caveman is unavailable, state this and follow the same principles without claiming it was used.

## Issue-to-merge workflow

Every bug fix must have a GitHub issue. Search existing issues and PRs first; reuse the matching ticket and avoid duplicate work.

Assign one implementation owner per issue. Work on a scoped branch and open one PR targeting the repository's approved integration branch (normally main; retain master where it is the existing default). Include "Closes #<issue>" for completed fixes, the problem, fix and validation evidence. Related fixes may share a PR when their scope is explicit.

Preserve collaborators' changes. Resolve conflicts on the working branch. Merge only after required CI and applicable independent review pass; never bypass protections or push directly to the protected integration branch.

When delivery is authorised, normal pushes, PR updates and normal merge are included. Do not repeatedly request intermediate approval. This rule does not itself grant delivery permission; specific owner restrictions take precedence.

Verify the resulting integration-branch commit and linked issue closure. Track merged, DEV-tested and production-released states separately. Deployment requires its own authorisation.
