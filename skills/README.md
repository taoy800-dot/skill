# Codex Skills 收藏

本仓库集中保存已安装的 Codex Skill 包，原始目录结构和配套文件尽量保持不变。

## 已收录

### 本机安装包

| Skill | 目录 |
| --- | --- |
| Agent Reach | [`skills/agent-reach`](./agent-reach) |
| Copywriting | [`skills/copywriting`](./copywriting) |
| MediaCrawler Easy | [`skills/media-crawler-easy`](./media-crawler-easy) |
| MoneyPrinterTurbo Video | [`skills/moneyprinterturbo-video`](./moneyprinterturbo-video) |
| pyVideoTrans | [`skills/pyvideotrans`](./pyvideotrans) |
| HyperFrames | [`skills/hyperframes`](./hyperframes) |
| HyperFrames Animation | [`skills/hyperframes-animation`](./hyperframes-animation) |
| HyperFrames Audio | [`skills/hyperframes-audio`](./hyperframes-audio) |
| HyperFrames CLI | [`skills/hyperframes-cli`](./hyperframes-cli) |
| HyperFrames Core | [`skills/hyperframes-core`](./hyperframes-core) |
| HyperFrames Creative | [`skills/hyperframes-creative`](./hyperframes-creative) |
| HyperFrames Keyframes | [`skills/hyperframes-keyframes`](./hyperframes-keyframes) |
| HyperFrames Registry | [`skills/hyperframes-registry`](./hyperframes-registry) |
| Remotion Best Practices | [`skills/remotion-best-practices`](./remotion-best-practices) |

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
