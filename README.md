# Mod_Talky_Metrics
## Metrics Module for Prosody

Sends various metrics to the backend of your choice, as used for Talky.io

### Collects metrics from:

* Prosody events
* Jitsi Videobridge component events
* mod_eventlog events

### Supported backends

* Influxdb
* File logging

#### Influxdb

Sends metrics to Influxdb UDP interface

Configuration:

```
talky_metrics = {
    -- Influxdb hostname
    hostname = "127.0.0.1",
    -- UDP port Influxdb is listening to
    port = 4444
}
```

#### File Logging

Saves JSON blobs to a log file

Configuration:

```
talky_metrics = {
    -- Set this to enable file logging
    log_to_file = true,
    -- Where should it log to. Defaults to "/var/log/prosody/metrics.log"
    log_file = "/var/log/prosody/metrics.log",
    -- How big should the metrics logs get until rotation. Defaults to 10240
    log_size = 10240,
    -- How many log files to keep. Defaults to 10
    log_index = 10
}
```