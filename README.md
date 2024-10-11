# README

```yaml
sinks:
  # 命令注入
  - { method: "<java.lang.Runtime: java.lang.Process exec(java.lang.String)>", index: 0 }
  - { method: "<java.lang.Runtime: java.lang.Process exec(java.lang.String[])>", index: 0 }
  - { method: "<java.lang.ProcessBuilder: java.lang.Process start()>", index: base }
  - { method: "<java.lang.ProcessImpl: java.lang.Process start()>", index: base }
  - { method: "<java.lang.UNIXProcess: java.lang.Process start()>", index: base }
```
`method`为函数签名，`index`表示关键参数的位置，`0`表示如果第一个参数用户可控则存在风险，`base`表示如果基变量用户可控则存在风险。