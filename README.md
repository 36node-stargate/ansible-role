# stargate-role

stargate 部署套件

## Requirements

- python3
- ansible2

## Role Variables

- state: 部署状态

## Dependencies

## Example Playbook

```yaml
  - role: 36node.project.stargate
    tags:
      - stargate
    vars:
      state: present
      domain: "stargate.casc.cc"
      account_version: 1.4.0
      admin_version: 1.4.0
      # auth_version: 1.21.0
      auth_version: casc
      auth_path: /auth/v1
      auth_admin_url: "http://{{ admin_path }}.{{ domain }}"
      account_path: account
      account_auth_path: "http://api.{{ domain }}{{ auth_path }}"
      account_url_path: "{{ account_path }}.{{ domain }}"
      admin_path: admin
      admin_auth_path: "http://api.{{ domain }}{{ auth_path }}"
      admin_auth_url: "http://stargate.{{ account_path }}.{{ domain }}/auth"
      admin_auth_login_url: "http://stargate.{{ account_path }}.{{ domain }}/login"
      admin_app_id: 5f86d013e0de9b00116c2e05
```

## Develop guide

Link to local installed role for convenience.

```sh
rm -rf ~/.ansible/roles/36node.project.stargate
ln -s $PWD ~/.ansible/roles/36node.project.stargate
```
