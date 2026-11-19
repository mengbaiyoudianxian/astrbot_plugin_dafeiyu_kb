# 大肥鱼知识库

> `astrbot_plugin_dafeiyu_kb` · v0.1.0 · [大肥鱼](https://github.com/mengbaiyoudianxian/dafeiyu) 的自写插件之一

把她待的群里的聊天、她刷到的贴吧/推特/B站全部存下来，定期整理成梗、话题、事件、群友印象；聊天时自动想起相关的；群友发的表情包看过、赋予意义后收进自己的表情包

## 安装

AstrBot（4.x）后台 → 插件 → 右上角「+」→ 从链接安装，填：

```
https://github.com/mengbaiyoudianxian/astrbot_plugin_dafeiyu_kb
```

装完在插件列表里点开它的配置，按需改。平台目前只适配 aiocqhttp（NapCat / OneBot v11）。

## 怎么用

不用指令。她自己会用 recall_memory 回忆、send_collected_meme 发收来的表情包；群友说「别记我」她会用 forget_me

## 搭配

这个插件会读写下面这些大肥鱼插件的数据，单独装也能跑，但相关功能会少一块：

- [`astrbot_plugin_dafeiyu_tieba`](https://github.com/mengbaiyoudianxian/astrbot_plugin_dafeiyu_tieba)
- [`astrbot_plugin_dafeiyu_x`](https://github.com/mengbaiyoudianxian/astrbot_plugin_dafeiyu_x)

## 配置项

| 键 | 说明 | 提示 |
|---|---|---|
| `platform_id` | QQ 平台名 |  |
| `owner_qq` | 主人 QQ |  |
| `llm_provider_id` | 整理记忆用的模型 |  |
| `vision_provider_id` | 看表情包用的模型 |  |
| `digest_min_new` | 一个群攒够多少条新消息就整理一次 |  |
| `digest_chunk` | 每次整理最多看多少条 |  |
| `backfill_pages` | 第一次启动往回拉多少页群历史（每页 100 条） |  |
| `collect_memes` | 收群友的表情包 |  |
| `inject_items` | 聊天时最多带几条相关记忆 |  |

## 许可

[大肥鱼 非商业许可协议 v1.0](LICENSE)：可以看、可以自己用、可以改，**不得商用**——不得收费代部署 / 代托管 / 做成 SaaS，不得改成别家 Agent 或产品卖。整套部署方法见 [大肥鱼主仓库](https://github.com/mengbaiyoudianxian/dafeiyu)。
