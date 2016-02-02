# ansible-role-csgo

Ad-hoc role to configure multiple csgo servers using [LGSM](https://github.com/dgibbs64/linuxgsm). Might work, though it's completely unsupported for now. Most of the variables have defaults and they can be defined per server or globally,

## example usage
### playbook
```YAML
---
- hosts: csgoservers
  sudo: true
  roles:
    - csgo
```

### hostvars
```YAML
---
csgo_gslt_token: "mytoken"
csgo_defaultmap: de_dust2
csgo_maxplayers: 16
csgo_tickrate: 128
csgo_rcon_password: "supersecret"
csgo_servers:
  - name: csgo-server1
    ip: "10.0.0.1"
    hostname: "My awesome CS:GO server #1"
  - name: csgo-server2
    ip: "10.0.0.2"
    hostname: "My awesome CS:GO server #2"
```
