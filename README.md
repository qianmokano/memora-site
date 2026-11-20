# memora-site

Memora 的静态网站，现在只有隐私政策，部署在 Cloudflare Pages（连接这个 GitHub 仓库，每次 push 到 main 自动更新）。

| 路径 | 内容 |
|---|---|
| `/` | 跳转到 `/privacy/` |
| `/privacy/` | 隐私政策（中文） |
| `/en/privacy/` | Privacy Policy（English） |

- 纯 HTML 和 CSS，没有构建步骤。Cloudflare Pages 的设置：构建命令留空，输出目录 `/`。
- 本地预览：`python3 -m http.server 8787`，打开 http://localhost:8787/privacy/
- **样式**照 App 的设计规范（`memora/docs/DESIGN.md`）：`styles.css` 的令牌抄自 `memora/docs/design-demo.html`，分组页的灰底白卡、三档字号、圆角 24 的卡片、品牌绿只用在「发邮件」按钮。改 App 的颜色时同步改这里。
- **图标** `icon.svg` 按 `memora/Icon/AppIconArt.swift` 的数据画。

## 和 App 保持一致

政策写的是 App 实际怎样处理数据，清单和要同步的时机写在 `memora/docs/PRIVACY.md`。App 的数据流变了（新的网络请求或 AI 服务商、同步方式、权限、日志内容、备份格式），要在同一次改动里更新这里的中英两页，并改顶部的生效日期。中英两页逐节对应，改一页就改另一页。
