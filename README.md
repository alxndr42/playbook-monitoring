# playbook-monitoring

Ansible playbook for a simple Prometheus/Grafana setup on Debian-based systems.

Hosts in the `monitoring` group are configured with a default [Alertmanager][],
[Prometheus][] and [Grafana][] installation. The configuration for each service
must be customized locally.

Hosts in the `monitoring_targets` group are configured with a Prometheus
[node_exporter][].

Please see the individual roles for more information and defaults.

[alertmanager]: https://prometheus.io/docs/alerting/latest/alertmanager/
[grafana]: https://grafana.com/
[node_exporter]: https://github.com/prometheus/node_exporter
[prometheus]: https://prometheus.io/

## License

GPLv3
