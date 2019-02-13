EmPOWER: Mobile Networks Operating System
=========================================

### What is EmPOWER?
EmPOWER is a new network operating system designed for heterogeneous mobile networks.

### Top-Level Features
* Supports both LTE and WiFi radio access networks
* Northbound abstractions for a global network view, network graph, and
  application intents.
* REST API and native (Python) API for accessing the Northbound abstractions
* Support for Click-based Lightweight Virtual Networks Functions
* Declarative VNF chaning on precise portion of the flowspace
* Flexible southbound interface supporting WiFi APs LTE eNBs

Checkout out our [website](http://empower.create-net.org/) and our [wiki](https://github.com/5g-empower/empower-runtime/wiki)

This repository includes the EmPOWER packages for OpenWRT 15.05.01.

Code is released under the Apache License, Version 2.0.

### How to install

```
  $: cd $TOPDIR
  $: echo 'src-git empower https://github.com/lucaleonardi91/empower-lede-packages.git' >> feeds.conf.default
  $: ./scripts/feeds update empower
  $: ./scripts/feeds install -a -p empower
  $: make menuconfig
  $: select Network -> empower-agent
```

ATTENZIONE
E' fondamentale cambiare le seguenti voci nel make file prima della compilazione in modo da utilizzare la versione aggiornata di empower-lvap-agent:

PKG_VERSION:=20190213
PKG_RELEASE:=1
PKG_REV:=ffa793621d77383ad73862b4f0c9a39ae1e7edd3
