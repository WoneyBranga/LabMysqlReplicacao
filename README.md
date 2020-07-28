# LAB REPLICAÇÃO MYSQL 5.5.20 => MARIA10.3.22

Laboratório para homologação da replicação entre bancos diferentes.

---
Ambiente simulado:
```
SERVER MASTER > mysql5.5.20
SERVER SLAVE  > mariadb10.3.22
```

---

## Reprodução do Lab:
 
 1. `git clone`
 2. `docker-coposer up`
 3. `mysql -hHOST_DOCKER -uUSER -pPASS < DUMP_SQL.sql`

> Note que para compatibilidade foi necessário desativar o checksum no slave!
> ```bash
> slave_sql_verify_checksum=0
> ```

*Repo utilizando como base material http://tarunlalwani.com/post/mysql-master-slave-using-docker*