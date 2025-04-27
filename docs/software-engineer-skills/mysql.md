# Mysql

排序规则: utf8mb4_general_ci

Int型数据范围:

```
tinyint: (2^8)^1
smallint: (2^8)^2
int: (2^8)^4
bigint: (2^8)^8
```

```sql
create schema db collate utf8mb4_general_ci;

```



```sql
select DATE_FORMAT(CONVERT_TZ(FROM_UNIXTIME(T_ICR.created_at / 1000), 'UTC', 'Europe/Berlin'),
                   '%Y-%m-%d') AS german_date,
       T_ICR.op_id,
       T_SU.username,
       T_SU.name,
       count(*)                as cnt
from yt_inventory_check_record T_ICR
         left join yt_sys_user T_SU on T_ICR.op_id = T_SU.user_id
group by german_date, T_ICR.op_id, T_SU.username, T_SU.name
order by german_date desc



select DATE_FORMAT(CONVERT_TZ(FROM_UNIXTIME(T_ICR.created_at / 1000), 'UTC', 'Europe/Berlin'),
                   '%Y-%m-%d %H:%i:%s') AS german_date,
       T_ICR.op_id,
       T_SU.username,
       T_SU.name,
       count(*)                as cnt
from yt_inventory_check_record T_ICR
         left join yt_sys_user T_SU on T_ICR.op_id = T_SU.user_id
group by german_date, T_ICR.op_id, T_SU.username, T_SU.name
order by german_date desc





CREATE TABLE `t_user` (
    `id` bigint unsigned NOT NULL AUTO_INCREMENT COMMENT '自增主键ID',
    `user_id` bigint unsigned NOT NULL COMMENT '用户ID',
    `nickname` varchar(64) NOT NULL COMMENT '用户昵称',
    `email` varchar(128) NOT NULL COMMENT '邮箱',
    `password` varchar(32) NOT NULL COMMENT 'MD5密码',
    `create_timestamp` bigint unsigned NOT NULL COMMENT '创建时间',
    `update_timestamp` bigint unsigned NOT NULL COMMENT '更新时间',
    PRIMARY KEY (`id`)
) ENGINE = InnoDB AUTO_INCREMENT = 2 DEFAULT CHARSET = utf8mb4 COLLATE = utf8mb4_0900_ai_ci COMMENT = '用户表'
```

