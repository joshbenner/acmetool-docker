# acmetool-docker

Docker container to auto-acquire and renew SSL certs with LetsEncrypt.

Uses [acmetool](https://github.com/hlandau/acme) for LetsEncrypt interactions.

[![Docker Repository on Quay](https://quay.io/repository/joshbenner/acmetool/status "Docker Repository on Quay")](https://quay.io/repository/joshbenner/acmetool)

## Configuration

Configuration is performed with Docker environment variables.

| Variable | Default | Description |
| -------- | ------- | ----------- |
| `ACME_EMAIL` | changeme@example.com | Email used to register with LetsEncrypt |
| `ACME_SERVER` | https://acme-staging.api.letsencrypt.org/directory | ACME API URL, defaults to staging API. |
| `CERT_DOMAINS` | example.com www.example.com | Space-delimited list of domains to get certificates for |
| `HAPROXY_ALWAYS_GENERATE` | yes | If set, generates combined cert and private key files that can be used by HAProxy. |
