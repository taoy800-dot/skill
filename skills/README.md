# Codex Skills 收藏

本仓库集中保存已安装的 Codex Skill 包，原始目录结构和配套文件尽量保持不变。

## 使用状态（2026-11-06）

产品宣传视频统一用 [OpenFilm](https://github.com/openfilm/openfilm) 官方版制作，只维护一套模板（见电脑上的 `E:\Claude超级剪辑`）。本仓库的 Skill 一律保留不删，按下表状态使用：

| 状态 | 含义 |
| --- | --- |
| ✅ 在用 | 在宣传片流程里使用 |
| ⏸ 暂停 | 和 OpenFilm 功能重叠（Remotion、HyperFrames），两套模板会让风格分叉；OpenFilm 做不到时再启用 |
| ⛔ 停用 | MoneyPrinterTurbo：用通用素材库视频配音，画面与产品无关，达不到宣传片质感 |
| ⚠️ 限用 | MediaCrawler：非商用许可，抓取的他人视频只用于分析节奏，不进成片 |

AiToEarn 内置 Skills 默认暂停；其中 `generating-videos`（Grok 生视频）只允许生成背景和氛围画面，不得生成产品本体（会画错外形、Logo 和细节）。

## 已收录

### 本机安装包

| Skill | 目录 | 状态 |
| --- | --- | --- |
| Agent Reach | [`skills/agent-reach`](./agent-reach) | 保留 |
| Copywriting | [`skills/copywriting`](./copywriting) | ✅ 在用（文案） |
| MediaCrawler Easy | [`skills/media-crawler-easy`](./media-crawler-easy) | ⚠️ 仅竞品分析 |
| MoneyPrinterTurbo Video | [`skills/moneyprinterturbo-video`](./moneyprinterturbo-video) | ⛔ 停用 |
| pyVideoTrans | [`skills/pyvideotrans`](./pyvideotrans) | ✅ 在用（外语版） |
| HyperFrames | [`skills/hyperframes`](./hyperframes) | ⏸ 暂停 |
| HyperFrames Animation | [`skills/hyperframes-animation`](./hyperframes-animation) | ⏸ 暂停 |
| HyperFrames Audio | [`skills/hyperframes-audio`](./hyperframes-audio) | ⏸ 暂停 |
| HyperFrames CLI | [`skills/hyperframes-cli`](./hyperframes-cli) | ⏸ 暂停 |
| HyperFrames Core | [`skills/hyperframes-core`](./hyperframes-core) | ⏸ 暂停 |
| HyperFrames Creative | [`skills/hyperframes-creative`](./hyperframes-creative) | ⏸ 暂停 |
| HyperFrames Keyframes | [`skills/hyperframes-keyframes`](./hyperframes-keyframes) | ⏸ 暂停 |
| HyperFrames Registry | [`skills/hyperframes-registry`](./hyperframes-registry) | ⏸ 暂停 |
| Remotion Best Practices | [`skills/remotion-best-practices`](./remotion-best-practices) | ⏸ 暂停 |

### AiToEarn 内置 Skills

已从 [yikart/AiToEarn](https://github.com/yikart/AiToEarn) 收录其 AI Agent 内置的 13 个 Skills，见 [`skills/aitoearn`](./aitoearn)。AiToEarn 上游 MIT 许可保存在该目录中：analyzing-videos、composing-videos、crawling-social-media、editing-images、editing-videos、extracting-thumbnails、generating-drama-recaps、generating-images、generating-videos、managing-content、removing-subtitles、transferring-video-styles、translating-videos。

## MediaCrawler 上游依赖

[`skills/media-crawler-easy/MediaCrawler`](./media-crawler-easy/MediaCrawler) 是指向 [NanmiCoder/MediaCrawler](https://github.com/NanmiCoder/MediaCrawler) 的 Git 子模块。MediaCrawler 上游采用非商用学习许可；其代码没有复制进本仓库提交。克隆本仓库后，用以下命令取回子模块：

```powershell
git submodule update --init --recursive
```

## 在 Codex 中安装

将要使用的单个 Skill 文件夹复制到 `%USERPROFILE%\.codex\skills\`，重启 Codex 后生效。AiToEarn 内置 Skills 位于 `skills/aitoearn/<skill-name>`，可单独复制其中任意 Skill 文件夹。

## 尚未找到的条目

- **Hyperperformers**：此前请求安装的同名项目没有出现在本机 Skill 目录中，目前也无法确认对应的 Codex `SKILL.md` 来源，因此没有用其他项目冒名替代。提供准确链接后可补入。
