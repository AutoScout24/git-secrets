# CHANGELOG

## 1.1.0 - 2016-04-06

* Bug fix: the pre-commit hook previously only scanned the working directory
  rather than staged files. This release updates the pre-commit hook to instead
  scan staged files so that git-secrets will detect violations if the working
  directory drifts from the staging directory.
* Added the `--scan-history` subcommand so that you can scan your entire
  git history for violations.
* Added the ability to filter false positives by using a .gitallowed file.
* Added support for `--cached`, `--no-index`, and `--untracked` to the `--scan`
  subcommand.

## 1.0.1 - 2016-01-11

* Now works correctly with filenames in a repository that contain spaces when
  executing `git secrets --scan` with no provided filename (via `git grep`).
* Now works with git repositories with hundreds of thousands of files when
  using `git secrets --scan` with no provided filename (via `git grep`).

## 1.0.0 - 2015-12-10

* Initial release of ``git-secrets``.
