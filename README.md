# Test Redis Sentinel
Start vagrant boxes
```bash
vagrant up
```
Build redis sentinel
```
ansible-playbook \
  -i inventories/hosts.ini \
  playbook.yml
```
