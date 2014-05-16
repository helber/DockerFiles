===========
Fedora 18 ssh supervisor
===========

Fedora docker file for ssh service which managed by supervisor

:MAINTAINER:
        Helber Maciel Guerra
        helbermg@gmail.com


**Built and Tested on** Docker-0.11

HOW TO BUILD
------------

- Execute:
.. code-block:: shell
    docker build --rm -t /helber/fedora18-ssh-supervisor .
        + rm - Remove intermediate containers
        + t - Build tag


HOW TO RUN
----------

- Execute:
.. code-block:: shell
docker run -d -p 22 /helber/fedora18-ssh-supervisor

        + d - Run as daemon
        + p - Expose port

CHECK DOCKER STATUS
-------------------

- Execute:
.. code-block:: shell
docker ps

        + It will list running container and provide container ID

CHECK CONTAINER IP
------------------

- Execute:
.. code-block:: shell
docker inspect <Container_ID> | grep IP


TEST SSH SERVICE
----------------
- Execute:
.. code-block:: shell
ssh root@<container_IP>

        + default root passwd is password for This image
