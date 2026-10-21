# 秩野Vibe｜小红书图文制作技能

这是一套用于「秩野Vibe」账号的小红书图文制作技能。它保留账号已经确认的标题逻辑、封面层级、视觉风格、可编辑 Canva 交付方式，以及每次调整后的 GitHub 同步规则。

仓库地址：[PD-XuHui/--ZY](https://github.com/PD-XuHui/--ZY)

## 换电脑后的首次安装

在新电脑安装并登录 Codex 后，把本仓库克隆到 Codex 的技能目录。Windows 默认目录如下：

`C:\Users\你的用户名\.codex\skills\artifact-template-vibe`

在 PowerShell 中执行：

```powershell
New-Item -ItemType Directory -Force "C:\Users\你的用户名\.codex\skills"
git clone https://github.com/PD-XuHui/--ZY.git "C:\Users\你的用户名\.codex\skills\artifact-template-vibe"
```

完成后新开一个 Codex 对话，即可直接输入：

```text
$artifact-template-vibe 制作选题：你的选题名称
```

也可以直接说“为秩野Vibe制作小红书图文”，Codex 会根据技能说明进入对应工作流。

## 已经安装过时如何更新

不要重复克隆。进入已有技能目录后拉取最新版本：

```powershell
git -C "C:\Users\你的用户名\.codex\skills\artifact-template-vibe" pull --ff-only origin main
```

如果此电脑曾手动修改过技能文件，先保留或提交本地修改，再更新，避免覆盖未同步的内容。

## 日常创作方式

1. 提供一个选题，先只产出标题、封面钩子、页数和每页文字；此阶段等待确认。
2. 你确认后，再生成底图、排版为可编辑文字并制作 Canva 图文。
3. 你说“确认保存”后，检查 Canva 的 3:4 比例、页数、文字可编辑状态和保存状态。
4. 同步在对应选题目录生成发布信息 Markdown，包含标题、简介、最多 5 个话题、页数和 Canva 链接。

## 这套技能固定保留的规则

- 标题与封面主标题：**行动激励＋具体方法＋明确结果**。
- 封面小字：**用户痛点＋干货形式＋收藏理由**。
- 所有最终中文文字均保留为可编辑文本，不能烘焙进底图。
- 封面先保证核心人物、产品或对比差异足够大，再安排留白；手机缩略图下必须一眼看出主体。
- 人物封面优先半身、三分之二身或局部特写；确需全身时，人物从头到脚宜占画面高度约 60% 以上。
- 对比图只改变要解释的变量，避免通过换脸、换光线或换服装误导效果。
- 内容默认服务普通男生的低成本形象提升，不局限于服装，也可涵盖发型、眼镜、清洁、气味、体态、剃须和生活习惯。

详细执行规则见：

- [SKILL.md](SKILL.md)：技能入口与工作约束
- [制作与归档工作流](references/production-workflow.md)：文案确认、Canva 保存、发布信息与归档
- [视觉规范](references/visual-style.md)：字体、颜色、构图、人物、封面缩略图验收

## 本仓库包含与不包含什么

本仓库包含可迁移的**技能规则、参考图、视觉规范与工作流**。

本仓库不包含每个选题的成品、历史数据、发布信息、账号素材库或本地 Canva 导出文件。换电脑时，如需无缝延续运营，还应单独迁移你的 `秩野Vibe【小红书】` 账号项目文件夹；Canva 设计需在新电脑登录同一个 Canva 账号后继续编辑。

## 技能更新与 GitHub 同步

之后每次调整本技能的规则、参考图、模板或工作流，均按以下流程处理：

1. 检查修改内容是否只影响本技能；
2. 验证后提交 Git；
3. 推送到本仓库的 `main` 分支；
4. 返回提交结果。

不会提交访问令牌、账号密码、个人凭据、临时文件或无关项目文件。

## 仓库结构

```text
artifact-template-vibe/
├── SKILL.md                    # Codex 读取的核心技能说明
├── artifact-template.json      # 模板元数据
├── assets/                     # 视觉参考图
├── references/                 # 制作工作流与视觉规范
└── agents/openai.yaml          # 技能界面元数据
```
