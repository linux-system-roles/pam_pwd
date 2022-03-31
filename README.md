# pam_pwd
![CI Testing](https://github.com/linux-system-roles/template/workflows/tox/badge.svg)

This role implements a password policy for PAM to meet requirements like
minimum password length, history, complexity, etc.

## Requirements

None.

## Role Variables

A description of all input variables (i.e. variables that are defined in
`defaults/main.yml`) for the role should go here as these form an API of the
role.

```yaml
pam_pwd_minlen: "12" # defines the minimum acceptable size for a password.
pam_pwd_history: "5" # defines the number of previous passwords which cannot \
                       be used.
pam_pwd_dcredit: "-1" # defines minimum credit for having required digits in \
                        password.
pam_pwd_ucredit: "-1" # defines minimum credit for having uppercase characters \
                        in password.
pam_pwd_lcredit: "-1" # defines minimum credit for having lowercase characters \
                        in password.
pam_pwd_ocredit: "-1" # defines minimum credit for having other characters in \
                        password.
pam_pwd_minclass: "4" # defines minium number of required character classes in \
                        new password.
pam_pwd_enforce_root: "enforce_for_root" # (""|"enforce_for_root") defines \
                                           whether or not to enforce password \
                                           complexity for user root.
pam_pwd_policy_name: "password-policy" # RHEL 8 only. Define name of the \
                                         custom authselect profile.
pam_pwd_deny: "5" # Set the number of failed login attempts after which the \
                    account is locked.
pam_pwd_unlock_time: "300" # Time in seconds after which an account is unlocked\
                             again.
```

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  roles:
    - pam_pwd
```

More examples can be provided in the [`examples/`](examples) directory. These
can be useful especially for documentation.

## License

MIT.

## Author Information

Author: Joerg Kastning  
Contact: joerg.kastning@uni-bielefeld.de
