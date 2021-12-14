# ParaView CI Example

An example project to show how to build and test a plugin
using gitlab CI.

This project is a standard plugin with a .gitlab-ci.yml added to it.

All is handled in .gitlab-ci.yml, you can copy it to your own project
on gitlab.kitware.io to be able to build and test your ParaView plugin
or ParaView based application.

## Choose ParaView image

To build with another paraview image, just change the `image` tag on top of the .gitlab-ci.yml 
to point to another image.

Available images can be seen here: 
https://gitlab.kitware.io/visualization/paraview-image-builder/container_registry
