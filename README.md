# 精选直播源

一份实测可用的 IPTV 播放列表（m3u），覆盖中国大陆、中国香港、中国台湾、日本、英国、美国、俄罗斯、乌克兰、法国。

## 文件说明

| 文件 | 说明 |
| --- | --- |
| `playlist.m3u` | 主列表，203 个频道，按地区分组 |
| `chinese.m3u` | 中文频道精简版 |
| `config.json` | TVBox / 猫影视类 App 的接口配置，直播源指向本仓库的 `playlist.m3u` |

## 怎么筛选出来的

从公开源采集 4688 个候选地址，逐个测试连通性 → 拉取真实视频分片 → 实测下载速率，最后只保留能真正播放的。详细速率见主列表文件名中的分组标记。

## 用法

在 TVBox / 猫影视类 App 的「推送」或「接口」里填入：

```
https://cdn.jsdelivr.net/gh/kyousukeQWQ/iptv-playlist@main/config.json
```

或者直接导入播放列表：

```
https://cdn.jsdelivr.net/gh/kyousukeQWQ/iptv-playlist@main/playlist.m3u
```

## 说明

- 列表里的频道都是互联网上的公开直播地址，来源为各电视台官网、公开 CDN 及公开聚合列表。
- 这类地址会不定期失效，失效后重新替换 `playlist.m3u` 即可，`config.json` 不用改。
- 部分频道有地区限制或限时播出，实测结果仅代表导出当时、在当地网络下的情况。
