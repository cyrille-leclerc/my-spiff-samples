
## Context

```
spiff -v
spiff version 1.0.3
```

## Multiline YML attribute

See https://github.com/cloudfoundry/cf-release/blob/ee8d52f5dc2a525b6b376c1b4928eddbd9daa1f0/bosh-lite/cf-stub-spiff.yml

YML fragment

```yml
...
    certificates:
      - |
          -----BEGIN CERTIFICATE-----
          MIIDETCCAfmgAwIBAgIJANZuykf1uh3LMA0GCSqGSIb3DQEBBQUAMB8xHTAbBgNV
          BAMMFCouMTAuMjQ0LjAuMzQueGlwLmlvMB4XDTE0MTIyNDIzMTkxM1oXDTI0MTIy
          MTIzMTkxM1owHzEdMBsGA1UEAwwUKi4xMC4yNDQuMC4zNC54aXAuaW8wggEiMA0G
          CSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDCjq73Fgwfj2UT0/+wR9kVVsGAguMj
          poA0opLCgE0yHStAhSvqq7YpO39dH3vBMWXyr2xIfDyaeZyhV86jWu/ZKswGjNGI
          ZKv/yUINe1bqukOBqd+SHVvkVhxSLJuD1MR83JQMONRjOPJp661/ABpVhnrNfBiA
          AA6aaFv4/KbyGY/E1FHoUXqEdh4WxaJdfX6SbgG05ArWxhSD7PNj4CYvJWGCdvqP
          KBsvWFDrkxBHn5h1JIDfZJB8FKP6vaHBr7MU4pIHM+qaZ1Y+8ja0wcgkHn4YHcp6
          IOhqpck7LaH5Qq2ydYFNTcG4fTbG0jXqcit2WSUxRkXzWnrgo2E0SiHBAgMBAAGj
          UDBOMB0GA1UdDgQWBBSpCtEDtEvMwaZzXN6Lvk5U7Eyn2zAfBgNVHSMEGDAWgBSp
          CtEDtEvMwaZzXN6Lvk5U7Eyn2zAMBgNVHRMEBTADAQH/MA0GCSqGSIb3DQEBBQUA
          A4IBAQB1YIHmw3gPiMn8WDR4yVxDvSVgFHY6ZE1iZb17vVs4N2/mhQZXWJ2nZV02
          goAivtgxHOj39sK5OBWsGvrQo5H8dt1t4XmbwB1C6xRerGc25dhDRq42RqhCN0RJ
          zzjd9b8YSiwtAaZlW36l2jVDLfRapb00tWToF9qYrDrmKy2sekS7g2hbiRStcue/
          bpT4X/CHxb/lUbpL4m8BpDbkGiOJgl+SEHRx5tZ0Kob/RDQRCcN3p+71FRbDIEBj
          +8sJl/yUUUPwQ6PNYx6cjtlICWJ1G0l0hRa141VXPqSNCmxYS4dp/8ifPCSoLc+k
          9TXFkuGl+86CPTyyMJxyMhEcAGZT
          -----END CERTIFICATE-----

```

## 'Identity' transformation


template.yml

```yml
properties: (( merge ))
```

command line

```
spiff merge template.yml cf-stub-diff.yml 
```

## Output

```
properties:
  ca_truster:
    certificates:
    - '-----BEGIN CERTIFICATE-----

      MIIDETCCAfmgAwIBAgIJANZuykf1uh3LMA0GCSqGSIb3DQEBBQUAMB8xHTAbBgNV

      BAMMFCouMTAuMjQ0LjAuMzQueGlwLmlvMB4XDTE0MTIyNDIzMTkxM1oXDTI0MTIy

      MTIzMTkxM1owHzEdMBsGA1UEAwwUKi4xMC4yNDQuMC4zNC54aXAuaW8wggEiMA0G

      CSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDCjq73Fgwfj2UT0/+wR9kVVsGAguMj

      poA0opLCgE0yHStAhSvqq7YpO39dH3vBMWXyr2xIfDyaeZyhV86jWu/ZKswGjNGI

      ZKv/yUINe1bqukOBqd+SHVvkVhxSLJuD1MR83JQMONRjOPJp661/ABpVhnrNfBiA

      AA6aaFv4/KbyGY/E1FHoUXqEdh4WxaJdfX6SbgG05ArWxhSD7PNj4CYvJWGCdvqP

      KBsvWFDrkxBHn5h1JIDfZJB8FKP6vaHBr7MU4pIHM+qaZ1Y+8ja0wcgkHn4YHcp6

      IOhqpck7LaH5Qq2ydYFNTcG4fTbG0jXqcit2WSUxRkXzWnrgo2E0SiHBAgMBAAGj

      UDBOMB0GA1UdDgQWBBSpCtEDtEvMwaZzXN6Lvk5U7Eyn2zAfBgNVHSMEGDAWgBSp

      CtEDtEvMwaZzXN6Lvk5U7Eyn2zAMBgNVHRMEBTADAQH/MA0GCSqGSIb3DQEBBQUA

      A4IBAQB1YIHmw3gPiMn8WDR4yVxDvSVgFHY6ZE1iZb17vVs4N2/mhQZXWJ2nZV02

      goAivtgxHOj39sK5OBWsGvrQo5H8dt1t4XmbwB1C6xRerGc25dhDRq42RqhCN0RJ

      zzjd9b8YSiwtAaZlW36l2jVDLfRapb00tWToF9qYrDrmKy2sekS7g2hbiRStcue/

      bpT4X/CHxb/lUbpL4m8BpDbkGiOJgl+SEHRx5tZ0Kob/RDQRCcN3p+71FRbDIEBj

      +8sJl/yUUUPwQ6PNYx6cjtlICWJ1G0l0hRa141VXPqSNCmxYS4dp/8ifPCSoLc+k

      9TXFkuGl+86CPTyyMJxyMhEcAGZT

      -----END CERTIFICATE-----

'
  cc:
    default_running_security_groups:
    - public_networks
    - dns
    - services
    - load_balancer
    min_cli_version: 6.0.0
    min_recommended_cli_version: 6.10.0
    security_group_definitions:
    - name: public_networks
      rules:
      - destination: 0.0.0.0-9.255.255.255
        protocol: all
      - destination: 11.0.0.0-169.253.255.255
        protocol: all
      - destination: 169.255.0.0-172.15.255.255
        protocol: all
      - destination: 172.32.0.0-192.167.255.255
        protocol: all
      - destination: 192.169.0.0-255.255.255.255
        protocol: all
    - name: dns
      rules:
      - destination: 0.0.0.0/0
        ports: "53"
        protocol: tcp
      - destination: 0.0.0.0/0
        ports: "53"
        protocol: udp
    - name: services
      rules:
      - destination: 10.244.1.0/24
        protocol: all
      - destination: 10.244.3.0/24
        protocol: all
    - name: load_balancer
      rules:
      - destination: 10.244.0.34
        protocol: all
  loggregator_endpoint:
    shared_secret: PLACEHOLDER-LOGGREGATOR-SECRET
``