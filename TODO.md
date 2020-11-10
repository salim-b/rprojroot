# Steps for adopting older packages to new development standards

## `docs` branch

- [x] Create from last released tag
- [x] Copy `.github/workflows/pkgdown.yaml` there
- [x] Fix URL in DESCRIPTION, don't forget trailing slash
- [x] Tweak `_pkgdown.yml`
- [x] Set source of GitHub Pages to branch

## Separate pull requests

- [x] Use GitHub Actions
- [x] Disable tic
- [x] Disable Travis CI and AppVeyor
- [x] Consider open pull requests
- [x] Tweak README

    - use `downlit::readme_document` and `load_all()` if possible

- [x] Update roxygen2
- [x] Use `@examplesIf` where appropriate
- [x] `styler::style_pkg()`
- [x] Remove `Collate:`
- [x] `usethis::use_lifecycle_badge()`
- [x] `usethis::use_lifecycle()`
- [x] Add pkgdown reference index
- [ ] Adapt tests to testthat 3e
- [ ] Ensure that dependency between source files is cycle-free, as in https://github.com/yonicd/foreman/issues/2
- [ ] Ensure that source files correspond to test files via `devtools::test_coverage_file()`
- [x] Import rlang where appropriate
- [x] Close open issues
- [x] Deprecate functions that have moved somewhere else
- [x] Avoid `iris`
- [x] Synchronize with own downstream packages
- [ ] Add type to documentation of function arguments, as in `?here::here`
- [ ] Check `goodpractice::gp()`
- [ ] Release to CRAN