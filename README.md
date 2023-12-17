# playbook-monitoring

Ansible playbook for a simple Prometheus/Grafana setup on Debian-based systems.

All hosts are configured with nginx and Certbot, unless `nginx` and `certbot`
are set to `false`. The Certbot role requires `certbot_email` to be defined.

Please see the individual roles for more information and default values.

External collections/roles:

- [commons](https://codeberg.org/alxndr42/ansible-commons)

## Requirements

- Debian-based system with systemd
- Dependencies installed

```bash
# Install dependencies via Codeberg
ansible-galaxy install -r requirements-codeberg.yml

# Install dependencies via GitHub
ansible-galaxy install -r requirements-github.yml
```

## Monitoring Servers

Hosts in the `monitoring` group are configured with a default [Prometheus][]
and [Grafana][] installation. [Pushgateway][] can be installed by setting
`pushgateway` to `true`. The configuration for each service must be customized
locally.

[grafana]: https://grafana.com/
[prometheus]: https://prometheus.io/
[pushgateway]: https://github.com/prometheus/pushgateway

## Monitoring Targets

Hosts in the `monitoring_targets` group are configured with a Prometheus
[node_exporter][].

[node_exporter]: https://github.com/prometheus/node_exporter

## License

GNU General Public License v3 or later (GPLv3+)
