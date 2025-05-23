v8.17.6
=======

Bugfixes
--------

- Fix Windows handling in target_for_root. (#28)


v8.17.5
=======

Bugfixes
--------

- Prefer glob for finding files in a possibly-non-existent directory. (#26)


v8.17.4
=======

Bugfixes
--------

- Allow the short parameter for target.


v8.17.3
=======

Bugfixes
--------

- Fix usage when soliciting a path.Path, which typer doesn't support.


v8.17.2
=======

No significant changes.


v8.17.1
=======

Bugfixes
--------

- Make sure workflows isn't consumed before passing to infer_secrets.


v8.17.0
=======

Features
--------

- Add support for adding secrets in coherent projects.


v8.16.2
=======

Bugfixes
--------

- Fix issue in create-github-release with typer usage. (#23)


v8.16.1
=======

Bugfixes
--------

- Add type annotations for base, branch, dry_run, and restore short options to tag and keyword.


v8.16.0
=======

Features
--------

- Migrated from autocommand to typer for CLI handling. (#21)


v8.15.1
=======

Bugfixes
--------

- Use more modern 'is_dir' incantation.


v8.15.0
=======

Features
--------

- Add support for resolving metadata even when pyproject.toml is in conflict. (#19)


v8.14.1
=======

Bugfixes
--------

- Correct failure in configure_fork.


v8.14.0
=======

Features
--------

- When configuring a fork, configure the default repo as the upstream repo (for PRs, etc).


v8.13.0
=======

Features
--------

- Rely on jaraco.packaging.metadata.hunt_down_url to resolve the homepage.


Bugfixes
--------

- Fix bug where migrate-config would fail to include a homepage.
- Inject the URLs agead of project.optional-dependencies, but only if there's not already a homepage indicated.


v8.12.2
=======

Bugfixes
--------

- Fix bug where migrate-config would replace an already multiline contributor with extra space.


v8.12.1
=======

Bugfixes
--------

- Fix typo in migrate-config.


v8.12.0
=======

Features
--------

- Add command for migrating config to pyproject.toml.


v8.11.1
=======

Bugfixes
--------

- Succeed even if git returns no substitutions.


v8.11.0
=======

Features
--------

- Restore Python 3.8 compatibility.


v8.10.1
=======

Bugfixes
--------

- Fix late-add bug in add-project where item was chosen and not attribute.


v8.10.0
=======

Features
--------

- Add routine to add a project.


v8.9.1
======

Bugfixes
--------

- In projects-run, flush stdout.


v8.9.0
======

Features
--------

- In projects-run, implemented selection and exclusion logic for tags and keywords.


v8.8.1
======

Bugfixes
--------

- Fix command syntax in make.


v8.8.0
======

Features
--------

- Updated Python build routine for macOS to support OpenSSL 3. (#16)


v8.7.0
======

Features
--------

- Added support for file:// URL for projects list.


v8.6.0
======

Features
--------

- In merge, ensure that an uncommented RTD badge isn't lost when resolving placeholders.


v8.5.0
======

Features
--------

- Update merge resolver to re-substitute placeholders to honor upstream changes.


v8.4.0
======

Features
--------

- Add 'projects-run' script for running a command across all of the projects.


v8.3.0
======

Features
--------

- Adding script for syncing a backport (configparser, singledispatch) to a CPython branch.


v8.2.0
======

Features
--------

- During finalize, create the newsfragments directory if it doesn't exist.


v8.1.0
======

Features
--------

- Improved handling of unrelated histories and correctly reporting projects updated in update-projects.


v8.0.0
======

Deprecations and Removals
-------------------------

- Replace ``pep517`` with ``build``. ``repo.get_project_metadata`` no longer includes the ``dist``.


v7.25.0
=======

Features
--------

- Added counter to update-projects.


v7.24.0
=======

Features
--------

- Add optional branch parameter to update-projects.


v7.23.0
=======

Features
--------

- Add ``finalize`` command.
- Require Python 3.8 or later.


v7.22.1
=======

* Fixed bug in argument handling of ``towncrier``.

v7.22.0
=======

* Added ``rst-header-replace`` script.

v7.21.0
=======

* Added ``towncrier.check_changes`` from ``setuptools``'
  ``finalize``.

v7.20.0
=======

* Added ``towncrier`` module for invoking towncrier with
  a version calculated based on towncrier news fragments
  in service of jaraco/skeleton#83.

v7.19.0
=======

* Replaced the "skeleton" merge resolver with a "project"
  merge resolver, based on the changes planned for
  jaraco/skeleton#70.

v7.18.0
=======

* ``update-projects`` now accepts a ``tag`` argument.
* ``update-projects`` now allows overriding the base from
  which to update.

v7.17.0
=======

* ``update-projects`` now accepts keyword arguments.
* Added another conflict resolver to ``merge`` module.

v7.16.1
=======

* Actually add the merge module, missed in prior release.

v7.16.0
=======

* Added 'merge' tool toward automatically resolving skeleton changes.

v7.15.0
=======

* Projects are now loaded from ``PROJECTS_LIST_URL`` instead of
  from am embedded text file.

v7.14.0
=======

* ``update-projects`` no longer prompts to edit the commit message.

v7.13.1
=======

* Declare requirement on Python 3.9.
* Fixed test failures in CI.

v7.13.0
=======

* Added performance optimizations on ``update-projects``.

v7.12.0
=======

* "checkout all" script now checks out more projects and lays them
  out according to organization.
* Require Python 3.9 or later.

v7.11.0
=======

* Added ``checkout-all`` script.

v7.10.0
=======

* Added ``update-projects`` script.

v7.9.1
======

* bpo-46975: Fix error in LDFLAGS building Python on macOS.

v7.9.0
======

* Add ``print-meta`` command.

v7.8.0
======

* Enable building of debug Python.

v7.7.0
======

* Added support for installing Wolfram|Alpha API key.

v7.6.0
======

* Prefer ``pep517`` for loading project metadata.

v7.5.0
======

* Switched to PEP 420 for ``jaraco`` namespace.

v7.4.0
======

* Add script to remove namespace.

v7.3.3
======

* #1: Use ``brew list --formula`` to avoid Homebrew error.

v7.3.2
======

* Replace dependency on munch with jaraco.collections, preventing undeclared dependency.

v7.3.1
======

* Actually add the script.

v7.3.0
======

* Add ``add-github-secrets`` routine that auto-detects the secrets needed
  and installs them.

v7.2.2
======

* Fix Python 3.6 compatibility.

v7.2.1
======

* Fixed bug in github.Repo handling (where authentication was missing).

v7.2.0
======

* Add add-github-secret routine.

v7.1.0
======

* Add create-github-release routine.

v7.0.0
======

* Removed many crufty modules and trimmed dependencies.

v6.2.0
======

* macos-build-python now checks that dependencies are installed.

v6.1.0
======

* Improve reliability of macOS build with reference to xz.

v6.0.0
======

* Require Python 3.6 or later.
* Removed 'make-namespace-package' command associated
  functionality in ``namespace`` module.
* Removed Bitbucket-related functionality. Nobody is going
  to need that again.
* Removed Github module. Use `hub <https://hub.github.com/>`_
  command.
* Removed selenium code that is old and with limited utility
  except on Windows.
* Removed all other command-line scripts.

5.0
===

Switch to `pkgutil namespace technique
<https://packaging.python.org/guides/packaging-namespace-packages/#pkgutil-style-namespace-packages>`_
for the ``jaraco`` namespace.

Drop support for Python 3.5.

4.2
===

Updated github to expect a token instead of username/password
in the keyring.

4.1
===

Exposed ``jaraco.develop.lib2to3.patch_for_newlines``.

4.0
===

Refreshed package metadata. Dropped support for Python 3.3.

Added ``jaraco.develop.lib2to3``, which addresses Python #11594
by retaining newlines.

3.0
===

Drop support for Python 3.0.

2.29.1
======

Use ``path.Path`` for compatibility with path.py 10.

2.29
====

Allow creation of Github repositories in an organization.

2.28
====

Moved hosting to Github.

2.27
====

Render README and CHANGES with .rst extensions for nicer rendering
on Github.

2.26
====

Add migration script, adapted from ``bitbucket_issue_migration``.

2.25
====

Add .travis.yml to skeleton.

2.24
====

In project skeleton generation, set default hosting to github.com.

2.23
====

Add github create repo command.

2.22
====

* Include wheels in releases

2.20
====

* Added stub for "extra" dependencies.

2.19
====

* Write templates using LF for line endings.

2.18
====

* Remove documentation link from README in skeleton generation.

2.17
====

* Setup template now includes package data by default.
* Added stub for entry points to define where in the script
  it should appear.

2.16
====

* Regenerated project structure using ``make-namespace-package``.
* Normalized syntax around plat requirements.

2.15
====

* Use setuptools_scm in sphinx config.

2.14
====

* Allow make-namespace-package to complete even when
  the tree already exists.

2.13
====

* Include the jaraco.develop version used to generate the package.

2.12
====

* Add link to documentation from readme.
* Remove changelog from package metadata.
* Include the history in the documentation.

2.11
====

* Drop dependency on jaraco.util.

2.10
====

* Use setuptools_scm.
* Add test = pytest alias.

2.9
===

* Include pytest and sphinx only when indicated.

2.8
===

* Added placeholder for install_requires.
* Use pytest.ini for pytest settings.

2.7
===

* Added sphinx doc and release alias.

2.2
===

* Runs natively on Python 3.

2.1
===

* Specify PyPI for releases.

2.0
===

* Removed 'url' parameter from calls in bitbucket module.
* Now use Requests in favor of restclient for bitbucket operations.

1.10
====

* Added ``add_version`` to ``bitbucket`` module.

1.9
===

* Added command to mark .hg directories as hidden (Windows).

1.8
===

* Added keyring support for bitbucket operations.
* Added command to patch hgrc files in a tree (patch-hgrc).

1.7
===

* Added support for recursive globs in indent module.

1.6.3
=====

* Updated jaraco.develop.msvc to support Python 3.

1.6.2
=====

* create-namespace-package will now also generate non-namespace packages.

1.6.1
=====

* Updated create-bitbucket-repository command so it now passes the new
  required parameter 'scm' (always mercurial).

1.6
===

* Added `compiler` module with a function `can_compile_extension` which
  will check if distutils can likely compile an extension module.

1.5
===

* Added build-python command, which finds Visual Studio, loads the
  appropriate environment, and then builds Python in the current PCBuild
  directory.
* Added vs-upgrade command which will take a Visual Studio project or solution
  file and upgrade it to the latest version.

1.4
===

* Added support for 4-space indentation in namespace package generation.
* Added preliminary bitbucket support (create-repo command).
* Added Python 3 support.

1.3
===

* Added package module (from jaraco.util).
* Added some helpful routines for invoking saucelabs including shortcuts
  for selecting browsers.
* Added a script to create the simple namespace package configuration.
* Added env_tool from the Gryphon project.

1.2
===

* Adding module for patching the msvc9compiler module
* Added command-line options to start-selenium

1.1
===

* Added routines for working with the Core CPython project (building,
  applying patches, etc).

1.0
===

* Initial release
