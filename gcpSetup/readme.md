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
ansible-playbook -t create playbooks/jenkins_infra.yml
```

```bash
ansible-playbook -t delete playbooks/jenkins_infra.yml
```



Install sudo pip install requests google-auth
```bash
ansible-playbook   -i inventories webservers playbooks/jenkins.yml
```

Pass different value to default, for example create an instance named  jmeter-demo-app 
```bash
ansible-playbook -e instance_name=jmeter-demo-app playbooks/demo-app.yml
```

Run demo app playbook using gcp inventory
```bash
ansible-playbook   -i inventories playbooks/demo-app.yml

```