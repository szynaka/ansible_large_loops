Setup count of hosts to test
```
head -n 10 hosts100 > hosts
```

Run playbook
```
ansible-playbook -i hosts test.yml --check
```

Add localhost address ssh host keys
```
for i in $(seq 1 100); do ssh-keyscan 127.0.0.$i >> ~/.ssh/known_hosts; done
```
