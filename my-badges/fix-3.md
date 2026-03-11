<img src="https://my-badges.github.io/my-badges/fix-3.png" alt="I did 3 sequential fixes." title="I did 3 sequential fixes." width="128">
<strong>I did 3 sequential fixes.</strong>
<br><br>

Commits:

- <a href="https://github.com/huangwb8/bensz-channel/commit/e9ae55b1ebe97de98e3602c2cdd28fba23feaf01">e9ae55b</a>: fix(mobile): 修复移动端频道切换抽屉的渲染和交互问题

- 将抽屉从粘性头部内移到页面根层，避免移动端浏览器固定层渲染异常
- 统一抽屉状态管理，移除易导致双触发的 touchend 监听
- 补充 CSS isolation 和 overscroll-behavior 属性，提升移动端层叠稳定性
- 新增回归测试锁定抽屉必须渲染在 header 之外
- 更新项目版本号至 1.28.3
- <a href="https://github.com/huangwb8/bensz-channel/commit/d90c352090e20afa3badfda223bfb9381142ddd8">d90c352</a>: fix: 修复文档和工作流中 config.yaml 的过时引用

- 更新 README.md 版本号管理章节，将 config.yaml 路径更正为 app/config.toml
- 更新 GitHub Actions 工作流名称和提示信息，从 config.yaml 改为 config.toml
- 修正 README.md 中 Docker 镜像发布时间描述，从"每 12 小时"更正为"每天北京时间 02:00"
- 更新 docs/version-management.md 文档中的所有过时引用
- <a href="https://github.com/huangwb8/bensz-channel/commit/7a5648ab1f09b2ffdaae59a0f807cebc20ba7b9f">7a5648a</a>: fix(style): 修复夜间模式样式显示问题

- 统一补齐深色主题变量与组件状态色的深色覆盖
- 优化登录页在夜间模式下的高对比深色视觉
- 改进 HTML 压缩逻辑以保护 script 和 style 标签内容
- 新增夜间模式样式回归测试锁定关键 dark override


Created by <a href="https://github.com/my-badges/my-badges">My Badges</a>