# Redis Tuning

## Recommendations

### /etc/sysctl.conf Tweaks

from [https://redis.io/docs/management/admin/](https://redis.io/docs/management/admin/)

`vm.overcommit_memory = 1`

from&#x20;

```bash
vm.swappiness = 1
```



### Disable Transparent Huge Pages

from [https://redis.io/docs/management/admin/](https://redis.io/docs/management/admin/)

`echo never > /sys/kernel/mm/transparent_hugepage/enabled`

More: [https://www.mongodb.com/docs/manual/tutorial/transparent-huge-pages/](https://www.mongodb.com/docs/manual/tutorial/transparent-huge-pages/)

### /etc/redis/redis.conf Tweaks

from x

`tcp-keepalive 0`

``
