# dsh-market

[DSH](https://github.com/deepseek-ai)（DeepSeek Harness）插件市场索引 —— **format 1**，收录 [@kongbaige11111](https://github.com/kongbaige11111) 发布的 bundle。

**索引地址**

```text
https://kongbaige11111.github.io/dsh-market/index.json
```

DSH 不带官方市场：所谓「市场」就是这个 JSON 文件，放在任意 https 地址上即可。插件页的 **Discover** 标签页会读取你添加的索引源。

## 怎么用

1. 打开 DSH Web 侧栏的 **插件（Plugins）**。
2. 点 **实验性插件（Experimental plugins）** 旁的 **更多**，打开 **自定义插件市场（Custom plugin markets）**，页面就会出现 **已安装 / Discover** 两个标签。
3. 在 **Discover** 里添加上面的索引地址。
4. 点安装。DSH 会把插件的精确 commit 钉住装进当前 profile。

> Host 会缓存一次成功的读取 10 分钟，且不接受重定向，所以新版本要么等缓存过期，要么重新读一次索引。

## 收录的插件

| 插件 | 说明 |
|---|---|
| [`dsh-pet-plus`](https://github.com/kongbaige11111/dsh-pet-plus) | 桌宠增强：QQ（NapCat/OneBot 11）互通、好感度养成与喂食、喝水/久坐/番茄钟提醒、右键菜单与提示音。 |

## 新增一个插件

1. 在插件仓库里改 `version`，提交、推送。
2. 回来跑 `node ../dsh-market-publish/publish.mjs --token <PAT>`，它会重新钉住 commit 并刷新本文件的 `index.json`。

## License

MIT
