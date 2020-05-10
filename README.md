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

## Configuration

Collectors can be enabled/disabled using the `collectors` and `no-collectors` configuration options with this snap. To specify multiple collectors, use a quoted string with space-separated values. For example:

```bash
snap set node-exporter collectors=ntp
snap set node-exporter no-collectors="mdadm netstat"
```

Reference the [prometheus/node_exporter README.md](https://github.com/prometheus/node_exporter/blob/master/README.md#collectors) for the list of collectors enabled by default.
## Contributors :sparkles:
<table>
<tr>
                <td align="center">
                    <a href="https://github.com/desmondgc">
                        <img src="https://avatars2.githubusercontent.com/u/128952?v=4" width="100;" alt="desmondgc"/>
                        <br />
                        <sub><b>Desmond Cox</b></sub>
                    </a>
                </td>
                <td align="center">
                    <a href="https://github.com/guilhem">
                        <img src="https://avatars1.githubusercontent.com/u/486876?v=4" width="100;" alt="guilhem"/>
                        <br />
                        <sub><b>Guilhem Lettron</b></sub>
                    </a>
                </td></tr>
</table>

