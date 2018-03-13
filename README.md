unzeroun/fakes3
===============

Docker image for [fake-s3](https://github.com/jubos/fake-s3)

Inspired by [lphoward/fake-s3](https://github.com/lphoward/fake-s3) but alpine 3.7 based 
(image size of ~62Mb instead of 167Mb for the debian based image.

Assets are by default stored in `/var/lib/fakes3/data`, overridable by CMD.

Default port is 4569.


docker-compose usage:
---------------------

```
version: '3'

services:
    s3:
        image:   unzeroun/fakes3
        ports:   [ '4569:4569' ]
        volumes: [ 's3:/var/lib/fakes3/data' ]

volumes:
    s3: ~


```
