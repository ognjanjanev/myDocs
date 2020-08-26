==========
Dockerfile
==========


Syntax for writing the ``Dockerfile``. A Dockerfile is simply a text-based script of instructions
that is used to create a container image.

Instruction to copy everything from the current directory in the root of the container.

.. code-block:: docker

    COPY . .
