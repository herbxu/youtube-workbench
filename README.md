# 面朝北北 · 制作工作台

episodes/<剧集名>/ 放同一选题的草稿、版本和试听对照；examples/ 放可独立打开的样片。与同级作品库使用相同剧集 ID。制作命令由 [youtube-studio](../youtube-studio/README.md) 提供。

runtime/ 是本地运行数据，不进入 Git。正式剧集和样片的运行目录分别在 runtime/episodes/<ID>/ 和 runtime/examples/<ID>/。删除前核对活动锁、付费请求和缓存；runtime/pre-split-d3bf0d5 是本次切换前的私有回退副本，不能作为普通缓存清理。历史一次性命令和实验素材保存在 runtime/historical-project-build，不作为现行程序入口。

## 版本索引

- [20260829-竞争优势](episodes/20260829-%E7%AB%9E%E4%BA%89%E4%BC%98%E5%8A%BF/%E7%89%88%E6%9C%AC%E7%B4%A2%E5%BC%95.md)
- [20260913-企业再融资-增发和发债](episodes/20260913-%E4%BC%81%E4%B8%9A%E5%86%8D%E8%9E%8D%E8%B5%84-%E5%A2%9E%E5%8F%91%E5%92%8C%E5%8F%91%E5%80%BA/%E7%89%88%E6%9C%AC%E7%B4%A2%E5%BC%95.md)
- [20261030-熊市买入-完整版](episodes/20261030-%E7%86%8A%E5%B8%82%E4%B9%B0%E5%85%A5-%E5%AE%8C%E6%95%B4%E7%89%88/%E7%89%88%E6%9C%AC%E7%B4%A2%E5%BC%95.md)
- [20261106-字节短剧对腾讯游戏与微信时长的冲击](episodes/20261106-%E5%AD%97%E8%8A%82%E7%9F%AD%E5%89%A7%E5%AF%B9%E8%85%BE%E8%AE%AF%E6%B8%B8%E6%88%8F%E4%B8%8E%E5%BE%AE%E4%BF%A1%E6%97%B6%E9%95%BF%E7%9A%84%E5%86%B2%E5%87%BB/%E7%89%88%E6%9C%AC%E7%B4%A2%E5%BC%95.md)

新增试剪时在相应版本索引写明比较点和采用范围，作者选择另存 selection.json（scope、evidence；每条依据含 repository、path、sha256）。历史原文保留；索引及新引用使用仓库相对路径。

## 本地恢复

2026-11-13 已将整个 runtime 按原目录复制至本账户私有的 `~/Library/Application Support/youtube-studio/recovery/runtime-20261113-LNxaLW/runtime/`。源目录与副本经 rsync 内容校验一致。副本在同一块磁盘，可用于误删恢复。磁盘故障恢复仍需由持有人指定独立介质，快照含私有配置。

恢复时先停用该期流水线，从快照中把所需目录复制到空目录，核对后再接回原路径。使用 `rsync -rlcn --delete --itemize-changes 源目录/ 恢复目录/` 只读核对文件、链接和多余项。恢复付费任务时先核对请求记录，再继续制作。
