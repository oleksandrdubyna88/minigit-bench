# minigit-bench — `template/process-csharp`

The starting point of every **process** run on **C# 14 on .NET 10** in the minigit stack benchmark. Plan:
`dew_flow_benchmark · todo/PLAN_minigit_stack_bench.md`.

PROCESS arm: a Claude Code team lead working under the dew_flow conventions — plan, coai review gates, Sonnet coders, pull requests against a per-run base branch, CI, CodeRabbit, merge.

Each run starts from its own base branch `run/<rid>/main`, cut from a tag of this branch. A run never reads another
run's branches or pull requests, and the harness audits that it did not.

> Status: **skeleton.** This branch holds only the task inputs. The arm's template (instructions, settings, CI, stack
> files) arrives with the plan's epic E2, built once for all four template branches.

## Task inputs — upstream, unchanged

This repository is a GitHub fork of [mame/ai-coding-lang-bench](https://github.com/mame/ai-coding-lang-bench). The four
files below are Yusuke Endoh's, taken byte for byte from its commit `7f6ffdc`. The upstream harness, results and
instructions are removed from this branch, so that nothing but the task reaches a run.

| File | sha256 |
|---|---|
| `SPEC-v1.txt` | `cee6af8fee3f80717809369f090c8e7915a063876d681c5316ae152233145061` |
| `SPEC-v2.txt` | `519064772d1c08c28885d4e4441481c8a741c64059128018f3538996eda8bf81` |
| `test-v1.sh` | `b7ae57d6ecfb30480f0d63a093b17069eead1dd3782ad38b18cf7d3a110f10e6` |
| `test-v2.sh` | `f106bf7cd1686527af5ae87278b650c3eac659a7ce2e889f042a8abf7997824c` |
