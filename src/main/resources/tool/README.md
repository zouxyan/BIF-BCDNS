# 申请参数工具类

1、工具类jar包（BCDNS-tool-1.0-SNAPSHOT-jar-with-dependencies.jar）

2、在jar包目录下用命令行执行 
**申请PTC参数：**

| 参数号 | 说明                                                         |
| ------ | ------------------------------------------------------------ |
| 0      | 值为ptc，指定为申请ptc证书                                   |
| 1      | 申请人私钥，ptc只能由超级节点申请                            |
| 2      | ptc的公钥                                                    |
| 3      | ptc的类型，0为外部验证者模式、1为委员会验证模式、2为中继验证模式 |

```
java -cp BCDNS-tool-1.0-SNAPSHOT-jar-with-dependencies.jar org.example.ApplyTool ptc 申请人的私钥 ptc的公钥 ptc的type
```
**申请relay（中继）参数：**

| 参数号 | 说明                               |
| ------ | ---------------------------------- |
| 0      | 值为relay，指定为申请relay证书     |
| 1      | 申请人私钥，中继只能由超级节点申请 |
| 2      | relay的公钥                        |

```
java -cp BCDNS-tool-1.0-SNAPSHOT-jar-with-dependencies.jar org.example.ApplyTool relay 申请人的私钥 relay的公钥
```

**申请域名参数：**

| 参数号 | 说明                                     |
| ------ | ---------------------------------------- |
| 0      | 值为domainName，指定为申请区块链域名证书 |
| 1      | 申请人私钥，区块链域名只能由中继代为申请 |
| 2      | 区块链的公钥                             |
| 3      | 区块链域名                               |

```
java -cp BCDNS-tool-1.0-SNAPSHOT-jar-with-dependencies.jar org.example.ApplyTool domainName 申请人的私钥 区块链的公钥 申请的区块链域名
```
