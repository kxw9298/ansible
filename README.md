Pull docker image
```
docker pull vincesestodocker/try-ansible:latest
```
Tag image with shorter name
```
docker tag vincesestodocker/try-ansible:latest ansible-utils
```

Run docker and map your local folder to /ansible in docker container
```
docker run -d -it --name ansible -v /path/to/your/ansible/playbook:/ansible ansible-utils
```
Sh into docker container to run ansible jobs
```
docker exec -it ansible sh
```
Run ansible playbook
```
cd ansible
ansible-playbook -i inventory/example1.yaml ansible/example1.yaml
```