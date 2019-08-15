```bash
ssh-keygen -t rsa -b 4096 -C "ansible"
cat ~/.ssh/ansible.pub | pbcopy
```

```bash
pip install ansible
pip install requests google-auth
```

```bash
ansible-inventory -i inventories/webservers.yml --graph
```

```bash
python $(which ansible-inventory)  -i inventories/server_gcp.yml --graph
```

```bash
./env.sh

```

```bash
ansible-playbook -t create playbooks/compute_infra.yml
```