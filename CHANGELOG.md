# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

## 1.3.0 (to be released)
### Added
- Support for `ngx_http_api_module`.
- New configuration options:
    - `connection_timeout`: timeout (in seconds) for the connection from the integration to Nginx
    - `status_module` (default: `discover`). Accepted values:
        * `ngx_http_stub_status_module`
        * `ngx_http_status_module`
        * `ngx_http_api_module`
        * `discover` to automatically choose between `ngx_http_stub_status_module` or `ngx_http_status_module`.
    - `endpoints`: if `status_module` is `ngx_http_api_module`, comma separated list, NON PARAMETERIZED, Endpoints   

## 1.2.0 (2019-04-29)
### Added
- Upgraded to SDK v3.1.5. This version implements [the aget/integrations
  protocol v3](https://github.com/newrelic/infra-integrations-sdk/blob/cb45adacda1cd5ff01544a9d2dad3b0fedf13bf1/docs/protocol-v3.md),
  which enables [name local address replacement](https://github.com/newrelic/infra-integrations-sdk/blob/cb45adacda1cd5ff01544a9d2dad3b0fedf13bf1/docs/protocol-v3.md#name-local-address-replacement).
  and could change your entity names and alarms. For more information, refer
  to:

  - https://docs.newrelic.com/docs/integrations/integrations-sdk/file-specifications/integration-executable-file-specifications#h2-loopback-address-replacement-on-entity-names
  - https://docs.newrelic.com/docs/remote-monitoring-host-integration://docs.newrelic.com/docs/remote-monitoring-host-integrations

## 1.1.0 (2019-04-08)
### Added
- Upgraded to SDKv3
- Remote monitoring option. It enables monitoring multiple NGINX instances,
  more information can be found at the [official documentation page](https://docs.newrelic.com/docs/remote-monitoring-host-integrations).

## 1.0.2 (2018-11-05)
### Fixed
- Issue where if 'config_path' provided is a directory the integration generates high CPU load.
- Issue where if nginx status page response code was different than 200

## 1.0.1 (2018-09-07)
### Changed
- Update Makefile

## 1.0.0 (2018-08-02)
### Added
- Initial release, which contains inventory and metrics data
