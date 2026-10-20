# Validation reflection

**Validator:** tcartier  **Project owner:** jdodd8 (theoretical teammate)

Because jdodd8 is a theoretical teammate, there was no live discussion. I settled every disagreement by substituting my own result, so the post-discussion numbers (100% agreement, kappa 1.0) come from that rule and are not evidence of anything. The pre-discussion numbers are the real comparison: 80%, 60%, 50%, 20% and 30% agreement for HasRecovered, WhyRecovered, ActivityPattern, Currentstatus and RecentThemes.

## Signals before long gaps

In these ten projects, the long gaps tended to follow low-volume, housekeeping-style work by one or a few people. fragit's 41-month gap (2020-05 to 2023-09) came after Travis and CI updates and one small pull request, with only 3 authors before it. revitpythonshell's 13-month gap followed installer, README and credits changes in late 2018. roboticslibrary_rl had only 3 authors before its 29-month gap, and grassmann.jl's pre-gap history was just an empty initial commit, generated files and a license. The short gaps were different: msnoise (5 months) and rlbench (4 months) paused after busy periods with many authors (39 and 17), which looks like a normal break.

## What triggers recovery

Recovery usually came with a specific job to do. Platform and dependency changes were common: a scipy compatibility fix in msnoise, a Boost 1.66 update in rl, OpenBabel installation and GitHub Actions in fragit, and a move to SDK-style project files in revitpythonshell. Recoveries were driven either by the same person returning (Michael Reed in grassmann.jl, Casper Steinmann in fragit, Thomas Lecocq in msnoise) or by someone new (Thomas Robitaille in pywwt, Alvaro Ortega in revitpythonshell, Markus Rickert in rl). Outside contributors also restarted work in rosintegration and rlbench, with the maintainer merging.

## When a gap does not mean the project is dead

grassmann.jl's gap was a project that had not really started yet. openram and neurodocker never had a gap of 3+ months, so recovery does not apply. fragit was quiet for over three years but released 1.9.1 in Dec 2023 and has a commit in Apr 2025 on GitHub, and msnoise was among its busiest in 2024 to 2025 after its pause. Recovery can also be thin: rosintegration had only 6 commits in James's data after its gap, mostly outside pull requests.

## Interpretation pitfalls and how I resolved them

1. **Stale or blank data.** James's GitHub columns were empty and his WoC data ended early (neurodocker in 2019, fragit in 2023), so his Currentstatus labels rested on old dates. I used each repo's latest GitHub commit date.
2. **Inflated counts.** His NumCommitsAfterLastGap was far too high for several projects (for example 435 vs 6 for rosintegration), which made recoveries look stronger. I recounted from his summary CSV.
3. **Short pauses treated as gaps.** Projects with no gap of 3+ months should be N/A, not Yes.
4. **Same developer vs new team.** I checked the author names on the first commits after each gap instead of trusting the label.
5. **Pattern vocabulary.** Rising or U-shaped was used for projects that peak early and decline, so I judged each label over the whole timeline.
6. **Theme labels.** Merge and pull-request commits, tie counts and refactoring made themes ambiguous. I put them under Other and counted the same two themes in either order as agreement.

One limit worth stating: kappa for HasRecovered was 0 even though agreement was 80%, because James marked all ten projects Yes. With one rater using a single category, kappa has almost nothing to measure.
