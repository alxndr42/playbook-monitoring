# playbook-monitoring

Ansible playbook for a simple Prometheus/Grafana setup on Debian-based systems.

Hosts in the `monitoring` group are configured with a default [Alertmanager][],
[Prometheus][] and [Grafana][] installation. The configuration for each service
must be customized locally. The Alertmanager installation can be disabled via
`alertmanager: false`.

Hosts in the `node_exporter` group are configured with a [node_exporter][].

Please see `site.yml` and each role's `defaults/main.yml` for details.

## License

GPLv3

[alertmanager]: https://prometheus.io/docs/alerting/latest/alertmanager/
[grafana]: https://grafana.com/
[node_exporter]: https://github.com/prometheus/node_exporter
[prometheus]: https://prometheus.io/
