# node_exporter-snap

[![Snap Status](https://build.snapcraft.io/badge/guilhem/node_exporter-snap.svg)](https://build.snapcraft.io/user/guilhem/node_exporter-snap)

snap package for prometheus node_exporter

## Post-installation

The node-exporter snap requires some interfaces to be manually connected in order to grant permission to collect certain metrics. Without these connections, only basic metrics are available. To connect all exposed interfaces, run the following commands after installation:

```bash
snap connect node-exporter:hardware-observe
snap connect node-exporter:mount-observe
snap connect node-exporter:network-observe
snap connect node-exporter:system-observe
```
