# Redis Tuning

## Recommendations

### /etc/sysctl.conf Tweaks

from [https://redis.io/docs/management/admin/](https://redis.io/docs/management/admin/) and others

`vm.overcommit_memory = 1`

`vm.swappiness = 1`

`net.core.somaxconn = 65365`

### Disable Transparent Huge Pages

from [https://redis.io/docs/management/admin/](https://redis.io/docs/management/admin/)

`echo never > /sys/kernel/mm/transparent_hugepage/enabled`

More: [https://www.mongodb.com/docs/manual/tutorial/transparent-huge-pages/](https://www.mongodb.com/docs/manual/tutorial/transparent-huge-pages/)

### /etc/redis/redis.conf Tweaks

from [https://redis.io/docs/management/admin/](https://redis.io/docs/management/admin/)

`maxmemory 3gb`\


from&#x20;

`timeout 300`\
`tcp-keepalive 0`\
`tcp-backlog 65536`



from [https://www.digitalocean.com/community/tutorials/how-to-install-and-secure-redis-on-ubuntu-22-04](https://www.digitalocean.com/community/tutorials/how-to-install-and-secure-redis-on-ubuntu-22-04)

```
rename-command FLUSHDB ""
rename-command FLUSHALL ""
rename-command DEBUG ""
```
