---
title: My Unbound DNS custom options
author: Danesh Manoharan
date: 2020-12-12T04:55:57+00:00

---
I'm running Unbound DNS on OPNsense at home. This covers my local PLEX server and DOH (DNS OVER HTTPs) setup. All my devices point to my PiHole server which then forwards them to the unbound server.

```text
server:
private-domain: "plex.direct"
server:
forward-zone:
  name: "."
  forward-addr: 1.1.1.1@853
  forward-addr: 1.0.0.1@853
  forward-addr: 8.8.8.8@853
  forward-addr: 8.8.4.4@853
  forward-addr: 2606:4700:4700::1111@853
  forward-addr: 2606:4700:4700::1001@853
  forward-addr: 2001:4860:4860::8888@853
  forward-addr: 2001:4860:4860::8844@853
  forward-ssl-upstream: yes
  ```
