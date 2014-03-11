## Ansible Role for mongodb on FreeBSD

This role does not assume the sysadmin want to use a specific tool to install mongodb. As such it does not install mongodb or configure any user.

This role provides a bootstrap strategy that can be run after installing mongodb:
  - run mongodb without auth
  - insert necessary users
  - restart mongodb with auth
  - use a state file: if created then boostrap has already been done

```
# The bootstrap strategy can be shutdown
mongodb_use_bootstrap: false

# or forced (see defaults/main.yml)
mongodb_force_bootstrap: true
```
