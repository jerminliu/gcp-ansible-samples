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
python $(which ansible-inventory)  -i inventories/server.gcp.yml --graph
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


###Setting up kubernetes nodes using ansible commands
```bash
ansible-playbook -t create -e instance_name=kube-master playbooks/kubernetes_infra.yml
ansible-playbook -t create -e instance_name=kube-node1 playbooks/kubernetes_infra.yml
ansible-playbook -t create -e instance_name=kube-node2 playbooks/kubernetes_infra.yml
```
#####Setup initial things on instances and download dependencies needed for kubernetes
```bash
ansible-playbook -i inventories playbooks/kubernetes-initial.yml 
ansible-playbook -i inventories playbooks/kubernetes-dependencies.yml 
```
#####Using gce dynamic inventory setup the master for kubernetes with cluster

```bash
ansible-playbook -i inventories playbooks/kubernetes-master.yml 

```
#####Using gce dynamic inventory node and make the node join the master using the token

```bash
ansible-playbook -i inventories playbooks/kubernetes-nodes.yml
```
