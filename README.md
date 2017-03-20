# Ansible Role: Dropbox

Install Dropbox <https://www.dropbox.com/> from Dropbox repository.

## Requirements

- Ansible >= 2.2
- Fedora 25
- sudo
- Nemo (Cinnamon) file manager

The role may run on other systems, but it is not tested.

## Role Variables

Keep Dropbox update (present | latest | absent).

```
dropbox_update: latest
```

Add action "Share with Dropbox" to Nemo (right-click copy to clipboard shared URL) (true | false).

```
dropbox_add_action: false
```

Nemo action template.

```
dropbox_action_template: templates/dropbox.nemo_action.j2
```

User list that will deploy the Nemo action "Share with Dropbox". The default will get the ansible user.

```
dropbox_users:
  - {
      name: "{{ ansible_user_id }}",
      home: "{{ ansible_user_dir }}",
    }
```

## Example

```
- hosts: all
  roles:
    - ansible-role-dropbox
```

## Dependencies

None

## License

MIT

## Author Information

Apostolos Tovletoglou [ansible-role-dropbox](https://github.com/tovletoglou/ansible-role-dropbox)
