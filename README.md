# Examples for InfluxData Kapacitor

Tested OS:
```
lsb_release -d
Description:    Debian GNU/Linux 10 (buster)
```

Tested Telegraf+InfluxDB+Kapacitor
```
dpkg -l telegraf influxdb kapacitor
Desired=Unknown/Install/Remove/Purge/Hold
| Status=Not/Inst/Conf-files/Unpacked/halF-conf/Half-inst/trig-aWait/Trig-pend
|/ Err?=(none)/Reinst-required (Status,Err: uppercase=bad)
||/ Name           Version      Architecture Description
+++-==============-============-============-===============================================================
ii  influxdb       1.8.1-1      amd64        Distributed time-series database.
ii  kapacitor      1.5.6-1      amd64        Time series data processing engine
ii  telegraf       1.15.2-1     amd64        Plugin-driven server agent for reporting metrics into InfluxDB.
```

Put any of selected examples under your `/etc/kapacitor/load/` directory and reload
kapacitor using:
```bash
systemctl kill -s SIGHUP kapacitor
```


# List of examples

- [tasks/cpu_alert_batch.tick](../../blob/master/tasks/cpu_alert_batch.tick)
  - heavily annotated stock CPU usage example in BATCH mode. Reading this example it should
    become clear what is exactly `.period()` and `.every()` etc...


