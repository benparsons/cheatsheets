# Synapse

## Purge old media

`curl --header "Authorization: Bearer <access_token>" -X POST "https://matrix.bpulse.org/_synapse/admin/v1/media/bpulse.org/delete?before_ts=<timestamp>"`

- timestamps include ms
- homeserver field ('bpulse.org') is effectively always your local server_name

`curl --header "Authorization: Bearer <access_token>" -X POST "https://matrix.bpulse.org/_synapse/admin/v1/purge_media_cache?before_ts=<timestamp>"`

- timestamps include ms
