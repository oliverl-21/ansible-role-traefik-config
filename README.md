# Role Name

Ansible Role to generate dynamic configuration for a Bimary Traefik installation. Will also work in a docker setup but needs customization for the default variables

## Requirements

Role expects a folder Structure for the Traefik configuration like the following below

```shell
/etc/traefik # can be defined with var: {{ traefik_conf_path }}
├── conf.d
│   └── dynamic.yaml
├── ssl
│   └── acme.json
└── traefik.yaml
```

## Role Variables

Global Role variables defined in `defaults/main.yml` with default values

```yaml
traefik_conf_path: "/etc/traefik"
traefik_dyn_conf_folder: "conf.d"
traefik_dyn_conf_file: "dynamic.yaml"
```

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

## License

MIT
