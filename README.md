# Ansible Role: DNS Express

DNS Express is an engine that provides the ability for the BIG-IP system to act as a high-speed,
authoritative DNS server.

With DNS Express configured, the BIG-IP system can answer DNS queries for a DNS zone and respond to
zone transfer requests from specified DNS nameservers (clients). Additionally, zone transfer
communications can be secured with TSIG keys.

## Requirements

* A BIG-IP which has been onboarded/bootstrapped and is ready to receive configuration
* GTM/DNS provisioned on the BIG-IP
* (optional) A TSIG key data from the authoritative DNS server that hosts the zone.
* (optional) A custom DNS profile created if you do not want to use the default ``dns`` profile.

## Role Variables

Available variables are listed below. For their default values, see `defaults/main.yml`:

    provider_server: localhost
    provider_server_port: 443
    provider_user: admin
    provider_password: secret
    provider_validate_certs: no
    provider_transport: rest
    provider_timeout: 120

## Dependencies

None.

## License

Apache

## Author Information

This role was created in 2018 by [Tim Rupp](https://github.com/caphrim007).
