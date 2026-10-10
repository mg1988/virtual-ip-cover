# virtual-ip-cover：虚拟 IP 直出封面 Skill

> 封面决定点击。这是一个让 AI 直接交付**可发布封面成品图**的 skill：虚拟 IP 出镜、生图只出无字底图、中文用代码叠字、逐张验图，不过不交付。

## 它解决什么问题

- 大多数封面工具只给你一段提示词，跑图、排字、修错字全是你自己的活。
- 生图模型写中文必错字，塑料全息感又一眼假，信息流里零点几秒就被划走。
- 今天一个风格明天一个风格，账号永远攒不出识别度。

这个 skill 把诺鸭船长 @noahduck283 的封面方法论（《如何做出一个好封面：从入门到榨干》）沉淀成了可执行流程，并附带一套已实测出图的 9 种风格和一个 AIGC 虚拟人物示例。

## 核心打法

1. **先看图再读文**：开工前逐张拆解参考封面的视觉语法（比例、承载面、标题压边、数据行配色、IP 占比与动作），只学文字方法论不看图，必翻车。
2. **虚拟 IP 出镜**：默认是一个 25 岁戴黑框眼镜的 AIGC 码农（可换成你自己的角色/吉祥物），人物动作必须和标题发生关系，不站桩。
3. **生图只生无字底图**：提示词锁死「零文字」，中文标题一律用 PIL 叠字，从根上消灭错字。
4. **风格库选型**：9 种已验证风格按题材选，同题出 2 版给人挑；系列默认风格定死，连出 5 期攒识别。
5. **逐张验图**：成品图必须打开逐字核对，没真看完不许声称已验收。

## 风格库一览

| 风格 | 适合 | 示例 |
|---|---|---|
| 撕纸概念海报 | 方法论、干货长文 | examples/cover-tearpaper-34.jpg |
| 浅色极简大字 | 连载系列、稳重题 | examples/style-minimal-light.jpg |
| 黄底夸张直球 | 工具横评、免费额度、突发爆点 | examples/style-direct-yellow.jpg |
| 聊天框风 | 社交话题、轻松题 | examples/style-chat.jpg |
| 复古报纸风 | 盘点、严肃干货 | examples/style-newspaper.jpg |
| 深色夜读 | 深度长文 | examples/style-dark-minimal.jpg |
| 深色终端科技风 | 工具、代码、Agent | examples/style-terminal.jpg |
| 浅色产品 UI 风 | 产品测评、工具横评 | examples/style-product-ui.jpg |
| 硬核数据截图 | 有真实后台/结果截图时 | 须真图，禁止编数据 |

横幅示例（X 长文头图约 5:2）：

![撕纸横幅](examples/cover-tearpaper-wide.jpg)

出镜人物参考：

![人物参考](examples/persona-ref.jpg)

## 安装

把本仓库放到你的 Agent skills 目录即可，例如：

- Muse / 通用：`~/.muse/skills/virtual-ip-cover/`
- 其他支持 SKILL.md 的 Agent：其 skills 目录下同名文件夹

然后复制 `config.example.md` 为 `config.md`，换上你自己的角色与默认风格。

## 使用

对你的 Agent 说：

```
使用 $virtual-ip-cover 给这篇文章做封面：<文章链接或正文>
```

它会走完：拆解参考图 → 提炼价值承诺 → 选风格 → 定标题 → 生无字底图 → 代码叠字 → 验图交付。常用三规格（X 约 5:2、公众号 2.35:1、竖版 3:4）同风格齐活。

## 文件结构

- `SKILL.md`：主流程与输出契约
- `references/noah-cover-method.md`：封面方法论沉淀（四大流派/三大死穴/执行参数）
- `references/visual-grammar.md`：从 14 张参考图拆出的视觉语法与开工前强制动作
- `references/style-library.md`：9 种已实测风格的配方与选用原则
- `references/persona.md`：示例 AIGC 人物设定与动作库
- `examples/`：人物参考 + 各风格成品示例

## 致谢

方法论来自诺鸭船长 @noahduck283 的 X 长文《如何做出一个好封面：从入门到榨干》；本仓库只做方法摘要与落地执行，不含原文全文，角色与图片均为原创生成。

## License

MIT
