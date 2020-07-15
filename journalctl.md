# journalctl

## -f

As in `tail -f`.

## Select unit

`-u name`

As in `journalctl -u matrix-synapse`

## --since --until

`journalctl --since "1 hour ago"`

`journalctl --since "2 days ago"`

`journalctl --since "2020-06-26 00:00:00" --until "2020-06-26 00:00:00"`

## just pipe into grep

eg
`journalctl -u matrix-synapse --since "1 hour ago" | grep servername`
