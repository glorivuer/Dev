

YC 编写的 《Vibe Coding 指南》 https://x.com/DataChaz/status/1967846530867695855

与 AI 结对编程，就像是拥有了一位虽然才华横溢、但偶尔会“走神”的实习生。它能在一小时内帮你完成过去需要一周才能搞定的工作，但有时也会在你项目的核心代码里悄悄埋下一个“惊喜”。

那么，如何才能驾驭好这位强大的编程伙伴呢？我们采访了多位利用 AI 编码的创始人，总结出了这套实用的“AI 协作编程指南”。

规划流程

好的开始是成功的一半。别指望“凭感觉编程” (Vibe Coding) 能带你走向成功。与 AI 高效协作的第一步，是制定一个清晰的路线图。

• 制定周详计划: 首先，和你的 AI 助手一起，在 Markdown 文件里写一份详尽的实施计划。
• 评审与精简: 审视这份计划，删掉不必要的部分。如果某个功能过于复杂，果断地将其标记为“暂不开发”。
• 控制项目范围: 单独开辟一个“未来想法”区域，把暂时不做的好点子都放进去，这能帮助你保持专注。
• 小步快跑，增量实现: 按部就班，一部分一部分地去实现，不要试图一口气吃成个胖子。
• 追踪进度: 每当一个部分成功实现后，让 AI 将其标记为“已完成”。
• 频繁提交: 在进入下一个环节之前，确保每个能正常工作的部分都已提交到 Git。

版本控制策略

当你的 AI 伙伴开始“自由发挥”时，版本控制系统就是你最可靠的后悔药。

• 将 Git 奉为圭臬: 不要完全依赖 AI 工具自带的撤销功能，Git 才是你的生命线。
• 从干净的起点开始: 每开发一个新功能，都确保你的 Git 工作区是干净的。
• 果断重置: 如果 AI 开始“天马行空”，让代码变得一团糟，别犹豫，立即使用 git reset --hard HEAD 命令回到上一个正常的状态。
• 避免问题滚雪球: 一次又一次失败的尝试，只会在错误的代码上堆砌更多错误的代码。
• 清爽地实现: 当你最终找到解决方案后，先重置代码库，然后在一个干净的版本上重新、清爽地实现它。

测试框架

和 AI 协作时，测试不仅是保证质量的手段，更是防止它“好心办坏事”的护栏。

• 优先进行高层级测试: 相比单元测试，优先编写端到端的集成测试。
• 模拟用户行为: 通过模拟真实用户在网站或应用中的点击操作来测试功能。
• 捕获“回归”问题: 大语言模型 (LLM) 常常会在修改代码时，无意中破坏一些不相关的功能。测试能帮你及时发现这些问题。
• 先测试，再前进: 在开始下一个新功能之前，确保所有现有的测试都能通过。
• 用测试作为护栏: 一些创始人建议，可以先编写测试用例，这能为 AI 的工作提供清晰的边界和目标。

高效修复 Bug

当 Bug 出现时，别单打独斗，让 AI 帮你分析。

• 善用错误信息: 很多时候，你只需要把完整的错误信息直接复制粘贴给 AI，它就能给出解决方案。
• 先分析，再动手: 在急于写代码修复之前，先让 AI 分析并列出几种可能导致 Bug 的原因。
• 失败后就重置: 每次修复尝试失败后，都回到干净的代码状态再进行下一次尝试。
• 添加日志: 在关键位置添加日志记录，能帮你和 AI 更好地理解代码的实际运行情况。
• 切换模型: 如果一个 AI 模型卡住了，不妨换个别的模型试试，也许会有意想不到的效果。
• 清爽地修复: 和开发新功能一样，一旦找到 Bug 的根源，就重置代码，然后干净利落地实现修复方案。

AI 工具优化

工欲善其事，必先利其器。充分配置你的 AI 工具，能让协作效率更上一层楼。

• 创建指令文件: 在项目里创建专门的指令文件（比如 cursor.rules, windsurf.rules, http://claude.md），把详细的指令和规范写在里面。
• 本地文档: 把需要用到的 API 文档下载到项目文件夹里，这能让 AI 的回答更加准确。
• 多工具协作: 有些创始人甚至会在同一个项目上同时运行 Cursor 和 Windsurf 这样的不同工具。
• 各取所长: 通常，Cursor 在处理前端任务时速度更快，而 Windsurf 更擅长处理耗时较长的复杂任务。
• 货比三家: 让不同的工具生成多种解决方案，然后挑选出最好的那一个。

复杂功能开发

面对复杂的大型功能，关键在于“化整为零”。

• 创建独立原型: 先在一个全新的、干净的代码库里，把复杂功能的核心部分构建成一个独立的原型。
• 提供参考范例: 指向一个已经能正常工作的代码示例，让 AI 学习和模仿。
• 明确边界: 保持外部 API 的一致性，允许 AI 在内部自由修改和重构。
• 模块化架构: 基于服务的模块化架构，由于其边界清晰，比庞大的单体仓库 (monorepo) 更适合与 AI 协作。

技术栈的选择

你的技术选择，会直接影响 AI 的发挥。

• 成熟框架表现更佳: 像 Ruby on Rails 这样拥有 20 年发展历史和大量惯例的框架，AI 对其理解更深。
• 训练数据是关键: 像 Rust、Elixir 这样的新兴语言，由于可供 AI 学习的公开代码较少，AI 的表现可能会稍逊一筹。
• 模块化是王道: 把代码拆分成更小的文件，不仅方便人类阅读，也更容易让 AI 理解和处理。
• 避免“万行神文件”: 不要让单个文件膨胀到数千行，这会成为你和 AI 的噩梦。
编码之外的妙用

AI 的能力远不止写代码。

• DevOps 自动化: 让 AI 帮你配置服务器、DNS 和托管服务。
• 设计辅助: 用 AI 生成网站图标 (favicon) 和其他设计元素。
• 内容创作: 帮你起草产品文档和市场营销文案。
• 你的私人教师: 让 AI 逐行解释它生成的代码，帮助你学习和理解。
• 利用截图: 遇到界面 Bug 或想借鉴某个设计时，直接把截图发给 AI。
• 语音输入: 借助像 Aqua 这样的工具，你可以用每分钟 140 个单词的速度通过语音输入指令，比打字快得多。

持续改进

与 AI 的合作是一个不断磨合、共同进步的过程。

• 定期重构: 当你建立起完善的测试体系后，就可以大胆地、频繁地进行代码重构。
• 发现改进机会: 主动询问 AI，让它帮你找出代码中可以重构优化的部分。
• 紧跟潮流: 每个新模型发布后都去试试，了解最新的技术进展。
• 认识模型特长: 不同的模型有不同的“性格”和擅长的领域，学会在合适的任务中选择合适的模型。


YC guide to vibe coding
Planning process
Create a comprehensive plan: Start by working with the Al to write a detailed implementation plan in a markdown file
Review and refine: Delete unnecessary items, mark features as won't do if too complex
Maintain scope control: Keep a separate section for ideas for later to stay focused
Implement incrementally: Work section by section rather than attempting to build everything at once
Track progress: Have the Al mark sections as complete after successful implementation
Commit regularly: Ensure each working section is committed to Git before moving to the next
Version control strategies
Use Git religiously: Don't rely solely on the Al tools' revert functionality
Start clean: Begin each new feature with a clean Git slate
Reset when stuck: Use git reset --hard HEAD if the Al goes on a vision quest
Avoid cumulative problems: Multiple failed attempts create layers and layers of bad code
Clean implementation: When you finally find a solution, reset and implement it cleanly
Testing framework
Prioritize high-level tests: Focus on end-to-end integration tests over unit tests
Simulate user behavior: Test features by simulating someone clicking through the site/app
Catch regressions: LLMs often make unnecessary changes to unrelated logic
Test before proceeding: Ensure tests pass before moving to the next feature
Use tests as guardrails: Some founders recommend starting with test cases to provide clear boundaries
Effective bug fixing
Leverage error messages: Simply copy-pasting error messages is often enough for the Al
Analyze before coding: Ask the Al to consider multiple possible causes
Reset after failures: Start with a clean slate after each unsuccessful fix attempt
Implement logging: Add strategic logging to better understand what's happening
Switch models: Try different Al models when one gets stuck
Clean implementation: Once you identify the fix, reset and implement it on a clean codebase

Al tool optimization
Create instruction files: Write detailed instructions for your Al in appropriate files (cursor.rules, windsurf.rules, claude.md)
Local documentation: Download API documentation to your project folder for accuracy
Use multiple tools: Some founders run both Cursor and Windsurf simultaneously on the same project
Tool specialization: Cursor is a bit faster for frontend work, while Windsurf think slonger
Compare outputs: Generate multiple solutions and pick the best one
Complex feature development
Create standalone prototypes: Build complex features in a clean codebase first
Use reference implementations: Point the Al to working examples to follow
Clear boundaries: Maintain consistent external APIs while allowing internal changes
Modular architecture: Service-based architectures with clear boundaries work better than monorepos
Tech stack considerations
Established frameworks excel: Ruby on Rails works well due to 20 years of consistent conventions
Training data matters: Newer languages like Rust or Elixir may have less training data
Modularity is key: Small, modular files are easier for both humans and Als to work with
Avoid large files: Don't have files that are thousands of lines long
Beyond coding
DevOps automation: Use Al for configuring servers, DNS, and hosting
Design assistance: Generate favicons and other design elements
Content creation: Draft documentation and marketing materials
Educational tool: Ask the Al to explain implementations line by line
Use screenshots: Share Ul bugs or design inspiration visually
Voice input: Tools like Aqua enable 140 words per minute input
Continuous improvement
Regular refactoring: Once tests are in place, refactor frequently
Identify opportunities: Ask the Al to find refactoring candidates
Stay current: Try every new model release
Recognize strengths: Different models excel at different tasks
