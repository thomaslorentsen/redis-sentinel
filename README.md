# Redis Sentinel Test Environment
Provides a test enviroment for redis sentinel and redis
# Usage
Start vagrant boxes
```bash
vagrant up
```
Build redis sentinel with ansible
```
ansible-playbook \
  -i inventories/hosts.ini \
  playbook.yml
```
# References
- [Redis Sentinel](https://redis.io/topics/sentinel)
- [How to build a fault-tolerant redis cluster with sentinel](https://seanmcgary.com/posts/how-to-build-a-fault-tolerant-redis-cluster-with-sentinel)
