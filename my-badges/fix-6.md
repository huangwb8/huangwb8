<img src="https://my-badges.github.io/my-badges/fix-6.png" alt="I did 6 sequential fixes." title="I did 6 sequential fixes." width="128">
<strong>I did 6 sequential fixes.</strong>
<br><br>

Commits:

- <a href="https://github.com/huangwb8/VibeNotification/commit/087f35e339d180d37e3d763366fe2a2b879eb4e4">087f35e</a>: fix(parsers): v1.0.25 强化钩子幂等与误通知抑制

- 修复 Claude Code 增量消息、后台任务与未知钩子的误通知
- 增加 Codex turn 跨进程幂等并强化生命周期事件静默
- 补充回归测试、语义文档与 1.0.25 发布元数据
- <a href="https://github.com/huangwb8/VibeNotification/commit/d06d734a34149318e4f4126e0a6e55f8b88f3837">d06d734</a>: fix(parsers): v1.0.23 抑制子代理钩子误通知，扩展 Codex 钩子事件识别

- 识别 Claude Code 子代理 sidechain 与 subagent 标记，跳过其 Stop 钩子通知
- 扩展 Codex 钩子事件类型，新增 subagentstart/subagentstop/precompact 等
- 新增官方钩子语义文档与子代理误通知回归测试
- <a href="https://github.com/huangwb8/VibeNotification/commit/6655f4f15ac912c824f5d6f63caf54e8f715106c">6655f4f</a>: fix(parsers): v1.0.22 抑制 Claude Code 重复 Stop 与非回复钩子误通知

- 增加 Claude Stop 去重状态，避免同一回复被多次通知
- 将 Notification 等非终止 hook 标记为显式忽略并在核心流程跳过
- 补充回归测试并更新发布版本到 1.0.22
- <a href="https://github.com/huangwb8/VibeNotification/commit/39c0da4f20a018fe93e41cb75f96751d737745f7">39c0da4</a>: fix(parsers): v1.0.21 修复 Claude Code 新版 Stop 钩子高频误通知

- 新增基于 transcript_path 真实状态的中间停止判定，仅在主代理完整回复结束时通知
- 通过 stop_hook_active 去重 Stop 链重复触发，避免重复通知
- 跳过 transcript 尾部元数据行，无 transcript 或读取失败时保守通知避免漏报
- 新增 8 个回归测试覆盖中间停止、回复结束、元数据跳过、去重与回退场景
- <a href="https://github.com/huangwb8/VibeNotification/commit/074da447aec43dc967c85e08d1322d41d33a4451">074da44</a>: fix(detectors): v1.0.19 将 SessionEnd/SubagentStop 标记为非回复完成，修复误通知

- SessionEnd 和 SubagentStop 不再触发通知，仅 Stop（主回复完成）触发
- Codex session-end 事件及嵌套 session-end 统一忽略
- Codex commentary phase 不再误判为最终答复，优先检测 terminal phase
- 移除 Claude Code parser 中 toolName 检测，避免工具调用误触发
- doctor 建议更新：SessionEnd hook 降级为 WARN，推荐仅使用 Stop
- 精简 README 文档，移除多余的 SessionEnd/SubagentStop 配置示例
- <a href="https://github.com/huangwb8/VibeNotification/commit/e77cc73321dfefa2b5393a43faf6866fde5d36e7">e77cc73</a>: fix(detectors): v1.0.18 修复 Codex 误通知逻辑，优化会话终止判定

- 修复 _looks_like_codex_progress_message 对确认前缀的误判，改为正确返回 True 抑制通知
- 简化 _detect_codex_conversation_end 结构化信号处理，移除冗余的 event_type 二次检查
- 修复 CI 工作流路径（src/ → vibe_notification/），改用 pip install -e . 安装
- 补充 .gitignore 对 tests/unit/test_*.py 和 conftest.py 的例外规则
- 新增单元测试文件覆盖核心逻辑


Created by <a href="https://github.com/my-badges/my-badges">My Badges</a>