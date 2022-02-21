# vocaloid-china-biliran-data
 
从萌娘百科整理得到的 [周刊 VOCALOID 中文排行榜](https://space.bilibili.com/156489) 数据。

数据格式为 json，每一期周刊单独存为一个文件。

目前统计了 ♪118–♪497 的全部数据。


## 数据格式

每一期的数据为一个文件名为期号的 json 文件。

根对象为一个数组。数组中的对象为按照当期排名依次排列的 **Super Hit** 曲目（位于最前）、**主榜**曲目和 **Pick Up** 曲目。

曲目对象：

| 键        | 类型   | 说明                                                      |
|----------|------|---------------------------------------------------------|
| `id`       | `num`  | 视频 av 号。所有的 BV 号均转换成了 av 号以保证前后数据统一                     |
| `title`    | `str`  | 曲名                                                      |
| `isCover`  | `bool` | 是否为翻唱曲。`true`为翻唱，`false`为原创曲                            |
| `rank`     | `num`  | 排名。SH使用`0`表示                                            |
| `date`     | `str`  | 视频发布时间。格式为`yyyy-MM-dd HH:mm` （481期后为`yyyy/MM/dd HH:mm`） |
| `point`    | `num`  | 最终得点                                                    |
| `view`     | `num`  | 播放数                                                     |
| `reply`    | `num`  | 评论数                                                     |
| `danmaku`  | `num`  | 弹幕数                                                     |
| `favorite` | `num`  | 收藏数                                                     |
| `corrA`    | `num`  | 修正 A                                                    |
| `corrB`    | `num`  | 修正 B                                                    |

参见萌娘百科模板页面 [Template:VOCALOID_Chinese_Ranking](https://zh.moegirl.org.cn/Template:VOCALOID_Chinese_Ranking) 。

注：
* “评论权重” 在数值上等于 修正 A × 25 （`corrA * 25`）
* “弹幕权重” 在数值上等于 修正 A （`corrA`）
* “收藏权重” 在数值上等于 修正 B （`corrB`）
* “播放权重” 可根据周刊规则中 “播放得点” 部分直接计算，但只有当修正 B < 10 时会在视频中显示出来。

## 授权协议

周刊 VOCALOID 中文排行榜 ♪118–♪306 采用 [CC BY-NC-ND 3.0 中国大陆](https://creativecommons.org/licenses/by-nc-nd/3.0/cn/) 许可协议；
♪307–♪324 没有声明许可协议；♪325 以后采用 [CC BY-NC-ND 4.0 国际](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.zh) 许可协议。

萌娘百科采用 [CC BY-NC-SA 3.0 中国大陆](https://creativecommons.org/licenses/by-nc-sa/3.0/cn/deed.zh) 许可协议。


## 更新


* ~~♪118–♪450 数据于 2021-5-5 收集自萌娘百科。~~
* ~~♪451–♪483 数据于 2021-11-19 收集自萌娘百科。~~
* ~~♪484 数据于 2021-11-21 收集自萌娘百科。~~
* ♪118–♪497 数据于 2022-2-21 重新收集自萌娘百科，并且对数据格式做了调整。


## 勘误

按照萌娘百科上的记录对部分数据进行了手动修正：

* ♪129 7 位《神经病之歌》收藏数 43 → 247；
* ♪255 SH 《达拉崩吧》播放数 160758 → 112141；
* ♪371 SH 《达拉崩吧·史诗版》发布日期 2019-08-17 09:47 → 2019-08-17 17:47；播放数 115844 → 97333。


## 特别鸣谢

* 洛天依新曲排行榜、中文VOCALOID新曲排行榜及周刊VOCALOID中文排行榜 [制作组](https://zh.moegirl.org.cn/%E5%91%A8%E5%88%8AVOCALOID%E4%B8%AD%E6%96%87%E6%8E%92%E8%A1%8C%E6%A6%9C#%E5%88%B6%E4%BD%9C%E4%BA%BA%E5%91%98)
* [萌娘百科](https://zh.moegirl.org.cn/Mainpage) 及 [萌百VC编辑团队](https://zh.moegirl.org.cn/User:%E7%A9%BA%E7%BF%8A/%E8%90%8C%E7%99%BEVC%E7%BC%96%E8%BE%91%E5%9B%A2%E9%98%9F) 、[周刊VOCALOID中文排行榜页面贡献者](https://zh.moegirl.org.cn/User:4O74Y74L74J7/%E5%91%A8%E5%88%8AVOCALOID%E4%B8%AD%E6%96%87%E6%8E%92%E8%A1%8C%E6%A6%9C) 

## 碎碎念

* 如你所见，周刊的每个视频简介里都会留下 http://vc.biliran.moe/ 这个神秘的周刊官网地址。你说它停更了，但是它确实在定期更新内容（虽然常常比 B 站视频晚一两期）；你说它更新及时，但是网站页面布局全是旧的，刊娘画风和 B 站 logo 全是 2015 年以前的样子，甚至还挂着一个早就用不了的“B 站视频专题”链接……
    * 顺带一提，这一域名的主站 www.biliran.moe 在几年以前也确实是周刊哔哩哔哩排行榜的官网，但是不知道什么时候挂了（ [网页时光机](https://web.archive.org/web/20151025211010/http://www.biliran.moe/) ），倒是 VC 子站点还活到了现在……
* 这些数据能不能做成 API？在学了在学了，下次一定做好
* ~~刊娘真可爱~~