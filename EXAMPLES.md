# Examples

## Creating user(s)
In this example we want to create an user named `ansible`
```
users:
  - name: "ansible"
    home: "/var/lib/ansible"
    uid: 420
    group: "wheel"
    comment: "Ansible Deployment User"
    system: "yes"
    shell: "/bin/bash"
#  - name: "USER_NAME"
#    uid: UNIQUE_UID
#    group: "wheel" # become group
#    groups: [] # optional
#    comment: "FULL_NAME"
#    non_unique: yes
#    system: no
#    createhome: yes
```

## Remove user(s)
```
users_absent:
  - name: backup
    uid: 421
    group: "backup"
```

## Add SSH key(s) for user(s)
```
users_ssh:
  - name: ansible
    key: "{{ lookup('file', 'user-ssh-keys/ansible.pub') }}"
  - name: exampleusertwo
    key: "{{ lookup('file', 'user-keys/exampleusertwo.pub') }}"
```

## Remove SSH key(s) for user(s)
```
users_absent_ssh:
  - name: backup
```

## Add users or groups to sudoers file
```
users_sudo:
  - name: "%wheel"
    mode: "ALL"
  - name: ansible
    mode: "NOPASSWD:ALL"
```

## Create group(s)
```
users_groups:
  - name: wheel
    gid: 425
    system: yes
#  - name: testgroup
#    gid: 1111
#    system: no
```

## Remove group(s)
```
users_absent_groups:
  - name: backup
    gid: 426
    system: yes
```
