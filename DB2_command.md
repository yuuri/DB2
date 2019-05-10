#### DB2 数据库简单命令

```
su db2inst1           （切换到db2inst1用户）
```

![1557454117006.png](https://i.loli.net/2019/05/10/5cd4e4777d8d4.png)



```
. ~/sqllib/db2profile （调入该用户配置脚本，设置db2inst1实例为当前实例
```

```
db2start              （启动当前实例）
```

![1557454367234.png](https://i.loli.net/2019/05/10/5cd4e4777f703.png)



如果我们希望一个实例在每次系统启动后自动启动，可以使用以下命令：

```
db2iauto -on <实例名>
```

如:希望实例db2inst1自动启动，命令为:

```
db2iauto -on db2inst1
```

如果希望关闭实例的自动启动，则可使用以下命令：

```
db2iauto -off <实例名>
```

```
db2iauto -off db2inst1
```





创建样本数据库

DB2 安装完成后默认是不会创建Sample数据库的，创建Sample数据库的命令为：

```
db2sampl
```

![1557454793649.png](https://i.loli.net/2019/05/10/5cd4e4778c1ce.png)

注意：创建Sample数据库前请确认当前实例名，避免将数据库创建到别的实例上，显示所有数据库实例的命令是

```
db2ilist
```

显示当前数据库实例的命令是

```
db2 get instance
```

![1557454570034.png](https://i.loli.net/2019/05/10/5cd4e47781b56.png)



如果需要将数据库创建到别的实例上，则参考前面实例启动/切换的内容先就行实例切换。





操作命令

1.查看当前所有的数据库

```
db2 list db directory  
```

![1557456816068.png](https://i.loli.net/2019/05/10/5cd4ebd1324a4.png)

2.连接到指定数据库

```
db2 connect  to (数据库名)
db2 connect to sample
```

![1557456914003.png](https://i.loli.net/2019/05/10/5cd4ebd13c26b.png)

3.查看当前所有的连接

```
db2 list application
```

![1557456990741.png](https://i.loli.net/2019/05/10/5cd4ebd13b6d1.png)

4.查看数据库中的表

```
db2 list tables for all
db2 list tables (查看所有非系统表)
```

![1557457172679.png](https://i.loli.net/2019/05/10/5cd4ebd1465c3.png)

5.查看表结构

```
db2 description table (表名)
```

![1557457357195.png](https://i.loli.net/2019/05/10/5cd4ebd128a0e.png)



