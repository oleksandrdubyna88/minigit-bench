# minigit-bench -- the `inputs` branch

This branch holds the task inputs of a benchmark that has two agent arms build the same small program ("minigit")
from the same specification. It is a fork of `banteg/minigit-bench`, itself a fork of
`mame/ai-coding-lang-bench`; this branch was cut from `mame/ai-coding-lang-bench@7f6ffdc`. The upstream harness, results,
figures and `CLAUDE.md` are removed here: they are not inputs.

| Path | What it is |
|---|---|
| `SPEC-v1.txt`, `SPEC-v2.txt` | the two specifications, byte for byte as upstream |
| `test-v1.sh`, `test-v2.sh` | the visible tests the agents run: upstream with three small edits, listed in each file's header (loud build failure, a crash counts as failures, the parent of a commit is checked) |
| `upstream/` | the four upstream files above, unchanged, as the reference the edits are measured against |

The benchmark harness lives elsewhere and fetches this branch at a pinned commit, then verifies every file against a list
of sha256 hashes. Nothing here is ever edited in place: a change is a new commit and a new pin.
