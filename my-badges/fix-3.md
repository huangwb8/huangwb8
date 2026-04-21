<img src="https://my-badges.github.io/my-badges/fix-3.png" alt="I did 3 sequential fixes." title="I did 3 sequential fixes." width="128">
<strong>I did 3 sequential fixes.</strong>
<br><br>

Commits:

- <a href="https://github.com/huangwb8/sub2api/commit/0ffcfbb39797ee0b06c6d2730d4e981da3da317c">0ffcfbb</a>: fix(dashboard): 重构盈利水平图表为独立组件并优化数据填充

- 抽取 ProfitabilityTrendChart 独立组件，替换 DashboardView 内联配置
- 新增 normalizeProfitabilityTrend 填充缺失时间桶，确保连续区间无断点
- 改用柱状图展示收入/成本，折线叠加利润与超额利润率

Co-Authored-By: Claude Opus 4.7 <noreply@anthropic.com>
- <a href="https://github.com/huangwb8/sub2api/commit/1ddde6d8e0eed49673a777593b65d060eef3d14a">1ddde6d</a>: fix(settings): 修复管理员首次进入系统设置页弹出 setting not found 告警

- 将 web_search_emulation_config 读取改为 fail-open 行为，空库/旧库不再报错
- 补充回归测试覆盖未配置与仓库故障场景
- 更新 CHANGELOG 与 Prompts 记录
- <a href="https://github.com/huangwb8/sub2api/commit/bad1118c0e00eb13143926957eb171d87f5712c0">bad1118</a>: fix(dashboard): 修复盈利水平图表无法正常显示的问题

- 将盈利汇总逻辑从最后一个点改为所选区间累计求和，修复全时段无数据问题
- 抽取盈利逻辑为独立模块，新增多数据集图表（收入/成本/利润/加价率）及双 Y 轴
- 补充英文国际化文案与单元测试

Co-Authored-By: Claude Opus 4.7 <noreply@anthropic.com>


Created by <a href="https://github.com/my-badges/my-badges">My Badges</a>