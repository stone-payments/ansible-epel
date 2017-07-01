# EPEL Repository

Installs the [EPEL repository](https://fedoraproject.org/wiki/EPEL) (Extra Packages for Enterprise Linux) for RHEL/CentOS.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yml
epel_repo_file: "/etc/yum.repos.d/epel.repo"
epel_repo_url: "https://dl.fedoraproject.org/pub/epel/epel-release-latest-{{ ansible_distribution_major_version }}.noarch.rpm"
epel_gpg_url: "/etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-{{ ansible_distribution_major_version }}"
```

## Dependencies

None.

## Example Playbook

    - hosts: servers
      roles:
        - stone-payments.epel

## License

MIT
