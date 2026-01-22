[MetaCheck](http://www.scienceverse.org/metacheck) version 0.0.0.9061  
Report Created: 2025-12-17

------------------------------------------------------------------------

🟢 no problems detected;  
🟡 something to check;  
🔴 possible problems detected;  
🔵 informational only;  
⚪️ not applicable;  
⚫️ check failed

## Summary

- [Causal Claims](#causal-claims): No causal claims were observed in the
  title. No causal claims were observed in the abstract.  
- [Preregistration Check](#preregistration-check): We found 1
  preregistration.  
- [AsPredicted](#aspredicted): 1 AsPredicted link was found and
  retrieved.  
- [Power](#power): You included power analysis, but some essential
  reporting aspects appear missing.  
- [Exact P-Values](#exact-p-values): We found 1 imprecise *p* value out
  of 3 detected.  
- [Non-Significant P Value Check](#non-significant-p-value-check): We
  found 2 non-significant p values that should be checked for
  appropriate interpretation.  
- [Marginal Significance](#marginal-significance): You described 2
  effects with terms related to ‘marginally significant’.  
- [Effect Sizes in t-tests and
  F-tests](#effect-sizes-in-t-tests-and-f-tests): We found 1 t-test
  and/or F-test where effect sizes are not reported.  
- [Code Check](#code-check): Some files loaded in the R scripts were
  missing in the repository. Hardcoded file paths were found. Libraries
  were loaded in multiple places. 1 file had no comments.  
- [StatCheck](#statcheck): 1 possible error in t-tests or F-tests  
- [Reference Check](#reference-check): We retrieved 1 of 1 missing DOI
  from crossref. We found 1 reference with comments on Pubpeer. You have
  cited 1 article for which replication studies exist. You have cited 1
  article for which entries in the Retraction Watch database exist.  
- [Miscitation](#miscitation): We detected no miscited papers  
- [RetractionWatch](#retractionwatch): You cited 1 paper in the
  Retraction Watch database

## Causal Claims

Medical journals often have the following instruction in the author
guidelines about the use of causal language:  
  
*Causal language (including use of terms such as effect and efficacy)
should be used only for randomized clinical trials. For all other study
designs (including meta-analyses of randomized clinical trials), methods
and results should be described in terms of association or correlation
and should avoid cause-and-effect wording.*

No causal claims were observed in the abstract,

Learn More

For advice on how to make causal claims, and when not to, see:

Antonakis, J., Bendahan, S., Jacquart, P., & Lalive, R. (2010). On
making causal claims: A review and recommendations. The Leadership
Quarterly, 21(6), 1086–1120.
[https://doi.org/10.1016/j.leaqua.2010.10.010](https://doi.org/10.1016/j.leaqua.2010.10.010)

Grosz, M. P., Rohrer, J. M., & Thoemmes, F. (2020). The Taboo Against
Explicit Causal Inference in Nonexperimental Psychology. Perspectives on
Psychological Science, 15(5), 1243–1255.
[https://doi.org/10.1177/1745691620921521](https://doi.org/10.1177/1745691620921521)

## Preregistration Check

We found 1 preregistration from AsPredicted. Meta-scientific research
has shown that deviations from preregistrations are often not reported
or checked, and that the most common deviations concern the sample size.
We recommend manually checking the full preregistration at the link
below. If you check one aspect of the preregistration, make it the
preregistered sample size.

#### Preregistered Sample Size

Full preregistration

Learn More

**For metascientific work on preregistration deviations**:

van den Akker, O. R. et al. (2024). The potential of preregistration in
psychology: Assessing preregistration producibility and
preregistration-study consistency. *Psychological Methods*. DOI:
[10.1037/met0000687](https://doi.org/10.1037/met0000687)

**For educational material on reporting deviations from
preregistrations**:

Lakens, D. (2024). When and How to Deviate From a Preregistration.
*Collabra: Psychology*, 10(1), 117094. DOI:
[10.1525/collabra.117094](https://doi.org/10.1525/collabra.117094)

## AsPredicted

1 AsPredicted link was found and retrieved.

Sample size is most common deviation. This is what was stated about
sample size:

> We randomly assigned 50 scientists to a condition where their
> manuscript was automatically checked for errors, and 50 scientists to
> a control condition with a checklist.

## Power

You included power analysis, but some essential reporting aspects appear
missing.

Power analyses need to contain the following information to be
interpretable: the statistical test, sample size, critical alpha
criterion, power level, effect size, and an effect size metric. For
example:

> An a priori power analysis for an independent samples t-test,
> conducted using the pwr.t.test function from pwr (Champely, 2020) with
> Cohen’s d = 0.5 and a critical alpha of p = 0.05, determined that 64
> participants are required in each group for 80% power.

## Exact P-Values

We found 1 imprecise *p* value out of 3 detected. Reporting *p* values
imprecisely (e.g., *p* \< .05) reduces transparency, reproducibility,
and re-use (e.g., in *p* value meta-analyses). Best practice is to
report exact p-values with three decimal places (e.g., *p* = .032)
unless *p* values are smaller than 0.001, in which case you can use *p*
\< .001.

Learn More

The APA manual states: Report exact *p* values (e.g., *p* = .031) to two
or three decimal places. However, report *p* values less than .001 as
*p* \< .001. However, 2 decimals is too imprecise for many use-cases
(e.g., a *p* value meta-analysis), so report *p* values with three
digits.

American Psychological Association. (2020). Publication manual of the
American Psychological Association 2020: the official guide to APA style
(7th ed.). American Psychological Association.

## Non-Significant P Value Check

We found 2 non-significant p values that should be checked for
appropriate interpretation.

Meta-scientific research has shown nonsignificant p values are commonly
misinterpreted. It is incorrect to infer that there is ‘no effect’, ‘no
difference’, or that groups are ‘the same’ after p \> 0.05.

It is possible that there is a true non-zero effect, but that the study
did not detect it. Make sure your inference acknowledges that it is
possible that there is a non-zero effect. It is correct to include the
effect is ‘not significantly’ different, although this just restates
that p \> 0.05.

Metacheck does not yet analyze automatically whether sentences which
include non-significant p-values are correct, but we recommend manually
checking the sentences below for possible misinterpreted non-significant
p values.

Learn More

For metascientific articles demonstrating the rate of misinterpretations
of non-significant results is high, see:

- Aczel, B., Palfi, B., Szollosi, A., Kovacs, M., Szaszi, B., Szecsi,
  P., Zrubka, M., Gronau, Q. F., van den Bergh, D., & Wagenmakers, E.-J.
  (2018). Quantifying Support for the Null Hypothesis in Psychology: An
  Empirical Investigation. *Advances in Methods and Practices in
  Psychological Science*, 1(3), 357–366. doi:
  [10.1177/2515245918773742](https://doi.org/10.1177/2515245918773742)

- Murphy, S. L., Merz, R., Reimann, L.-E., & Fernández, A. (2025).
  Nonsignificance misinterpreted as an effect’s absence in psychology:
  Prevalence and temporal analyses. *Royal Society Open Science*,
  12(3), 242167. doi:
  [10.1098/rsos.242167](https://doi.org/10.1098/rsos.242167)

For educational material on preventing the misinterpretation of p
values, see:
[lakens.github.io/statistical_inferences](https://lakens.github.io/statistical_inferences/01-pvalue.html#sec-misconception1).

## Marginal Significance

You described effects with terms related to ‘marginally significant’. If
*p* values above 0.05 are interpreted as an effect, you inflate the
alpha level, and increase the Type 1 error rate. If a *p* value is
higher than the prespecified alpha level, it should be interpreted as a
non-significant result.

Learn More

For metascientific articles demonstrating the rate at which
non-significant p-values are interpreted as marginally significant, see:

Olsson-Collentine, A., van Assen, M. A. L. M., & Hartgerink, C. H. J.
(2019). The Prevalence of Marginally Significant Results in Psychology
Over Time. Psychological Science, 30(4), 576–586.

<https://doi.org/10.1177/0956797619830326>

For the list of terms used to identifify marginally significant results,
see this blog post by Matthew Hankins:

<https://web.archive.org/web/20251001114321/https://mchankins.wordpress.com/2013/04/21/still-not-significant-2/>

## Effect Sizes in t-tests and F-tests

We found 1 t-test and/or F-test where effect sizes are not reported. We
recommend checking the sentences below, and add any missing effect
sizes.

The following sentences are missing effect sizes

Learn More

For metascientific articles demonstrating that effect sizes are often
not reported:

- Peng, C.-Y. J., Chen, L.-T., Chiang, H.-M., & Chiang, Y.-C. (2013).
  The Impact of APA and AERA Guidelines on Effect Size Reporting.
  Educational Psychology Review, 25(2), 157–209.
  doi:[10.1007/s10648-013-9218-2](https://doi.org/10.1007/s10648-013-9218-2).

For educational material on reporting effect sizes:

- [Guide to Effect Sizes and Confidence
  Intervals](https://matthewbjane.quarto.pub/guide-to-effect-sizes-and-confidence-intervals/)

All detected and assessed stats

## Code Check

Below, we describe some best coding practices and give the results of
automatic evaluation of these practices in the R files below. This check
may miss things or produce false positives if your R scripts are less
typical.

### Missing Files

The scripts load files, but 3 scripts loaded 3 files that could not be
automatically identified in the repository. Check if the following files
are made available, so that others can reproduce your code, or that the
files are missing:

### Hardcoded Paths

Best programming practice is to use relative file paths instead of
hardcoded file paths (e.g., C://Lakens/files) as these folder names are
do not exist on other computers. The following 4 hardcoded file paths
were found in 3 R file(s).

### Libraries

Best programming practice is to load all required libraries at one place
in the code. In 3 R files, libraries were at multiple places in the R
files (i.e., with more than 3 lines in between). This was true in the
following R files, where libraries were loaded on the following lines:

### Code Comments

Best programming practice is to add comments to code, to explain what
the code does (to yourself in the future, or peers who want to re-use
your code. The following 1 file had no comments:

## StatCheck

We detected possible errors in test statistics. Note that as the
accuracy of statcheck has only been validated for *t*-tests and
*F*-tests. As Metacheck only uses validated modules, we only provide
statcheck results for *t* tests and *F*-tests.

Learn More

For metascientific research on the validity of statcheck, and it’s
usefulness to prevent statistical reporting errors, see:  
  

Nuijten, M. B., van Assen, M. A. L. M., Hartgerink, C. H. J., Epskamp,
S., & Wicherts, J. M. (2017). The Validity of the Tool “statcheck” in
Discovering Statistical Reporting Inconsistencies. PsyArXiv. doi:
[10.31234/osf.io/tcxaja](https://doi.org/10.31234/osf.io/tcxaja)

Nuijten, M. B., & Wicherts, J. (2023). The effectiveness of implementing
statcheck in the peer review process to avoid statistical reporting
errors. PsyArXiv. doi:
[10.31234/osf.io/bxau9](https://doi.org/10.31234/osf.io/bxau9)

## Reference Check

This module only checks references classified as articles. Out of 4
references to articles in the reference list, 4 have a DOI.

### Missing DOIs

We retrieved 1 of 1 missing DOI from crossref. Only missing DOIs with a
match score \> 50 are returned to have high enough accuracy.
Double-check any suggested DOIs and check if the remaining missing DOIs
are available.

### PubPeer Comments

We found 1 reference with comments on Pubpeer. Pubpeer is a platform for
post-publication peer review. We have filtered out Pubpeer comments by
‘Statcheck’. You can check out the comments by visiting the URLs below:

### Replication Studies

You have cited 1 article for which replication studies exist. These
replications were listed in the FORRT Replication Database (as of
2025-11-24). Check if you are aware of the replication studies, and cite
them where appropriate.

### RetractionWatch

You have cited 1 article for which entries in the Retraction Watch
database exist. These articles were listed in the Retraction Watch
database (as of 2025-12-04). Check if you are aware of the issues, and
cite them where appropriate.

## Miscitation

We detected no miscited papers

## RetractionWatch

You cited 1 paper in the Retraction Watch database (as of 2025-12-04).
These may be retracted, have corrections, or expressions of concern.
