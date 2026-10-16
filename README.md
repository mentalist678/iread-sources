# 爱阅书香 · 渠道书源

为 iOS 爱阅书香准备的原生 JSON 配置。首批两渠道，手机端兼容仍待验证。

## Safari 一键导入

用 iPhone 自带 Safari 打开 **[书源导入页](https://mentalist678.github.io/iread-sources/)**，点击「导入全部书源」，确认打开爱阅书香，再在应用内核对导入预览。

若按钮没有反应，可复制[合集直链](https://raw.githubusercontent.com/mentalist678/iread-sources/main/configs.json)，在应用「书源配置」菜单中选择「导入剪切板中的信息」。也可尝试在「同步」中填入[本仓库地址](https://github.com/mentalist678/iread-sources)。

## 渠道

| 配置 | 范围 |
| --- | --- |
| [笔趣阁345](sources/biquge345.json) | 搜索、详情、目录、文本正文；搜索可能波动 |
| [SF轻小说公开章节](sources/sfacg-public.json) | 官方公开文本章节；不含 VIP 章节，图片附录不支持 |
| [合集](configs.json) | 同时包含上述两个渠道 |

配置不是 IBS 加密包；通过作者支持的在线 JSON 协议导入，没有改后缀冒充 IBS。JSON 配置的正确性与 Safari 是否成功唤起应用是两项独立检查，均需手机实测。

当前搜索仅取第一页；源站缺少的章节无法靠配置补齐，亦不保证与首发平台实时同步。导入合集后无须重复导入单渠道。

## 依据

- [作者的导入与管理教程](https://jxd524.github.io/2019/03/21/booksourcesImport/)
- [公开书源页面的实际导入链接](https://wxdjs.github.io/iFreeTimebookConfigs/)

只提供配置规则，不托管小说正文。使用范围遵循内容平台的访问权限。
