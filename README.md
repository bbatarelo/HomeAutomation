
Build everything (mosquito and node red) from scratch and run

docker compose up -d --build

Teardown everything including persisted data

docker compose down -v

Note: use sudo on Synology
Note: in case Node Red flows were modified, export them (to clipboard) before tearing down the container. Persist those changes if needed in flows.json (seed directory)
