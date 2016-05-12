Node services template
======================

## Overview

Template repo for node services.

## How to use it

Limits:

ulimit -n 120000 or more to unlimit the number of total open sockets that the process can has

net.core.rmem_max = 33554432
net.core.wmem_max = 33554432
net.ipv4.tcp_rmem = 4096 16384 33554432
net.ipv4.tcp_wmem = 4096 16384 33554432
net.ipv4.tcp_mem = 786432 1048576 26777216
net.ipv4.tcp_max_tw_buckets = 360000
net.core.netdev_max_backlog = 2500
vm.min_free_kbytes = 65536
vm.swappiness = 0
net.ipv4.ip_local_port_range = 1024 65535

this goes to /etc/sysctl.conf, apply with sysctl -p

## Quick help

* Install modules

```bash
    $ npm install
```

* Check tests

```bash
    $ ./tests.sh
```