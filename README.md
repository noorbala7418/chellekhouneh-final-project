# Chellekhouneh Final Project

- Create HA kubernetes cluster
- Create Monitoring Stack
- Setup Kafka single node
- Setup longhorn storage
- Setup Bastion Host

# How to run?

0. Create venv and enable it

```bash
python3 -m pip install --user --upgrade virtualenv
python3 -m virtualenv venv
source venv/bin/activate
```

1. Install `requirements.txt` modules

```bash
pip install -r requirements.txt
```

2. Add your host into `inventory/hosts-forward.yml` and `inventory/hosts-pub.yml`

3. Add your Secrets into `inventory/group_vars/all/vault.yml` (Password: `noorbala7418`)

```bash
ansible-vault decrypt inventory/group_vars/all/vault.yml

# After Edits -> Encrypt it

ansible-vault encrypt inventory/group_vars/all/vault.yml
```

4. Enable SSH-Agent

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa  # change address with your ssh-private-key address.
```
5. Step 1: Copy `ansible.cfg.example` to `ansible.cfg`

```bash
cp ansible.cfg.example ansible.cfg
```

5. Step 2: Add your SSH private-key address into `ansible.cfg`

```ini
private_key_file = /home/ubuntu/.ssh/id_rsa # change address with your ssh-private-key address.
```

6. Run `common.yml` playbook:

```yml
ansible-playbook -i inventory/hosts-pub.yml common.yml --ask-vault-pass
```

7. Run `deployer.yml` playbook:

```yml
ansible-playbook -i inventory/hosts-pub.yml deployer.yml --ask-vault-pass
```

8. Done :)