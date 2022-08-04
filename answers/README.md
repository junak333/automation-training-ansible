# AVD DLH


<details><summary>click here to give up and reveal the answer for Lab 2</summary>
<p>

1. Update the `Tenant_A_WEB_Zone` section in `ATD_TENANTS_NETWORKS.yml`

```
          124:
            name: Tenant_A_WEBZone_4
            tags: [ web ]
            enabled: true
            ip_address_virtual: 10.12.24.1/24
```
2. Create  vlan 124 and SVI 124 on host1 and host2 by updating the host1-day3.cfg and host2-day3.cfg
files

</p>
</details>

<details><summary>click here to give up and reveal the answer for Lab 3</summary>
<p>

Update the `ATD_FABRIC.yml` with the following:

```
aaa_authentication:
  login:
    default: group atds local
aaa_authorization:
  exec:
    default: group atds local
  commands:
    all_default: local

radius_servers:
  - host: 192.168.0.1
    vrf: default
    key: <replace it with the type7 key from the running-config>

aaa_server_groups:
  - name: atds
    type: radius
    servers:
      - server: 192.168.0.1
        vrf: default
```
</p>
</details>