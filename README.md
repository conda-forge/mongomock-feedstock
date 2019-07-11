About mongomock
===============

Home: https://github.com/mongomock/mongomock

Package license: BSD-3-Clause

Feedstock license: BSD 3-Clause

Summary: Small library for mocking pymongo collection objects for testing purposes

Mongomock is a small library to help testing Python code that interacts with
MongoDB via Pymongo.

MongoDB is complex. This library aims at a reasonably complete mock of
MongoDB for testing purposes, not a perfect replica. This means some
features are not likely to make it in any time soon.

Also, since many corner cases are encountered along the way, our goal is to
try and TDD our way into completeness. This means that every time we
encounter a missing or broken (incompatible) feature, we write a test for
it and fix it. There are probably lots of such issues hiding around
lurking, so feel free to open issues and/or pull requests and help the
project out!

NOTE: We don't include pymongo functionality as "stubs" or "placeholders".
Since this library is used to validate production code, it is unacceptable
to behave differently than the real pymongo implementation. In such cases
it is better to throw NotImplementedError than implement a modified version
of the original behavior.


Current build status
====================


<table><tr><td>All platforms:</td>
    <td>
      <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=7091&branchName=master">
        <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/mongomock-feedstock?branchName=master">
      </a>
    </td>
  </tr>
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-mongomock-green.svg)](https://anaconda.org/conda-forge/mongomock) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/mongomock.svg)](https://anaconda.org/conda-forge/mongomock) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/mongomock.svg)](https://anaconda.org/conda-forge/mongomock) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/mongomock.svg)](https://anaconda.org/conda-forge/mongomock) |

Installing mongomock
====================

Installing `mongomock` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
```

Once the `conda-forge` channel has been enabled, `mongomock` can be installed with:

```
conda install mongomock
```

It is possible to list all of the versions of `mongomock` available on your platform with:

```
conda search mongomock --channel conda-forge
```


About conda-forge
=================

[![Powered by NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](http://numfocus.org)

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[CircleCI](https://circleci.com/), [AppVeyor](https://www.appveyor.com/)
and [TravisCI](https://travis-ci.org/) it is possible to build and upload installable
packages to the [conda-forge](https://anaconda.org/conda-forge)
[Anaconda-Cloud](https://anaconda.org/) channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](https://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating mongomock-feedstock
============================

If you would like to improve the mongomock recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/mongomock-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://conda.io/docs/user-guide/tasks/build-packages/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://conda.io/docs/user-guide/tasks/build-packages/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@birnbaum](https://github.com/birnbaum/)
* [@mathiaseitz](https://github.com/mathiaseitz/)
* [@trendelkampschroer](https://github.com/trendelkampschroer/)

