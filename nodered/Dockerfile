FROM nodered/node-red:latest-minimal
ENV TZ=Europe/Zagreb

# Copy your exported flows into the image
COPY seed/flows.json /usr/src/node-red/seed/flows.json

USER node-red
RUN npm install --no-audit --no-fund node-red-dashboard

# Always overwrite flows.json and set correct ownership on every start
CMD ["/bin/sh","-lc","\
  cp /usr/src/node-red/seed/flows.json /data/flows.json; \
  chown node-red:node-red /data/flows.json 2>/dev/null || true; \
  exec npm start -- --userDir /data"]

