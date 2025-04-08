# data-analysis

## 面试题目准备

**如果你是抖音的CEO，你最关注的三个指标是什么？为什么?!**

- 用户活跃度：日活跃用户、月活跃用户比率，以及用户日均使用时长。这个指标体现了用户粘性和高频使用习惯，比率越高说明用户对平台的依赖性越高。使用时长越长则说明平台的内容对用户越有吸引力。抖音的核心竞争力是“沉浸式体验”时长短说明用户对平台的内容兴趣不大。更高的活跃度与更长的使用时长则说明有更大的商业转化机会，广告曝光将带来更大的商业利益。
- 用户留存率：新用户在首次使用后持续返回的比例。这个指标预示着抖音作为一款软件吸引新用户使用的能力。越多的用户留存则预示着平台未来的成长更为强劲。新用户愿意留在平台说明平台推荐的东西用户更喜欢，平台推荐算法更能精准地推荐用户所喜欢的东西，更了解用户喜好。
- 创作者生态指标：活跃的创作者数量，头部、中长尾用户的创作比例以及内容生产量。抖音作为一款视频分享的社交平台，其创作者是主要吸引用户使用的关键，好的创作者自然会吸引更多的人使用。创作者质量高则会带动更多人使用平台，更多人使用平台则会吸引更多人来抖音上创作分享，进而形成良性循环。高质量创作者同时也会吸引高质量商单，带动更高的商业价值。

**如果抖音人均使用时长下降怎么分析？**

- 首先，根据统计口径确认是否人均使用时长真的下降。排除其他干扰项：是否因为统计方式变更导致人均使用时长下降，是否由于节假日、或季节性波动导致人均使用时长下降。对比行业趋势，查看其他类似软件的使用时长是否下降，是否可能因为经济复苏，人们户外增多导致整个行业的用户使用时长下降。
- 其次，进行细粒度的问题定位：判断是哪部分用户的使用时长下降导致人均使用时长下降。例如是新用户还是老用户的人均使用时长下降；性还是女性的人均使用时长下降，是哪个年龄段的人均使用时长下降；哪个领域的品类人均使用时长下降，是娱乐区还是知识区；哪个时间段的人均使用时长下降，是节假日还是工作日，平台高峰期的人均使用时长是否有下降等等。
- 接着原因分析：
    * 假设1：内容生态出现问题 可以通过验证内容多样性来查看 可能因为算法过度曝光爆款导致用户审美疲劳，因而减少平台使用时长。例如，全站全是相似的变装、挑战等视频，用户产生审美疲劳，转而去其他平台观看口味不一样的视频。解决方法是：调整推荐算法，定期给用户推荐用户以前没看过的视频，提升用户的新鲜感
    * 假设2: 用户体验差 是否因为总有弹窗影响用户使用体验导致用户转而去其他弹窗少的视频平台。可能因为加入新功能，导致用户体验变差。验证的方法是做对比实验，一组给用户新页面，一组保留原有页面，对比二者使用时长，如果新页面使用时长变短，旧页面使用时长无变化则说明是新功能的引入导致用户使用不习惯进而减少了用户使用时长。解决方案是调整功能，尽量保留用户的使用习惯，减少用户因为新功能带来的学习成本。
    * 假设3：竞品软件是否提出了新的功能吸引抖音的用户转移使用平台。验证方法：查看竞品的人均使用时长，如果竞品的人均使用时长变长，则说明减少的使用时长中我们的用户转移到其他平台。解决方案：学习竞品软件的新功能点，并在抖音中也引入类似的功能点。
    * 假设4：抖音最近是否出了负面舆论，例如数据安全争议，内容审核丑闻等等。解决方案：进行公关活动，减小负面消息对抖音用户的影响。
- 最后进行类似情况的预防：定期检查人均使用时长、日均活跃用户等关键指标的情况，防微杜渐，这些指标出现不良趋势时及时揪因，及时调整。

**你认为处理异动分析的根本思想是什么？**

- 首先是确认异动内容，比如针对抖音人均使用时长下降的问题，首先要确认问题具体是什么，判断是哪部分用户的使用时长下降导致人均使用时长下降，是男性用户还是女性用户，是年轻的用户还是年长的用户；是什么时间段的用户，高峰期的使用时长是否下降；哪个类型的视频的用户使用时长下降，是娱乐区还是知识区？
- 其次是分析可能的原因：可以从视频质量，用户体验，推荐质量，舆论舆情，同品类竞品等几个方向进行分析，判断可能的原因，并加以验证。
- 最后是针对问题进行调整解决。并对调整后的结果进行检查，检查我们的调整是否解决了异动。

## SQL题目准备

**好评率计算** 西瓜视频近期开展了”2020百大人气创作者”优质内容扶持项目，鼓励用户产出优质的视频内容。现需要统计2020年11月01日至2020年11月30日期间创作的视频中，“科技”大类下“数码测评"子类的视频好评率（好评率=好评数/视频观看次数），写出sql语句进行查询。用户观看视频后的评价详情表：content_action_info：id（视频id，主键）create_time (创建时间，格式‘2020-11-01’)user_id（观看者id）content_id (视频id，外键)content_action (视频评价，包括’点赞‘，’差评‘，‘无评价’)， dim_content: content_id（视频id) content_category（视频种类）content_sub_category（视频子类）。

```sql
select
   count（1）as all_action sum(case when content_action='点赞' then 1 else 0 end) as like_action
   sum(case when content_action='点赞' then 1 else 0 end)/count(1) as like_ratefrom
   content_action_info as a join dim_content as b on a.content_id=b.content_id
where
   b.content_category='科技' and b.content_sub_category='数码测评' and a.create_time between '2020-11-01' and '2020-11-30';
```



