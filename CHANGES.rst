hmmlearn Changelog
==================

Here you can see the full list of changes between each hmmlearn release.

Version 0.2.0
-------------

- Changed the API to accept multiple sequences via a single feature matrix
  ``X`` and an array of sequence ``lengths``. This allowed to use the HMMs
  as part of scikit-learn ``Pipeline``. The idea was shamelessly plugged
  from ``seqlearn`` package by @larsmans. See issue #29 on GitHub.
- Removed ``params`` and ``init_params`` from internal methods. Accepting
  these as arguments was redundant and confusing, because both available
  as instance attributes.
- Implemented ``ConvergenceMonitor``, a class for convergence diagnostics.
  The idea is due to @mvictor212.
- Added support for non-fully connected architectures, e.g. left-right HMMs.
  Thanks to @matthiasplappert. See issue #33 and PR#38 on GitHub.
- Fixed normalization of emission probabilities in ``MultinomialHMM``, see
  issue #19 on GitHub.
- ``GaussianHMM`` is now initialized from all observations, see #1 on GitHub.
- Changed the models to do input validation lazily as suggested by the
  scikit-learn guidelines.
- Removed deprecated re-exports from ``hmmlean.hmm``.
- Fixed M-step for ``GMMHMM``, which incorrectly expeced ``GMM.score_samples``
  to return log-probabilities. See PR #4 on GitHub for discussion. Thanks to
  @mvictor212 and @michcio1234.

Version 0.1.1
-------------

Initial release, released on February 9th 2015
