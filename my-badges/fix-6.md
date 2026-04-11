<img src="https://my-badges.github.io/my-badges/fix-6.png" alt="I did 6 sequential fixes." title="I did 6 sequential fixes." width="128">
<strong>I did 6 sequential fixes.</strong>
<br><br>

Commits:

- <a href="https://github.com/huangwb8/ChineseResearchLaTeX/commit/81d9ed85e0a84e3fe07a5405e38fd947ea58ec06">81d9ed8</a>: fix(packages/bensz-paper): 修复 DOCX References 标题层级与 bibliography 单段排版

- 统一 References 为 Heading 1 并确保位于首条参考文献前
- 移除 CSL second-field-align="flush" 避免编号与正文拆段
- 新增标题升级与单段 bibliography 回归测试
- 版本升级 p_v20260405 → p_v20260406 / CLI 1.3.4 → 1.3.5

Co-Authored-By: Claude Opus 4.6 <noreply@anthropic.com>
- <a href="https://github.com/huangwb8/ChineseResearchLaTeX/commit/755ed2e747eafec748e1b811b2a23e557ab4235d">755ed2e</a>: fix(packages/bensz-paper): 修复 DOCX 通讯作者星号上标降级为原文 `^*^` 的问题

- 保留 Pandoc 生成的 `\*` 转义，不再在 `_convert_sup_tags_to_superscript` 中错误地将其替换为裸 `*`
- 新增转义星号单元测试与 DOCX round-trip 回归测试，防止再次回退
- 重构测试辅助函数 `_build_docx_via_production_pipeline` 以减少重复代码

Co-Authored-By: Claude Opus 4.6 <noreply@anthropic.com>
- <a href="https://github.com/huangwb8/ChineseResearchLaTeX/commit/ca50a0393f3c0b384b9d8c7d58d6dba3233d628d">ca50a03</a>: fix(packages/bensz-paper): 修复 References 书签稳定性与 DOCX 尾部章节兼容性

- main.tex 改为显式 \section{References} + \printbibliography[heading=none]，保证 PDF 书签稳定出现
- fix_docx_spacing.py 扩展尾部章节识别，兼容 Figure titles and legends 与 Supplemental information titles and legends 命名变体
- results.tex 将 cases 环境改为 array 环境，消除 xelatex 对齐符误报
- <a href="https://github.com/huangwb8/ChineseResearchLaTeX/commit/81622c670c4d2c1321809db5276530b79906feb1">81622c6</a>: fix(packages/bensz-paper): 修复 DOCX 数学公式退化、表格边框缺失与参考文献 DOI 冗余

- 重建 DOCX 导出链路：先经 HTML5+MathML 中间态再写入 Word，使 LaTeX 公式落成原生 OMML 对象
- 为 Pandoc 默认生成的 Normal Table 自动补上可见横向边框，保留已有自定义边框
- PDF/DOCX 参考文献改为 DOI 优先，抑制 URL 重复打印
- 扩充 paper-sci-01 示例：补入代表性公式、最小资源表与 CSL/bib 收口
- 新增数学语法、表格边框与 bibliography 口径回归测试
- 公共包版本升级至 p_v20260402（脚本 1.3.3）

Co-Authored-By: Claude Opus 4.6 <noreply@anthropic.com>
- <a href="https://github.com/huangwb8/ChineseResearchLaTeX/commit/26f0730e9fb0fc9cc847cdc9b5ef382e69f13dd7">26f0730</a>: fix(scripts): 修复 README 模板列表同步工作流被无关测试拦截的问题

- 将 update-template-list.yml 回归测试范围收窄至模板列表与 Issue 链接相关脚本，移除 test_install_architecture.py
- 为 pack_release.py 补回 add_*_runtime_bundle() 兼容入口，避免外部调用方断裂
- 修正 test_install_architecture.py 对 thesis-ucas-doctor 标准包内容的断言

Co-Authored-By: Claude Opus 4.6 <noreply@anthropic.com>
- <a href="https://github.com/huangwb8/ChineseResearchLaTeX/commit/5c0b14526956c94ab37dcb39870b051923903b70">5c0b145</a>: fix(packages/bensz-paper): 同步版本号至 1.3.1 并修正模块名

- 修正 __init__.py 模块文档字符串为 bensz-paper 并同步 __version__ 至 1.3.1
- 补充 __version__ 与 manuscript_tool.VERSION 的一致性测试

Co-Authored-By: Claude Opus 4.6 <noreply@anthropic.com>


Created by <a href="https://github.com/my-badges/my-badges">My Badges</a>