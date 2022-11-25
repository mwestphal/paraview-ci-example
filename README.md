Introduction
============
ParaView CI Example is an example on how to build, test and release a ParaView plugin using CI.
It contains only a very simple ParaView plugin associated with `.gitlab-ci.yml` and`.github/workflows/ci.yml` files.

Everything is handled in the yml files. You can copy the one you need in your own project,
on any gitlab instance or github to be able to build and test your ParaView plugin.

This example is developed by [Kitware SAS][].

[Kitware SAS]: https://www.kitware.eu

Build and test with a ParaView image
====================================
The provided yml files use multiple ParaView versions to build and test.
To select the version, keep the steps using the right `image` tag.
Available images are visible on [paraview-for-ci][] dockerhub repository.

Graphical testing is supported using [xvfb-run][].

[paraview-for-ci]: https://hub.docker.com/r/kitware/paraview-for-ci
[xvfb-run]: https://en.wikipedia.org/wiki/Xvfb

Building a plugin for the paraview.org binary release
=====================================================
The provided yml files also build a plugin compatible with the multiple [paraview.org][] binary releases.
The artifact can be recovered and contains the binary compatible plugin.
To select the version, keep the steps using the right `image` tag.
Available images are visible on [paraview_org-plugin-devel][] dockerhub repository.

[paraview_org-plugin-devel]: https://hub.docker.com/r/kitware/paraview_org-plugin-devel/tags
[paraview.org]: https://paraview.org/download

License
=======

This repository is distributed under the OSI-approved BSD 3-clause License.
The yml files in the repository can alternatively be used under the CC0 license
and, as such, can be copied without mentioning Kitware copyright.
See [License.txt][] for details. For additional licenses, refer to the
[ParaView License][].

[License.txt]: License.txt
[ParaView License]: http://www.paraview.org/paraview-license/

Technicalities
==============

In the .github example, a CI matrix is used to build against different version of ParaView.
Feel free to modify the values in this matrix as you see fit.

In the .gitlab example, jobs can be disabled using CI variables. eg: set `DISABLE_V510` to `True`.
This can be practical when sharing this file among multiples repositories.
