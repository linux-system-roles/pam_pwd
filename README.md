# pam_pwd
![CI Testing](https://github.com/linux-system-roles/template/workflows/tox/badge.svg)

This role configures PAM to implement a password policy to meet requirements like minimum password length, complexity, keep password history, etc. It supports:

  - Fedora >= 35
  - RHEL 7
  - RHEL 8
  - RHEL 9 Beta
  - CentOS 7
  - CentOS Stream 8
  - CentOS Stream 9

The role was tested with the following versions of Ansible:

  - ansible-core 2.11
  - ansible-core 2.12

To use this role you have to specify the role variables which are described below.

## Requirements

None.

## Role Variables

Here you find a description of all input variables (i.e. variables that are defined in
`defaults/main.yml`) for the role as these form the API of the role. The following code block shows all necessary input variables and their default values. They are specified in `defaults/main.yml`.

```yaml
pam_pwd_minlen: "12" # defines the minimum acceptable size for a password.
pam_pwd_history: "5" # defines the number of previous passwords which cannot be used.
pam_pwd_dcredit: "-1" # defines minimum credit for having required digits in password.
pam_pwd_ucredit: "-1" # defines minimum credit for having uppercase characters in password.
pam_pwd_lcredit: "-1" # defines minimum credit for having lowercase characters in password.
pam_pwd_ocredit: "-1" # defines minimum credit for having other characters in password.
pam_pwd_minclass: "4" # defines minium number of required character classes in new password.
pam_pwd_enforce_root: "enforce_for_root" # (""|"enforce_for_root") defines whether or not to enforce password complexity for user root.
pam_pwd_policy_name: "password-policy" # RHEL 8 only. Define name of the custom authselect profile.
pam_pwd_deny: "5" # Set the number of failed login attempts after which the account is locked.
pam_pwd_unlock_time: "300" # Time in seconds after which an account is unlocked again.
```

You can keep these default values if they fit your requirements. Or you can overwrite the defaults by specifiny some or all of them in places like `vars/main.yml`, `group_vars/`, `host_vars/` or your playbook.

## Dependencies

None.

## Example Playbook

The following code block shows the simplest playbook to run this role:

```yaml
- hosts: all
  roles:
    - pam_pwd
```

More examples can be found in the [`examples/`](examples) directory.

## License

MIT.

## Author Information

Author: Joerg Kastning  
Contact: joerg.kastning@uni-bielefeld.de
