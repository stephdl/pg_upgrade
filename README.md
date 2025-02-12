# pg_upgrade
- debian
podman  run --rm 	-e POSTGRES_USER="mattuser" 	-e POSTGRES_DB="mattermost" 	-e POSTGRES_PASSWORD="Nethesis,1234" 	-v postgres-data:/var/lib/postgresql/data:Z 	-v postgres-data17:/var/lib/postgresql/17/main/:Z 	ghcr.io/stephdl/postgres_upgrade:latest



- alpine
podman  run --rm 	-e POSTGRES_USER="mattuser" 	-e POSTGRES_DB="mattermost" 	-e POSTGRES_PASSWORD="Nethesis,1234" 	-v postgres-data:/var/lib/postgresql/data:Z 	-v postgres-data17:/var/lib/postgresql/17/data:Z --env PGDATANEW=/var/lib/postgresql/17/data --env PGDATAOLD=/var/lib/postgresql/data  ghcr.io/stephdl/postgres_upgrade:latest 
