<img src="https://my-badges.github.io/my-badges/fix-3.png" alt="I did 3 sequential fixes." title="I did 3 sequential fixes." width="128">
<strong>I did 3 sequential fixes.</strong>
<br><br>

Commits:

- <a href="https://github.com/huangwb8/bensz-channel/commit/cec20a77c95894c88f97de1b3a1e78df0f4b471f">cec20a7</a>: fix(ui): 修复频道管理界面夜间模式显示异常

- 为频道管理页各区块挂载语义化 channel-admin-* 样式类
- 拖拽高亮从硬编码 ring-blue-200 改为主题变量驱动
- 测试锁定 channel-admin-create-form、switch-track、card-dragging 类存在
- <a href="https://github.com/huangwb8/bensz-channel/commit/0c1bbd4d6b448cdb4fed8c787bad204de90e2c4d">0c1bbd4</a>: fix(docker): 修复 Web 容器图片上传大小限制

- 将 Nginx client_max_body_size 调整为 12m，解决 413 Payload Too Large
- 新增 php-upload.ini，将 upload_max_filesize 设为 10M、post_max_size 设为 12m
- Dockerfile 构建时复制上传配置到 PHP conf.d
- docker-smoke.sh 新增约 2MB 大图粘贴上传回归用例
- <a href="https://github.com/huangwb8/bensz-channel/commit/b321641a19780f3527514ab207995bdd6ed6fd8f">b321641</a>: fix(editor): 修复 Markdown 编辑器粘贴图片上传失败问题

- 独立封装粘贴逻辑，优先读取 clipboardData.items，必要时回退到 files
- 为剪贴板产生的无扩展名图片自动补齐稳定文件名
- 移除手工指定 multipart 请求头，改由浏览器自动附带 boundary
- 新增前端粘贴上传单元测试，校验剪贴板图片回退提取与 JPG 文件名补全
- 新增文章详情页快捷编辑回归测试，锁定管理员可直接进入编辑
- 优化文章详情页管理员操作路径，直接显示"编辑文章"入口

Closes #image-upload-issue


Created by <a href="https://github.com/my-badges/my-badges">My Badges</a>