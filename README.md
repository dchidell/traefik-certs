
# Traefik Certs

Minimal service to extract SSL certificates from traefik and create certificate files for use elsewhere.

Modified by David Chidell to conform to traefik v2.0 certificate files & customise filename.

## Quick Start

See the (examples) directory for example docker compose demonstrating config.

## Configuration

The environment variables are:

|Environment Variable|Default|Description|
|--------------------|-------|-----------|
|CERT_PATH|`/certs`|Path to directory where certs will be placed|
|ACME_PATH|`/acme`|Path to acme.json created by traefik|
|ACME_FILE|`acme.json`|Filename (usually acme.json) created by traefik|

## Output

The program with watch acme.json for changes and generate certficates and certfiacte chains with the names `domain.crt` and `domain.chain.crt` repsectively.

## Copyright

2018 Thom Seddon

## License

[MIT](https://github.com/thomseddon/traefik-certs/blob/master/LICENSE.md)
