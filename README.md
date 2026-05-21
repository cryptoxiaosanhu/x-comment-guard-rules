# X Comment Guard Rules

这是 X Comment Guard 的远程特征库。

插件会读取这个仓库里的 `rules.json`，用于远程更新垃圾评论、冒充博主、币圈水军等识别规则。

## 文件

- `rules.json`：远程特征库主文件
- `README.md`：说明文档

## rules.json 格式

```json
{
  "version": "2026-05-21-001",
  "spamKeywords": [],
  "impersonationBait": [],
  "cryptoShill": [],
  "genericSpamTemplates": [],
  "contacts": []
}
```

## 更新方式

每次你发现新的垃圾评论话术，就编辑 `rules.json`。

建议每次更新时修改版本号：

```json
"version": "2026-05-21-002"
```

## GitHub Raw 地址格式

如果你的 GitHub 用户名是：

```text
yourname
```

仓库名是：

```text
x-comment-guard-rules
```

那么远程规则地址就是：

```text
https://raw.githubusercontent.com/yourname/x-comment-guard-rules/main/rules.json
```

把这个地址填到插件的“远程特征库更新”里即可。

## 注意

这里不要放 JavaScript 代码，只放关键词和规则数据。
这样更安全，也更容易通过 Chrome 扩展审核。
