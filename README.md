# playbook-monitoring

Ansible playbook for a simple Prometheus/Grafana setup on Debian-based systems.

Hosts in the `monitoring` group are configured with a default [Alertmanager][],
[Prometheus][] and [Grafana][] installation. The configuration for each service
must be customized locally.

Hosts in the `monitoring_targets` group are configured with a Prometheus
[node_exporter][].

All hosts are configured with nginx and Certbot, unless `nginx` and `certbot`
are set to `false.` The Certbot role requires `certbot_email` to be defined.

Please see the individual roles for more information and defaults.

[alertmanager]: https://prometheus.io/docs/alerting/latest/alertmanager/
[grafana]: https://grafana.com/
[node_exporter]: https://github.com/prometheus/node_exporter
[prometheus]: https://prometheus.io/

## Requirements

- Debian-based system with systemd
- Dependencies installed

```bash
# Install dependencies via Ansible Galaxy
ansible-galaxy install -r requirements-galaxy.yml

# Install dependencies via GitHub
ansible-galaxy install -r requirements-github.yml
```

## License

GNU General Public License v3 or later (GPLv3+)
