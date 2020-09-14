---
layout: post
title: SFWEM Intranet Resouces Page Now Live
---
The Mesh Ops team is happy to announce the new SFWEM Intranet Resources page, taking advantage of a new feature added in the ARDEN Nightly Builds from 11 September 2020 that allows the publishing of CNAME DNS records via OSLR. Big thanks to Eric, KG6WXC for coding this feature (along with many others!) in the AREDN firmware.
<!--more-->
The site currently provides a place for operations-oriented buletins that doesn't depend on the public internet, as well as a AREDN Alert Messages (AAM) API endpoint for nodes to access. Eventually, it will also provide links to helpful apps on the mesh we want to highlight, a copy of the SFWEM and AREDN ReadTheDocs.io documentation, and other resources.

The site is hosted using Nginx on a Docker Swarm cluster hosted by Kiley, KD8DRX. While currenty located in LA (Kiley's QTH), the cluster serves as a proof-of-concept for a similar setup that will be deployed to a hardened site in San Francisco on the RF Mesh. In addition to the resoures page, the cluster hosts a tileserver, local AREDN Alert Messages server, APT mirror, and similar tools that will help Radio Amateurs, technologists, and served agencies remain fully operatoinal in a diaster.