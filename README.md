# pm2-monitoring-to-influx
####Send basic pm2 monitoring data to influx db 2.x. Check cloned repo for 1.x support.

This pm2 module sends cpu and memory values for every service running in pm2 to influxdb.  This can then be easily displayed in Grafana for basic monitoring with historial data.

To Install as a pm2 module:
```
pm2 install https://github.com/andmar/pm2-monitoring-to-influx/
```

Then set the interval to monitor in ms and the influxdb credentials. The influx database should already be created:
```
pm2 set pm2-monitoring-to-influx:interval 1000
pm2 set pm2-monitoring-to-influx:host 'hostname'
pm2 set pm2-monitoring-to-influx:token 'token'
pm2 set pm2-monitoring-to-influx:port 8086
pm2 set pm2-monitoring-to-influx:org 'org name or id'
pm2 set pm2-monitoring-to-influx:bucket 'bucket name or id'
```
Then enable the service after configuration is set.
```
pm2 set pm2-monitoring-to-influx:enabled true
```
