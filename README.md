# ansible_ubuntu
Ansible for WSL Ubuntu

## Description
WSL UbuntuにAnsibleでgithubの設定などを行えるようにしたPlaybook

### Versions
- ansible 2.4.1.0

### Roles
- prepare（bash、vimのビープ音の制御など）
- anyenv
- node v8.9.3（ndenv）
- ruby 2.4.1（rbenv）
- git
- github（ssh keyの登録）

## Install
```
$ git clone https://github.com/morio-pg/ansible_ubuntu.git
```

## Settings
```
$ cp vars/settings.yml.example vars/settings.yml
$ vi vars/settings.yml
```

### Create 'access_token'

[New personal access token](https://github.com/settings/tokens/new)にて`admin:public_key`にチェックを入れて作成する

## Usage
```
$ ansible-playbook -i localhost, -c local playbook.yml -K
```
