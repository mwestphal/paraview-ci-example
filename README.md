# ParaView CI Example

An example project to show how to build and test a plugin
using gitlab CI.

This project is a standard plugin with a .gitlab-ci.yml added to it.

All is handled in .gitlab-ci.yml, you can copy it to your own project
on any gitlab instance to be able to build and test your ParaView plugin
or ParaView based application.

## Choose ParaView image

By default, the latest build of paraview is used.

To build with another paraview image, eg: 5.9.1,
just change the `image` tag in .gitlab-ci.yml to point to another image.

Available images can be seen here: https://hub.docker.com/r/kitware/paraview-for-ci

## Building a plugin for the paraview.org binary release

This repository also shows how to build a ParaView plugin for the paraview.org binary release
in your CI. It builds by default for ParaView v5.10.0, but to choose the version,
just change the `image` tag in the build_release stage image.

Available images can be seen here: https://hub.docker.com/r/kitware/paraview_org-plugin-devel/tags
