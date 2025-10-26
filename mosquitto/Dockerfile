# Use official Eclipse Mosquitto image as base
FROM eclipse-mosquitto:2.0

# Copy your configuration, password file, and ACL (if any)
COPY mosquitto.conf /mosquitto/config/mosquitto.conf
#COPY passwd /mosquitto/config/passwd
#COPY acl /mosquitto/config/acl

# Expose MQTT (1883) and optional WebSocket (9001) ports
EXPOSE 1883
EXPOSE 9001

# Default command (already provided by base image)
CMD ["/usr/sbin/mosquitto", "-c", "/mosquitto/config/mosquitto.conf"]

