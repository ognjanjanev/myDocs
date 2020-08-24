======
docker
======


Common commands that I use with docker.

.. attention::
    When using windows use windows power shell to run the docker commands.

run
===

Run a container (``docker run``) from an image (``image``) in detached (``-d``) mode
and map port 80 of the host to port 80 in the container (``-p 80:80``):

.. code-block:: docker

    docker run -d -p 80:80 image

.. tip::
    You can also abbreviate the options form ``-d -p`` to ``-dp``.

Run a container (``docker run``) from an image(``image``) in interactive mode (``-it``),
remove(``--rm``) it afterwards and open a bash within the container (``/bin/bash``):

.. code-block:: docker

    docker run --rm -it image /bin/bash

build
=====

Build a docker image (``docker build``), and create a name tag
with the name getting-started (``-t getting-started``) from a
Dockerfile in the current directory (``.``):

.. code-block:: docker

    docker build -t getting-started .
