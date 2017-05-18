Setup count of hosts to test
```
head -n 10 hosts100 > hosts
```

Run playbook
```
ansible-playbook -i hosts test.yml --check
```
