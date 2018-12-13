# Kubernetes elasticsearch

This project deploys the `ansible-role-elasticsearch` role found here: https://github.com/rombit-be/ansible-role-elasticsearch

## Requirements
You need to checkout the role with the following command:

```bash
ansible-galaxy install -r requirements.yml --roles-path=roles  --force
```


## Install
Now you can install the elasticsearch cluster in a certain Kubernetes-namespace as follows:

* First create a new environment in `environments/`. You can take a look in the current `environments` folder for examples
* Make sure the namespace you define, exists on your Kubernetes cluster
```
kubectl create namespace my-elasticsearch-namespace  # <-- replace with the correct namespace
```

* Run the role with the following command:
```
ansible-playbook create.yml -i environments/<your environment>.yml
```
