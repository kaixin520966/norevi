NOREVI X V12 Ultimate Launch Edition

上线候选版 / Launch Candidate

核心：
- 内容引擎重建：700+ 条影视标题数据。
- 主板块：韩剧 / 中剧 / 泰剧 / 电影 / 短剧 / 动漫 / 今日热门。
- 首页精选展示，更多页展开浏览。
- 去重：同一屏和首页各模块尽量避免重复。
- 每部内容包含：剧情简介、主演、导演、年份、地区、语言、类型、观看入口、相关推荐。
- 图片引擎：公开海报多源加载 + 浏览器缓存 + 懒加载；不再使用彩色假图冒充真实海报。
- 手机端优先：底部导航、底部分享栏、移动端详情页。
- 分享保留：Telegram / WhatsApp / Facebook / Viber / 系统分享 / Copy Link。
- Official Assistant: https://t.me/NOREVI01

重要说明：真实海报长期稳定秒开，最终仍建议将确认可用的海报放到自己的服务器/CDN。

打开方式：VS Code → 打开文件夹 → Go Live


V12 Performance Patch
- 修复原来只加载前80张、滑动后不继续触发的问题。
- 新增 IntersectionObserver：用户滑到哪里，自动加载哪里的海报。
- 新增加载队列，最多同时加载5张，避免手机卡顿。
- 首屏前28张优先加载，后续懒加载。
- 加载失败会停止无限Loading，显示 Poster unavailable，并允许刷新/重试。
- 成功图片缓存到浏览器 localStorage，下次打开更快。
