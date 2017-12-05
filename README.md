# rhel_set_hostname

## Description:

Set RHEL Hostname on a system in a proper way

_Note: Still work in progress_

## Behaviour:

**Feature:** Set hostname on a system
- **Given** a VM of capable size and power is available
- **Given** the connection details to the VM are known
- **When** A new RHEL-system has been installed
- **Then** set the hostname
- **Then** regenerate initramfs
- **Then** reboot
- **Then** add to hosts-file

## Configuration:

Common variables used by this role:

| Variable  | Description  | Example  | 
|---|---|---|
| **hostname** | System hostname | hostname=mysuper.host.name |

## Usage:

How to invoke the role from a playbook:

```yaml
- name: Set hostname
  include_role:
    name: rhel_set_hostname
  vars:
    hostname: mysuper.host.name
```

Note: add common variables to the `vars` list as required.
