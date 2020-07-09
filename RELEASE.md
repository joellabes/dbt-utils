# dbt-utils releases

As of July 2020, a new minor release of `dbt-utils` will be released in line with
a new minor release of `dbt`. The `dbt-utils` release number will share the same
major and minor numbers. Patch numbers may diverge.

Breaking changes and new functionality should wait for a new minor release,
while fixes can be released with a patch release.

## Branching
For each new dbt minor version, we will create a new (un-released) dbt branch,
which will appear as the main branch on GitHub. New PRs (except for bug-fixes)
should be made against this branch


## Release checklist
When creating a new release
1. Check if there were any patch releases. If so, make sure you rebase the active branch onto the latest release.

2. Create a new PR that ensures that:
  - [ ] The `require-dbt-version` config has been incremented, e.g. `">=0.18.0"`
  - [ ] The dbt version in [run_test.sh](run_test) should be incremented `pip install  "dbt>=0.18.0,<0.19.0"`
  - [ ] The release number matches the dbt major and minor release, e.g. `0.18.0`
  - [ ] The [changelog](CHANGELOG.md) is updated

3. Create the release

4. Create a new branch for the next release, named `dev/0.19.0`, and make it the default branch
