# demonpig.ersatztv

This role will install [ErsatzTV](https://github.com/ErsatzTV/ErsatzTV) onto a managed host. The application allows for creating an IPTV service using local media files.

### Requirements

Nothing at the moment.

### Role Variables

```yaml
ersatztv_version: latest
```

Specifies the version of the ErsatzTV to install on the managed host. The role pulls the artifacts from https://github.com/ErsatzTV/ErsatzTV/releases.

If the variable is set to `latest` (default), then the role will perform a check against the repository for the latest release.

```yaml
ersatztv_user: root
```

Service account that ErsatzTV will run as on the managed host.

```yaml
ersatztv_install_dir: /opt/ersatztv
```

This is the directory where ErsatzTV will be installed.

```yaml
ersatztv_data_dir: /var/lib/ersatztv
```

This is the directory where ErsatzTV's user-data will be located.

### Dependencies

- Ansible 2.9+

### Example Playbook

```yaml
---

- name: Install ErsatzTV
  hosts: all

  roles:
    - name: demonpig.ersatztv
```

### License

MIT
