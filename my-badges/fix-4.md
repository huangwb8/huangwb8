<img src="https://my-badges.github.io/my-badges/fix-4.png" alt="I did 4 sequential fixes." title="I did 4 sequential fixes." width="128">
<strong>I did 4 sequential fixes.</strong>
<br><br>

Commits:

- <a href="https://github.com/huangwb8/ChineseResearchLaTeX/commit/cd89694f0a23142ec2a7a070833efa80518a7402">cd89694</a>: fix(bensz-thesis): 对齐 thesis-nju-master 章标题/目录/小节/图表/表格字体与南京大学论文规范

- 章标题字号收敛为小三号仿宋加黑（15bp），目录章级条目补回小四号仿宋加粗
- 小节标题行距调整为小四号 1.5 倍口径（18bp baseline）
- 图表题注统一使用五号仿宋，表格正文（tabular/tabularx/longtable）默认五号仿宋
- 包版本推进至 p_v20260606.3，避免安装器跳过此次样式修复
- <a href="https://github.com/huangwb8/ChineseResearchLaTeX/commit/51a5e635833321867616197fc5ccdd2a78b1f1f5">51a5e63</a>: fix(bensz-thesis): 对齐 thesis-nju-master 目录页章级条目与内容列缩进

- 收回章级条目左凸问题，让"第 1 章 绪论"等与摘要、参考文献等目录项处于同一内容列
- 调整 section/subsection 缩进与点线密度，改善目录层级拥挤问题
- 目录页后追加 \thispagestyle{njuempty} 抑制页码
- 将 package.json 版本推进到 p_v20260606.2
- <a href="https://github.com/huangwb8/ChineseResearchLaTeX/commit/272b32ca741a3425cfc321479b6480e3148531c8">272b32c</a>: fix(bensz-thesis): 对齐 thesis-nju-master 与南京大学 2023.2 论文规范的仿宋体系与前后置材料

- 将正文、章节标题、摘要标题和图表题注统一收敛到仿宋字体（AutoFakeBold=3.5），封面根据 \njuSetDegreeType 区分"申请硕士专业学位/申请硕士学位"与"专业学位类别（领域）/学科、专业名称"字段
- 新增原创性声明、学位论文使用授权声明和出版授权书页面宏，章节编号改用阿拉伯数字
- 移除 README 中不存在的 baseline.tex 说明，同步更新 CHANGELOG 并将 package.json 版本推进到 p_v20260606.1
- <a href="https://github.com/huangwb8/ChineseResearchLaTeX/commit/544ab447d77a8222f4cca9f326c69afa58af4cb9">544ab44</a>: fix(bensz-thesis): 优化 thesis-nju-master 封面题目填写区与目录层级样式

- 扩大封面字段区与下划线宽度，对超长题目增加自动测量与等比压缩保护
- 重新设计目录页章/节/小节层级缩进与点线节奏，改善拥挤问题
- 将 package.json 版本推进到 p_v20260606


Created by <a href="https://github.com/my-badges/my-badges">My Badges</a>