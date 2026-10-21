# homelab

A personal infrastructure lab used to practise and document network, systems and security work. Everything here is either built and verified, or clearly marked as planned.

## Status

| Area | Status | Doc |
|---|---|---|
| Proxmox virtualisation | Built | [docs/virtualisation.md](docs/virtualisation.md) |
| Windows Server 2022 domain controller | Built | [docs/active-directory.md](docs/active-directory.md) |
| Active Directory hardening baseline | In progress | [docs/ad-hardening.md](docs/ad-hardening.md) |
| Storage (TrueNAS SCALE, ZFS) | Built | [docs/storage.md](docs/storage.md) |
| Monitoring (Zabbix, Prometheus, Grafana, Wazuh) | Built | [docs/monitoring.md](docs/monitoring.md) |
| Physical Cisco lab (2901, 2960, 3550) | Built | [docs/network-lab.md](docs/network-lab.md) |
| Linux (RHEL, Ansible) | Planned | |
| Azure hub and spoke with Terraform | Planned | |

## Architecture

- Two Proxmox nodes running Windows Server 2022, Windows 11 and Ubuntu Server VMs.
- A nested VMware ESXi host for a second hypervisor.
- TrueNAS SCALE with a ZFS mirror pool and NFS shared to the cluster.
- A Windows Server 2022 domain controller providing Active Directory and DNS.
- An Ubuntu monitoring host running Zabbix, Prometheus, Grafana and Wazuh in Docker.
- A physical Cisco rack for routing, switching and ACL practice on real hardware.

Addresses, hostnames and credentials are deliberately left out of this repository.

## Repository layout

    docs/       build notes, verification steps and runbooks
    scripts/    PowerShell and Bash used in the lab
    diagrams/   network and architecture diagrams

## How each doc is written

Every doc follows the same layout so it can be reviewed quickly:

1. Goal
2. What was done
3. How it was verified
4. Rollback
5. Next steps

## Author

Chuchu Anyanwu, Perth WA. [LinkedIn](https://www.linkedin.com/in/chuchuanyanwu)
