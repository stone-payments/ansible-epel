# EPEL Repository

Installs the [EPEL repository](https://fedoraproject.org/wiki/EPEL) (Extra Packages for Enterprise Linux) for RHEL/CentOS.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yml
epel_repo_file: "/etc/yum.repos.d/epel.repo"
epel_repo_url: "https://dl.fedoraproject.org/pub/epel/$releasever/$basearch/"
epel_gpg_file: "/etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-{{ ansible_distribution_major_version }}"
epel_gpg_url: "https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-{{ ansible_distribution_major_version }}"
epel_gpg_check: "yes"

epel_satellite: false #change to true when you want to get EPEL packages from an internal Satellite mirror
epel_satellite_label: "" #when epel_satellite is true:  add repo with subscription-manager
                         #                       false: remove repo with subscription-manager
```

## Dependencies

None.

## Example Playbook

    - hosts: servers
      roles:
        - stone-payments.epel

## License

MIT
