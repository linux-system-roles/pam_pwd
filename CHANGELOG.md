Changelog
=========

[0.0.14] - 2024-10-30
--------------------

### Other Changes

- ci: Add tft plan and workflow (#67)
- ci: Update fmf plan to add a separate job to prepare managed nodes (#69)
- ci: Bump sclorg/testing-farm-as-github-action from 2 to 3 (#70)
- ci: Add workflow for ci_test bad, use remote fmf plan (#71)
- ci: Fix missing slash in ARTIFACTS_URL (#72)
- ci: Add tags to TF workflow, allow more [citest bad] formats (#73)
- docs: Update contact email address (#74)
- ci: ansible-test action now requires ansible-core version (#75)
- ci: add YAML header to github action workflow files (#76)
- refactor: Use vars/RedHat_N.yml symlink for CentOS, Rocky, Alma wherever possible (#78)

[0.0.13] - 2024-07-02
--------------------

### Bug Fixes

- fix: add support for EL10 (#65)

### Other Changes

- ci: ansible-lint action now requires absolute directory (#64)

[0.0.12] - 2024-06-11
--------------------

### Other Changes

- ci: use tox-lsr 3.3.0 which uses ansible-test 2.17 (#59)
- ci: tox-lsr 3.4.0 - fix py27 tests; move other checks to py310 (#61)
- ci: Add supported_ansible_also to .ansible-lint (#62)

[0.0.11] - 2024-04-04
--------------------

### Other Changes

- ci: fix python unit test - copy pytest config to tests/unit (#55)
- ci: Bump ansible/ansible-lint from 6 to 24 (#56)
- ci: Bump mathieudutour/github-tag-action from 6.1 to 6.2 (#57)

[0.0.10] - 2024-01-16
--------------------

### Other Changes

- ci: support ansible-lint and ansible-test 2.16 (#52)
- ci: Use supported ansible-lint action; run ansible-lint against the collection (#53)

[0.0.9] - 2023-12-08
--------------------

### Other Changes

- ci: Bump actions/github-script from 6 to 7 (#49)
- refactor: get_ostree_data.sh use env shebang - remove from .sanity* (#50)

[0.0.8] - 2023-11-29
--------------------

### Other Changes

- Bump actions/checkout from 3 to 4 (#40)
- ci: ensure dependabot git commit message conforms to commitlint (#43)
- ci: tox-lsr version 3.1.1 (#47)

[0.0.7] - 2023-09-08
--------------------

### Other Changes

- ci: Add markdownlint, test_converting_readme, and build_docs workflows (#36)

  - markdownlint runs against README.md to avoid any issues with
    converting it to HTML
  - test_converting_readme converts README.md > HTML and uploads this test
    artifact to ensure that conversion works fine
  - build_docs converts README.md > HTML and pushes the result to the
    docs branch to publish dosc to GitHub pages site.
  - Fix markdown issues in README.md
  
  Signed-off-by: Sergei Petrosian <spetrosi@redhat.com>

- docs: Make badges consistent, run markdownlint on all .md files (#37)

  - Consistently generate badges for GH workflows in README RHELPLAN-146921
  - Run markdownlint on all .md files
  - Add custom-woke-action if not used already
  - Rename woke action to Woke for a pretty badge
  
  Signed-off-by: Sergei Petrosian <spetrosi@redhat.com>

- ci: Remove badges from README.md prior to converting to HTML (#38)

  - Remove thematic break after badges
  - Remove badges from README.md prior to converting to HTML
  
  Signed-off-by: Sergei Petrosian <spetrosi@redhat.com>

[0.0.6] - 2023-07-19
--------------------

### Other Changes

- ci: Add pull request template and run commitlint on PR title only (#32)
- ci: Rename commitlint to PR title Lint, echo PR titles from env var (#33)
- ci: ansible-lint - ignore var-naming[no-role-prefix] (#34)

[0.0.5] - 2023-05-23
--------------------

### Other Changes

- docs: Consistent contributing.md for all roles - allow role specific contributing.md section
- docs: remove unused Dependencies section in README
- ci: update tox-lsr to version 3.0.0
- test: ensure facts for tests_include_vars_from_parent.yml

[0.0.4] - 2023-04-27
--------------------

### Other Changes

- ci: Add commitlint GitHub action to ensure conventional commits with feedback

[0.0.3] - 2023-04-13
--------------------

### Other Changes

- ansible-lint - use changed_when on conditional tasks (#22)

[0.0.2] - 2023-04-06
--------------------

### Other Changes

- Add check for non-inclusive language
- fix ansible-lint issues (#16)
- Add README-ansible.md to refer Ansible intro page on linux-system-roles.github.io (#20)

Changelog
=========

[0.0.1] - 2022-07-20
--------------------

### New Features

- initial version

### Bug Fixes

- none

### Other Changes

- none

