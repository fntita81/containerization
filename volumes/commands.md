Create a Dockerfile and write
VOLUME [“/myvolume”]
RUN ”touch f1”

docker build -t image3.

docker run-it-name cont-3 image3 /bin/bash

Now do Is you see volume.
Now share volume with another container.
docker run -it --name cont-4(new) –privileged=true --volumes-from cont-3 image-3 /bin/bash
