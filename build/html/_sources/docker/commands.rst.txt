========
Commands
========


Common commands that I use with docker.

.. attention::
    When using windows use windows power shell to run the docker commands.

Run a container from an image in detached mode and
map port 80 of the host to port 80 in the container:

.. code-block:: docker

    docker run -d -p 80:80 image

Run a container from an image in interactive mode,
remove it afterwards and open a bash within the container:

.. code-block:: docker

    docker run --rm -it image /bin/bash
