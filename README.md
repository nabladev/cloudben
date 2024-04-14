# `cloudben`

**Usage**:

```console
$ cloudben [OPTIONS] COMMAND [ARGS]...
```

**Options**:

* `--install-completion`: Install completion for the current shell.
* `--show-completion`: Show completion for the current shell, to copy it or customize the installation.
* `--help`: Show this message and exit.

**Commands**:

* `create-record`
* `delete-record`
* `delete-records`
* `get-records`

## `cloudben create-record`

**Usage**:

```console
$ cloudben create-record [OPTIONS] ZONE_ID NAME CONTENT TYPE:{A|CNAME|AAAA|TXT|MX}
```

**Arguments**:

* `ZONE_ID`: your zone id  [required]
* `NAME`: name of the Cloudflare record  [required]
* `CONTENT`: value of the Cloudflare record (what the record will resolve to)  [required]
* `TYPE:{A|CNAME|AAAA|TXT|MX}`: type of the Cloudflare record  [required]

**Options**:

* `--priority INTEGER RANGE`: priority of the TXT record  [default: 0; 0<=x<=65535]
* `--json / --no-json`: will output valid JSON. It can we useful when using this command in your script. Vanity logging will be disabled  [default: no-json]
* `--help`: Show this message and exit.

## `cloudben delete-record`

**Usage**:

```console
$ cloudben delete-record [OPTIONS] ZONE_ID RECORD_ID
```

**Arguments**:

* `ZONE_ID`: your zone id  [required]
* `RECORD_ID`: id of the record to delete  [required]

**Options**:

* `--force`: Do not ask for confirmation when deleting.
* `--help`: Show this message and exit.

## `cloudben delete-records`

**Usage**:

```console
$ cloudben delete-records [OPTIONS] ZONE_ID QUERY
```

**Arguments**:

* `ZONE_ID`: your zone id  [required]
* `QUERY`: Text to be contained in the record's name.  [required]

**Options**:

* `--force`: Do not ask for confirmation when deleting.
* `--help`: Show this message and exit.

## `cloudben get-records`

**Usage**:

```console
$ cloudben get-records [OPTIONS] ZONE_ID
```

**Arguments**:

* `ZONE_ID`: your zone id  [required]

**Options**:

* `--query TEXT`: Text to be contained in the record's name.
* `--json / --no-json`: will output valid JSON. It can we useful when using this command in your script. Vanity logging will be disabled  [default: no-json]
* `--help`: Show this message and exit.
