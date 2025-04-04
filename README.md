# Ansible role [bareos_fd](#bareos_fd)

Install and configure [Bareos](https://www.bareos.com/) File Daemon.

|GitHub|GitLab|Downloads|Version|
|------|------|---------|-------|
|[![github](https://github.com/adfinis/ansible-role-bareos_fd/workflows/Ansible%20Molecule/badge.svg)](https://github.com/adfinis/ansible-role-bareos_fd/actions)|[![gitlab](https://gitlab.com/robertdebock-iac/ansible-role-bareos_fd/badges/master/pipeline.svg)](https://gitlab.com/robertdebock-iac/ansible-role-bareos_fd)|[![downloads](https://img.shields.io/ansible/role/d/)](https://galaxy.ansible.com/adfinis/bareos_fd)|[![Version](https://img.shields.io/github/release/adfinis/ansible-role-bareos_fd.svg)](https://github.com/adfinis/ansible-role-bareos_fd/releases/)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/adfinis/ansible-role-bareos_fd/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: true
  gather_facts: true

  roles:
    - role: adfinis.bareos_fd
      bareos_fd_backup_configurations: true
      bareos_fd_install_debug_packages: true
      bareos_fd_encryption_enable: true
      bareos_fd_encryption_private_key: |
        -----BEGIN RSA PRIVATE KEY-----
        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
        -----END RSA PRIVATE KEY-----
      bareos_fd_encryption_master_public_key: |
        -----BEGIN CERTIFICATE-----
        MIIDyjCCArKgAwIBAgIJAIAjOIGqAGRwMA0GCSqGSIb3DQEBCwUAMIGSMQswCQYD
        VQQGEwJOTDEQMA4GA1UECAwHVVRSRUNIVDESMBAGA1UEBwwJQnJldWtlbGVuMSIw
        IAYDVQQKDBlBZGZpbmlzIElUIE5lZGVybGFuZCBCLlYuMQ8wDQYDVQQDDAZiYXJl
        b3MxKDAmBgkqhkiG9w0BCQEWGXJvYmVydC5kZWJvY2tAYWRmaW5pcy5jb20wHhcN
        MjMwOTExMDg1MzA0WhcNMjMxMDExMDg1MzA0WjCBkjELMAkGA1UEBhMCTkwxEDAO
        BgNVBAgMB1VUUkVDSFQxEjAQBgNVBAcMCUJyZXVrZWxlbjEiMCAGA1UECgwZQWRm
        aW5pcyBJVCBOZWRlcmxhbmQgQi5WLjEPMA0GA1UEAwwGYmFyZW9zMSgwJgYJKoZI
        hvcNAQkBFhlyb2JlcnQuZGVib2NrQGFkZmluaXMuY29tMIIBIjANBgkqhkiG9w0B
        AQEFAAOCAQ8AMIIBCgKCAQEAxFjcLKHDTf8dcT4kKtyZlIh4Zh7zNglaa6SJNBGW
        pmcvtgfR9aBCDbcEphcssdytrXIiLsCEfv1h63o58UXePKYJMtNzbn6NNyzamxB9
        CM4oHWr/td8i6fYaYXmqOxOimX707joWPlTB9+/rKWFrxwyg08oVGFdBNR6GmWek
        Y5aRaEMwRBhh+bSVR9/Rj/QmqlF9pCB9/TtY3hhBdQkcy1tLTDo7Mf/Z4gLpk7d2
        vRmpvVY8JloXjzuJNgVNbzY09pylqe78m9UsrJGBlzocZO5+AnO7wsqMAtUvplOM
        oE7GHrg1FpfLjY3bqTQka/fVd1bDt5eDjAJnPqO1RYpKjQIDAQABoyEwHzAdBgNV
        HQ4EFgQURTeY0pPxExJwTelsdBXr5PxgOdAwDQYJKoZIhvcNAQELBQADggEBALCi
        urw+j1Yg2QDkOzMxmr6r0O/kF3WfrfpcevOCGVN0GxdxP/nGcfAh8feq4xj4oAnS
        2CyhNfPPi+rIO1T0EkZWwL/kTByMGoR9Qc+juMgJ1HTYP6nEnBOXPMo1OyUdK5K3
        MefQpNgHdWNSjWtLuW3YW8rkIeF8ZjmlXOSmBdOmqFi7p3OwwF8FnuXze1RLTgPL
        VeI8D8DtzbX+mocuYxfIAFEmRXAmMeimXgwrVyI+w8+3IRGw8rDje0pFZX5X2aED
        Gcz2IVF2cw5k1ryYW5kN027oK9igd8qc6dcJC6nMJw1kLbBdo68Eq3EOx92Fljlg
        Wa7Dw2pD6yQGl/dfgQg=
        -----END CERTIFICATE-----
      bareos_fd_directors:
        - name: "bareos-dir"
          password: "secretpassword"
          monitor: false
          connection_from_client_to_director: true
          connection_from_director_to_client: false
          tls_enable: true
          tls_verify_peer: false
      bareos_fd_messages:
        - name: "Standard"
          director:
            server: bareos-dir
            messages:
              - all
              - "!skipped"
              - "!restored"
          description: "Send relevant messages to the Director."
          append:
            file: "/var/log/bareos/bareos.log"
            messages:
              - all
              - "!skipped"
              - "!terminate"
          console:
            - all
            - "!skipped"
            - "!saved"
        - name: "disabled-message"
          enabled: false
      bareos_fd_plugins:
        - mariabackup
      bareos_fd_rear_enable: true  # enables Relax-and-Recover (ReaR) support
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/adfinis/ansible-role-bareos_fd/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Prepare
  hosts: all
  become: true
  gather_facts: false

  roles:
    - role: robertdebock.bootstrap
    - role: adfinis.bareos_repository
      bareos_repository_enable_tracebacks: true
```

These roles are provided as is, without warranty of any kind. Use it at your own risk.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/adfinis/ansible-role-bareos_fd/blob/master/defaults/main.yml):

```yaml
---
# defaults file for bareos_fd

# The client has these configuration parameters.

# Backup existing configurations.
bareos_fd_backup_configurations: false

# Install debug packages. This requires the debug repositories to be enabled.
bareos_fd_install_debug_packages: false

# The hostname of the File Daemon.
bareos_fd_hostname: "{{ inventory_hostname }}"

# The maximum bandwidth to use.
bareos_fd_max_job_bandwidth: "10 mb/s"

# The message to use.
bareos_fd_message: "Standard"

# The maximum number of concurrent jobs.
bareos_fd_maximum_concurrent_jobs: 20

# Enable TLS.
bareos_fd_tls_enable: true

# Verify the peer.
bareos_fd_tls_verify_peer: false

# The inteval in seconds to send a heartbeat.
bareos_fd_heartbeat_interval: 0

# The Director to connect to. Bareos only supports one Director!
bareos_fd_directors:
  - name: "bareos-dir"
    password: "secretpassword"
    monitor: false
    description: "Allow the configured Director to access this file daemon."

# The Messages to configure.
bareos_fd_messages:
  - name: "Standard"
    director:
      server: bareos-dir
      messages:
        - all
        - "!skipped"
        - "!restored"
    description: "Send relevant messages to the Director."

# For encryption of data, set this to `true`.
bareos_fd_encryption_enable: false

# You may bring your own private key. If falset specified, a new one will be generated.
bareos_fd_encryption_private_key: ""

# The master public key to use.
bareos_fd_encryption_master_public_key: ""


# Enable for Relax-and-Recover (ReaR). Check argument_specs for more related arguments.
bareos_fd_rear_enable: false
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/adfinis/ansible-role-bareos_fd/blob/master/requirements.txt).

## [Context](#context)

This role is a part of the Adfinis Bareos Ansible Collection: https://galaxy.ansible.com/ui/repo/published/adfinis/bareos/docs/

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/robertdebock):

|container|tags|
|---------|----|
|[Debian](https://hub.docker.com/r/robertdebock/debian)|bookworm, bullseye, buster|
|[EL](https://hub.docker.com/r/robertdebock/enterpriselinux)|8, 9|
|[Fedora](https://hub.docker.com/r/robertdebock/fedora/)|40, 41|
|[Ubuntu](https://hub.docker.com/r/robertdebock/ubuntu)|22.04, 24.04|

The minimum version of Ansible required is 2.15, tests have been done to:
- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/adfinis/ansible-role-bareos_fd/issues).

## [License](#license)

[Apache-2.0](https://github.com/adfinis/ansible-role-bareos_fd/blob/master/LICENSE).

## [Author Information](#author-information)

[Adfinis](https://adfinis.com/)

