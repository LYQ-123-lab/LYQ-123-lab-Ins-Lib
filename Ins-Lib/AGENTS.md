# AGENTS.md - Ins_Lib RSS个人灵感库
遵循 Karpathy LLM Wiki 方法论
参考：https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

## 目录说明
- raw/：RSS抓取的原始内容，保存标题、来源链接、发布时间
- wiki/：提炼主题、趋势、观点、案例、创作选题灵感，持续关联更新

## RSS订阅源（B组 宏观补充 · 20源）
教育部最新文件：https://rsshub.dicomp.net/gov/moe/newest_file
政策解读：https://rsshub.dicomp.net/gov/moe/policy_anal
教育考试网中小学教师资格：https://rsshub.dicomp.net/neea/local/ntce
PubScholar 公益学术平台：https://rsshub.dicomp.net/pubscholar/explore
联合早报 中港台：https://rsshub.dicomp.net/zaobao/realtime/china
央视新闻联播：https://rsshub.dicomp.net/cctv/lm/xwlb
知乎热榜：https://rsshub.dicomp.net/zhihu/hot
知乎日报：https://rsshub.dicomp.net/zhihu/daily
第一财经新闻：https://rsshub.dicomp.net/yicai/news
哔哩哔哩排行榜：https://rsshub.dicomp.net/bilibili/ranking/all
36Kr热榜：https://rsshub.dicomp.net/36kr/hot-list
豆瓣实时热门书影音：https://rsshub.dicomp.net/douban/list/subject_real_time_hotest
豆瓣实时热门电影：https://rsshub.dicomp.net/douban/list/movie_real_time_hotest
豆瓣实时热门电视：https://rsshub.dicomp.net/douban/list/tv_real_time_hotest
豆瓣热门书籍：https://rsshub.dicomp.net/book/rank/fiction
财联社头条：https://rsshub.dicomp.net/cls/depth/1000
格隆汇快讯：https://rsshub.dicomp.net/gelonghui/live
金十数据：https://rsshub.dicomp.net/jin10
虎嗅24小时新闻：https://rsshub.dicomp.net/huxiu/moment

## 工作目标
不是RSS收藏夹，而是生长式灵感Wiki，用来发现趋势、选题、有价值案例，跟踪主题变化。

## 工作规则
1. 原始RSS内容存入raw，保留来源、链接、时间。
2. 新RSS内容进来优先更新已有wiki页面，只有全新重要主题才新建页面，避免孤立摘要页。
3. 区分普通新闻、持续趋势、观点、创作灵感，区分信息价值高低。
4. 自动去重，不再重复处理已经入库的文章。
5. 架构保持简单：本地Markdown文件，不引入额外数据库、向量库。
6. 所有结论可追溯到raw里RSS原文。

## RSS订阅源（A组 新传主线 · 14源）

【新媒体行业智库】
36氪：https://36kr.com/feed
极客公园：https://www.geekpark.net/rss
人人都是产品经理：https://rsshub.app/woshipm/popular
新榜周刊：https://rsshub.app/newrank/weekly
全媒派（腾讯传媒智库）：https://rsshub.app/qqnews/quanmeipai

【主流媒体融合、舆论、全媒体研究】
人民网研究院：https://rsshub.app/people/research
澎湃新闻：https://rsshub.app/thepaper/recommend
新京报传媒研究：https://rsshub.app/xjbcmresearch

【数字媒介、AIGC、互联网平台观察】
爱范儿：https://www.ifanr.com/feed
量子位：https://www.qbitai.com/feed
少数派：https://sspai.com/feed

【海外媒介研究】
Nieman Journalism Lab：https://niemanlab.org/feed/
AP News 媒介科技板块：https://apnews.com/hub/technology/rss
The Verge：https://www.theverge.com/rss/index.xml

## 订阅规则（2026-10-27 增补，适用于全部源站）

1. 每次抓取只拉最新条目，自动去重，已入库条目不再重复处理。
2. 原始全文、标题、发布时间、原文链接完整存入 raw/。
3. 提炼优先识别：媒介现象、平台算法、短视频/账号传播案例、AIGC内容生产、舆论演变、媒体融合、国际传播相关观点。
4. 自动分级标注内容类型：【短时新闻】【持续趋势】【核心观点】【优质案例】【创作选题】。
5. 同主题新旧文章自动关联、更新主题wiki页面，不孤立生成摘要。
6. 标签体系：#媒体融合 #AIGC传播 #平台研究 #舆论观察 #新媒体案例 #国际传播。
7. 严格隔离：只在 Ins-Lib 内部检索关联，绝不读取 Style-Lib、Vibe-Note 素材。
8. 分组标签：每篇入库笔记强制打上 #A新传主线 或 #B宏观补充（由源站决定），与内容分级标签并存。
9. 关联规则：优先同组内建立关联；跨组关联只在信息确有内在逻辑时才链接，不强牵线，避免主题信号被稀释。
10. 抓取范围：34源全部参与日常自动增量抓取，不设低频限制、不做源站取舍；每次只取自上次以来的新条目，靠台账去重。
11. 链接格式（2026-10-27 修订，自下一次「读取RSS入库」起生效）：
    - 外部网页原文链接一律用标准 Markdown 链接语法，URL 外套尖括号：`[原文链接](<https://xxx>)`。
    - 禁止裸写 URL：链接里的下划线、括号等符号会破坏 Obsidian 解析，导致无法点击跳转。
    - 库内页面之间的关联继续用 Obsidian 原生双链 `[[笔记名]]`，不用 Markdown 链接替代。
    - 已入库的历史笔记不批量回改，维持原样；新抓的条目、新写的页面一律用新格式。

## 支持指令
1. 读取RSS订阅源，获取自上次执行以来的新内容，按规则入库更新wiki
2. 查询：最近值得关注的方向 / 某个主题的发展变化 / 可组合的选题