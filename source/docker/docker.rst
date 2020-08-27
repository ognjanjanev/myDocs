======
docker
======


Some common commands that I use with docker.

.. attention::
    When using windows use windows power shell to run the docker commands.
    
pull
====

Pull an image (``docker pull image``) with the specified version(``:version``):

.. code-block:: docker

    docker pull image:version

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
        
exec
====

Open a bash terminal interactively (``-it``) in a running container with the id (``ic``).

.. code-block:: docker

    docker exec -it 1c bash

Display a file contents in a running container.

.. code-block:: docker

    docker exec <container id> cat filename

container
=========

Show all containers (``ls --all``), running and inactive:

.. code-block:: docker

    docker container ls --all
    docker ps -a

Remove (``rm``) docker container with the id 12345:

.. code-block:: docker

    docker container rm 12345
    docker rm 12345

Forcely (``-f``) stop a running container ad remove it:

.. code-block:: docker

    docker container rm -f <the-container-id>
    docker rm -f <the-container-id>

tag
===

Create a copy of an image with a new name. (to be able to push it on docker hub)

.. code-block:: docker

    docker tag image-name ognjanjanev/image-name

push
====

Push a docker image on docker hub.

.. note::

    Create a repository for your app on docker hub
    for example ognjanjanev/image-name. Then push your
    local image with the command bellow.

    If no image-tag is given latest will be pushed.

.. code-block:: docker

    docker push ognjanjanev/image-name:image-tag

volume
======

Create a volume, mount it (``-v todo-db:/etc/todo-db``) and inspect it.

.. code-block:: docker

    docker volume create todo-db
    docker run -dp 3000:3000 -v todo-db:/etc/todo-db image
    docker volume inspect todo-db