# 爱阅书香 · 渠道书源

为 iOS 爱阅书香准备的 JSON 配置。已有版本收到手机导入失败反馈，此版修正结构字段和下载地址，手机兼容待重新验收。

## Safari 一键导入

用 iPhone 自带 Safari 打开 **[书源导入页](https://mentalist678.github.io/iread-sources/)**，点击「导入全部书源」，确认打开爱阅书香，再在应用内核对导入预览。

若按钮没有反应，可复制[合集直链](https://mentalist678.github.io/iread-sources/configs.json)，在应用「书源配置」菜单中选择「导入剪切板中的信息」。也可尝试在「同步」中填入[本仓库地址](https://github.com/mentalist678/iread-sources)。

## 渠道

| 配置 | 范围 |
| --- | --- |
| [笔趣阁345](sources/biquge345.json) | 搜索、详情、目录、文本正文；搜索可能波动 |
| [SF轻小说公开章节](sources/sfacg-public.json) | 官方公开文本章节；不含 VIP 章节，图片附录不支持 |
| [笔迷读](sources/bimidu.json) | GBK 搜索、完整目录、正文及章内翻页 |
| [笔趣阁365](sources/biquge365.json) | 文本正文；使用与345相似的网站模板 |
| [顶点小说365](sources/dingdian365.json) | 文本正文；同类模板，搜索存在波动 |
| [合集](configs.json) | 同时包含上述五个渠道 |

修复版导入链接直接使用本站 Pages 地址，不再依赖 raw.githubusercontent.com。另提供[单源 TXT 兼容文件](sources/biquge345.txt)，内容为单个完整配置对象，与历史公开参考文件的封装形式一致，不是伪装 IBS。

已探测 [27 个平台入口](platforms.json)，其中包含起点、纵横、17K、晋江、番茄、七猫、SF、次元姬、飞卢和不可能的世界。入口可访问不等于书源可用；验证失败的平台不混入合集，同模板渠道也不宣称是独立内容库。

配置不是 IBS 加密包；通过作者支持的在线 JSON 协议导入，没有改后缀冒充 IBS。JSON 配置的正确性与 Safari 是否成功唤起应用是两项独立检查，均需手机实测。

当前搜索仅取第一页；源站缺少的章节无法靠配置补齐，亦不保证与首发平台实时同步。导入合集后无须重复导入单渠道。

## 依据

- [作者的导入与管理教程](https://jxd524.github.io/2019/03/21/booksourcesImport/)
- [公开书源页面的实际导入链接](https://wxdjs.github.io/iFreeTimebookConfigs/)

只提供配置规则，不托管小说正文。使用范围遵循内容平台的访问权限。

## 本地原版 IBS

[19 个原版书源文件及导入入口](originals.html)。18 份不同内容，重复副本保留；内部规则加密，未优化，当前可用性和 iPhone 导入待验证。

## 新增五源试用

新增16K小说、书坊文学、星星小说、大唐小说、天地中文公开章节。提供[仅导入新增五源](adapted.html)，总合集现为10个配置。前四个为相似模板备用渠道，搜索限第一页；手机导入、搜索和阅读待验证。

- 16K小说·适配试用20261016：HTTP Error 502: Bad Gateway。
- 书坊文学·适配试用20261016：桌面完整流程通过。
- 星星小说·适配试用20261016：桌面完整流程通过。
- 大唐小说·适配试用20261016：桌面完整流程通过。
- 天地中文公开章节·适配试用20261016：timed out。

参考[tickmao/Novel](https://github.com/tickmao/Novel)规则与作者教程重写；网页变更和网络波动会影响可用性。详见[本批验证记录](adapted-validation.json)。
