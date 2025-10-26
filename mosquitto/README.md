Build this:
docker build -t my-mosquitto .

Run this:

docker run --network iotnet -d \
  --name mqtt-broker \
  -p 1883:1883 \
  -p 9001:9001 \
  -v ./data:/mosquitto/data \
  -v ./log:/mosquitto/log \
  my-mosquitto


iotnet network must exist:
docker network create iotnet
