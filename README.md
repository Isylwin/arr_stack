# WHAT IS IT

This will set a *arr stack containing:
- Radarr -> management of movies
- Prowlarr -> management of indexers
- Bazarr -> management of subtitles
- qbittorrent -> management of legal things

# ENV VARS

The following env vars need to be defined in a `.env`:

```
HOST_STORAGE_FOLDER="path_to_host_directory_where_all_files_can_be_stored"            
HOST_CONFIG_FOLDER="path_to_host_directory_where_configs_can_be_stored"
CONT_STORAGE_FOLDER="path_to_container_directory_where_all_files_can_be_stored"
CONT_CONFIG_FOLDER="path_to_container_directory_where_configs_can_be_stored"
```

An example could be:

```
HOST_STORAGE_FOLDER=/mnt/media
HOST_CONFIG_FOLDER=/home/username/data/arr_stack
CONT_STORAGE_FOLDER=/media
CONT_CONFIG_FOLDER=/config
```

# RUNNING

Set up the env vars described above.
Run all containers by using `docker compose up -d`
Update all containers, when necessary, with `docker compose pull && docker compose up -d`

The applications will be running under:
- Bazarr - 6767
- Prowlarr - 9696
- Radarr - 7878
- qbittorrent - 8080
