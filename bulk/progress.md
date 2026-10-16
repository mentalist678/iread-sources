# 按可行性转译：首轮进展

- 固定输入1194条，保留重复。基线217条，本轮新增286条；收紧校验排除1条；当前502条，其中19条复用、483条静态转译。剩余692条。
- 13项本地行为测试通过，并对全部生成配置执行结构及表达式检查；未逐站联网、未在iPhone验证。配置仍默认关闭。
- 已补：索引/排除集合、部分CSS伪类、同一上下文的规则回退、正文正则清理、简单捕获提取、详情页目录跳转、声明式初始化及别名、带选中标记的目录分页、静态单引号请求对象、首次请求参数展开。
- 已纠正：章内分页排除“下一章”链接；不再把未处理脚本前缀的正文当成转换成功。
- JSON基础语法映射已补并经过本地样例检查，但本批尚无一个JSON接口来源的全部必要链路通过。因此不能把JSON解析器支持等同于新增JSON来源。
- 目录option分页依赖选中标记；无标记时会停止，可能不完整。部分清理、登录、图片及运行时能力未移植，逐项看catalog.json的warnings。

## 后续优先级（互斥主分类）

| 优先级 | 剩余条目 | 路径 |
| --- | ---: | --- |
| 1 | 55 | 继续处理嵌套/有序集合、混合解析器回退、复杂JSON查询及捕获替换；不能改变节点和排序语义。 |
| 2 | 19 | 处理复杂目录跳转、初始化与分页状态；补充页面结构依据。 |
| 3 | 97 | 处理动态请求及请求头；只迁移可解释的静态逻辑。 |
| 4 | 521 | 逐站重新适配运行时脚本、缺规则及WebView；凭据和非文本来源单列，不通过绕过访问限制补齐。 |

上表按首要阻塞归类，完整原因仍可重叠；高优先级条目也不保证能直接完成。

## 收紧校验排除的旧条目

- main-0914：江印小说网，body: runtime JavaScript or variable dependency。不自动删除手机已有配置，请勿据旧结果认定可用。

## 依据

- https://jxd524.github.io/2018/11/14/bookConfigs/
- https://jxd524.github.io/2019/02/03/xpathEx/
- https://jxd524.github.io/2019/02/03/json-parser/
- https://jxd524.github.io/2019/02/03/regex-parser/
- https://github.com/LegadoTeam/legado/blob/master/app/src/main/java/io/legado/app/model/analyzeRule/AnalyzeByJSoup.kt
- https://github.com/LegadoTeam/legado/blob/master/app/src/main/java/io/legado/app/model/analyzeRule/AnalyzeRule.kt
