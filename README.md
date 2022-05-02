Introduction
============
ParaView CI Example is example on how to build and test a ParaView plugin using CI.
It contains only a very simple ParaView associated with a `.gitlab-ci.yml` file.

All is handled in `.gitlab-ci.yml`, you can copy it to your own project
on any gitlab instance to be able to build and test your ParaView plugin
or ParaView based application.

This example is developed by [Kitware SAS][].

[Kitware SAS]: https://www.kitware.eu

Build and test with a ParaView image
====================================
The provided `.gitlab-ci.yml` use ParaView 5.10.1 to build and test.
To choose another version, just change the `image` tag in .gitlab-ci.yml to point to another image.
Available images are visible on [paraview-for-ci][] dockerhub repository.

Graphical testing is supported using a [Xvfb][] entry point.

[paraview-for-ci]: https://hub.docker.com/r/kitware/paraview-for-ci
[Xvfb]: https://en.wikipedia.org/wiki/Xvfb

Building a plugin for the paraview.org binary release
=====================================================
The provided `.gitlab-ci.yml` also build a plugin compatible with the [paraview.org][] 5.10.1 binary release.
The artifact can be recovered and contains the compatible binary plugin.
To build a plugin compatible with another version, just change the `image` tag in the build_plugin_release stage.
Available images are visible on [paraview_org-plugin-devel][] dockerhub repository.

[paraview_org-plugin-devel]: https://hub.docker.com/r/kitware/paraview_org-plugin-devel/tags

License
=======

This repository is distributed under the OSI-approved BSD 3-clause License.
See [License.txt][] for details. For additional licenses, refer to the
[ParaView License][].

[License.txt]: License.txt
[ParaView License]: http://www.paraview.org/paraview-license/
