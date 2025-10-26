Build this:
docker build -t my-nodered:mini .


Run this:
docker run --network iotnet -d --name nodered \
  -p 1880:1880 \
  -e TZ=Europe/Zagreb \
  -v nodered-data:/data \
  my-nodered:mini


iotnet network must exist:
docker network create iotnet
