# Cursor IDE 使用说明文档 V0.1

​	以下是 Cursor IDE 最新版本的详细使用说明文档，基于用户提供的模板，结合官方文档和其他可靠资源编写。文档结构清晰，由浅入深，涵盖从安装到高级功能的所有关键内容，旨在帮助用户全面掌握这款 AI 驱动的集成开发环境（IDE）。内容基于截至 2025 年 5 月 8 日的可用信息，部分细节可能因版本更新而有所变化，建议参考 官方文档 获取最新信息。

---

## 1. 介绍

### 1.1 什么是 Cursor IDE

​	Cursor IDE 是一个人工智能驱动的集成开发环境，旨在通过将先进的 AI 功能无缝集成到编码流程中来提升开发人员的生产力。它由 Anysphere Inc. 开发，是 Visual Studio Code（VS Code）的分支，增加了代码生成、智能重写、代码库查询等 AI 功能。Cursor IDE 特别适合希望利用 AI 加速开发流程的开发者，同时保留了 VS Code 的熟悉界面和扩展生态。

### 1.2 主要功能和特点

Cursor IDE 的核心功能包括：

- **标签完成（Tab Completion）**：提供智能代码建议，支持多行编辑和现有代码修改。
- **聊天 AI（Chat）**：在 IDE 内与 AI 交互，查询代码库或获取编码帮助。
- **⌘K（Command-K）**：用于高级代码编辑和操作。
- **AI 提交消息生成**：自动生成 Git 提交消息。
- **便笺（Notepads，Beta）**：在 IDE 内记录笔记。
- **代码库索引（Codebase Indexing）**：帮助 AI 理解项目结构，提供更精准的建议。
- **规则（Rules）**：自定义 AI 行为。
- **@ 符号**：快速访问函数、变量或文档。
- **忽略文件（Ignore Files）**：排除特定文件不被 AI 分析。
- **模型上下文协议（Model Context Protocol）**：支持集成自定义 AI 模型。
- **计划和使用（Plans & Usage）**：管理订阅和使用情况。
- **隐私与安全（Privacy & Security）**：提供数据保护选项，符合 SOC 2 认证。
- **支持多种 AI 模型**：包括自定义 API 密钥。
- **早期访问计划（Early Access Program）**：体验新功能。
- **故障排除指南（Troubleshooting Guide）**：解决常见问题。

### 1.3 系统要求

由于 Cursor IDE 基于 VS Code，其系统要求与 VS Code 类似：

- **Windows**：Windows 10 或更高版本（不支持 Windows 7 和 8.1）。
- **macOS**：macOS 11 Big Sur 或更高版本。
- **Linux**：大多数 Linux 发行版，需 GLIBCXX 版本 3.4.15 或更高，GLIBC 版本 2.15 或更高。
- **存储**：下载大小小于 200 MB，磁盘占用小于 500 MB。
- **其他**：稳定的互联网连接以支持 AI 功能，推荐 4GB 内存（8GB 更佳）。

| 操作系统 | 最低版本        | 内存 | 磁盘空间    |
| -------- | --------------- | ---- | ----------- |
| Windows  | 10              | 4GB  | &lt; 500 MB |
| macOS    | 11 Big Sur      | 4GB  | &lt; 500 MB |
| Linux    | GLIBCXX 3.4.15+ | 4GB  | &lt; 500 MB |

---

## 2. 安装和设置

### 2.1 下载和安装

安装 Cursor IDE 的步骤简单：

1. 访问 Cursor 官网 并点击“下载”按钮，安装程序会根据您的操作系统自动下载。
![image](https://github.com/user-attachments/assets/e8b853f2-8c72-4a13-bc1f-01e2e8eb2b33)
2. 运行下载的安装程序，按照提示完成安装。
3. 安装完成后，通过桌面快捷方式或应用程序菜单启动 Cursor。

对于 Linux 用户，Cursor 提供 AppImage 格式，下载后需设置可执行权限（chmod +x Cursor.AppImage）并运行。

### 2.2 登录和配置

首次启动 Cursor 时，您可以进行以下配置：

- **键盘快捷方式**：自定义快捷键以适应个人习惯。
- **语言**：设置 IDE 显示语言，可在规则文档中进一步调整 AI 语言行为。
![image](https://github.com/user-attachments/assets/e27fd886-3dc8-48a0-b8ce-2743d59b39cf)
- **代码库索引**：启用或禁用代码库索引以优化 AI 建议（详见 代码库索引）。
- **CLI 快捷方式**：设置 cursor 和 code 命令，方便从终端启动。
- **导入 VS Code 设置**：一键导入 VS Code 的扩展、主题、用户设置和键盘快捷方式。
![image](https://github.com/user-attachments/assets/636e015d-2ebf-45f6-ab02-119f463d1fd8)
- **数据隐私**：设置数据偏好，决定是否允许 AI 访问代码（详见 隐私页面）。
![image](https://github.com/user-attachments/assets/be0b9ebc-27d7-43bb-9f8f-3a87128d7a41)

### 2.3 界面介绍

Cursor IDE 的界面继承了 VS Code 的布局，熟悉 VS Code 的用户可以快速上手。主要组成部分包括：

- **侧边栏**：包含资源管理器（文件管理）、搜索、源控制、扩展等面板。

  ![image](https://github.com/user-attachments/assets/ef7fa839-7433-4016-a64b-5ceb18462e7d)
- **编辑器区域**：主区域，用于编写和编辑代码，支持多文件并排显示。
![image](https://github.com/user-attachments/assets/85266c5c-63af-47d8-ad5a-1d818e5c8835)
- **状态栏**：显示当前文件的状态，如语言、编码格式、行号等。
![image](https://github.com/user-attachments/assets/56a8fc41-f25f-4e90-a462-3d6cc4af925c)
- **活动栏**：位于侧边栏左侧，用于快速切换不同视图（如资源管理器、调试、扩展）。
![image](https://github.com/user-attachments/assets/94f29082-9f6f-451c-9b3b-23c8db39fe4e)

此外，Cursor IDE 在界面中集成了 AI 功能入口，如聊天窗口和 Tab 补全提示。主要组成部分包括：

- **智能补全框**：用于编写代码过程中，嵌入 AI 智能补全建议，支持快速代码补全。在编辑代码时，可以定位某个位置，或选中某段代码后，通过快捷键 Ctrl+k 触发
![录屏_选择区域_20250508201158](https://github.com/user-attachments/assets/026c76d6-b09c-4624-a339-1b17012ffe97)
- **AI辅助栏**：用于常规的 AI 辅助问答，最新 AI Agent 功能，传统的 AI Manual 功能。
![录屏_选择区域_20250508202313](https://github.com/user-attachments/assets/38108181-e5d3-48ba-9ed8-e9bc7e21d031)
- **MCP扩展**：近期 Cursor 版本新添加功能，结合热门的 MCP 协议，提供各类 MCP 服务扩展和调用功能。
![image](https://github.com/user-attachments/assets/3fc7a48d-4db9-41eb-a930-aaf2e9f2adbf)

---

## 3. 基本功能

### 3.1 文件管理

Cursor IDE 提供强大的文件管理功能，类似于 VS Code：

- **打开文件夹**：通过“文件 &gt; 打开文件夹”选择项目目录。
  
![image](https://github.com/user-attachments/assets/b78bfef6-945a-48da-b2f1-2ec8159e5910)
- **文件操作**：创建、重命名、删除文件或文件夹。

![image](https://github.com/user-attachments/assets/7baefbbe-8113-4f1a-8ce4-3cf80c73784f)
- **搜索**：使用快捷键 Ctrl/Cmd + T 或侧边栏搜索功能快速定位文件或代码。

![image](https://github.com/user-attachments/assets/d1574fcb-732c-49b7-9c0f-912d852d3d2d)
- **工作区管理**：支持多工作区，方便管理多个项目。

![image](https://github.com/user-attachments/assets/848251e6-f179-4bf3-96b8-a0edbc8750be)

### 3.2 代码编辑

代码编辑功能包括：

- **语法高亮**：支持多种编程语言，自动高亮代码结构。

![image](https://github.com/user-attachments/assets/444586b7-6370-45ed-b1aa-57edbf46233d)
- **自动缩进**：根据语言规则自动调整缩进。

![image](https://github.com/user-attachments/assets/d7223046-e873-4ef1-8ce3-88455f05b1f3)
- **代码折叠**：折叠函数或代码块以提高可读性。

![image](https://github.com/user-attachments/assets/8f663137-c61c-4c46-a7c3-fb98f6562c17)
- **多光标编辑**：使用 Alt + 鼠标点击 或 Ctrl/Cmd + D 同时编辑多处。
  
![录屏_选择区域_20250508204640](https://github.com/user-attachments/assets/44fd92e1-a03c-4c2d-a7c5-7b94769999fa)

### 3.3 代码补全

除了 AI 驱动的智能补全（见第 4.1 节），Cursor IDE 还提供标准的代码补全功能，基于语言服务器协议（LSP），支持变量、函数和模块的自动提示。

### 3.4 代码导航

代码导航功能帮助开发者快速定位和理解代码：

- **转到定义**：右键点击变量或函数，选择“转到定义”或使用 F12。
  
![录屏_选择区域_20250508205251](https://github.com/user-attachments/assets/a2c035b6-03cb-4410-81a1-22e53bc8af89)
- **查找引用**：使用 Shift + F12 查看变量或函数的所有引用。
  
![录屏_选择区域_20250508205356](https://github.com/user-attachments/assets/8c99b7fe-31b6-41aa-9e69-c82d8a55a074)
- **符号搜索**：通过 Ctrl/Cmd + T 搜索项目中的符号（如类、函数）。
  
![录屏_选择区域_20250508205520](https://github.com/user-attachments/assets/8ac45979-c675-41b5-97f3-3cc0b8a42d29)
- **面包屑导航**：编辑器顶部显示文件结构，方便跳转。
  
![image](https://github.com/user-attachments/assets/4ec32d6d-5858-4ae3-97be-3112dae8923e)

---

## 4. AI 功能

### 4.1 智能代码补全

Cursor Tab 是 Cursor IDE 的核心 AI 功能，类似于 GitHub Copilot，但更强大。它由自定义模型驱动，能建议多行代码并修改现有代码。

**功能描述**：

- 建议范围覆盖当前行上方一行到下方两行。
- 支持插入新代码或修改现有代码，显示为灰色文本（插入）或 diff 弹出窗口（修改）。
- 根据最近更改和 linter 错误提供上下文相关建议。
- 可以自定义模型（最优选模型为claude-sonnet-3.7）（插图）

**使用方法**：

- **接受建议**：按 Tab。
- **拒绝建议**：按 Esc 或继续输入。
- **逐词接受**：按 Ctrl/Cmd + →。
- **开关功能**：通过状态栏右下角的“Cursor Tab”图标启用/禁用。
- **自定义快捷键**：在 设置 &gt; 键盘快捷方式 中搜索 Accept Cursor Tab Suggestions。
- **禁用注释触发**：在 Cursor 设置 &gt; Tab 完成 中取消选中“在注释中触发”。

**限制**：

- 免费用户首次注册每月可获得 50 次高级建议和 200 次普通建议。
- Pro 和 Business 计划用户享受无限建议。

### 4.2 代码生成

Cursor IDE 的 Composer 功能允许用户通过自然语言描述生成代码。例如，您可以输入“创建一个 React 登录页面”，Composer 将生成包含必要组件和样板的代码。此外，聊天功能也支持生成代码片段。

### 4.3 代码库理解

通过代码库索引功能，Cursor IDE 的 AI 可以分析整个项目结构，理解文件之间的关系，从而提供更准确的代码建议和查询结果。用户可在首次启动时启用索引，或在设置中手动调整。

### 4.4 与 AI 聊天

聊天功能允许用户在 IDE 内与 AI 对话，适用于：

- **代码解释**：选择代码片段，询问其功能或逻辑。
- **调试帮助**：描述错误，获取修复建议。
- **重构建议**：请求优化代码的替代写法。
- **文档查询**：使用 @ 符号引用特定文档（如 @PyTorch）。

操作方法：

- 打开聊天面板（通常在侧边栏）。（插图）
- 输入问题或选择代码后提问。（插图）
- 使用 @ 符号添加上下文（如文件或文档）。（插图）

### 4.5 在终端中使用 AI

Cursor IDE 支持在集成终端中使用 AI，例如：

- **生成命令**：输入自然语言描述，AI 生成对应的终端命令。（插图）
- **解释输出**：选择终端输出，请求 AI 解释其含义。（插图）

此功能需在设置中启用，具体操作可参考 官方文档。

---

## 5. 高级功能

### 5.1 自定义设置

用户可以自定义以下设置：

- **键盘快捷方式**：通过 设置 &gt; 键盘快捷方式 调整。
- **主题**：选择深色、浅色或其他 VS Code 兼容主题。
- **AI 行为**：通过 .cursorrules 文件定义 AI 的响应规则（详见 规则文档）。扩展rules的解释
- **语言偏好**：设置 AI 的语言风格或代码格式。

### 5.2 扩展和插件

Cursor IDE 完全兼容 VS Code 的扩展生态，用户可以通过扩展市场安装：

- 语言支持扩展（如 Python、JavaScript）。
- 调试工具。
- 格式化工具（如 Prettier）。

安装方法：

1. 打开侧边栏的“扩展”面板。
2. 搜索并安装所需扩展。
3. 重启 IDE 以应用更改。

### 5.3 团队协作

Cursor IDE 支持团队协作功能，包括：

- **代码共享**：通过链接分享代码片段。
- **实时协同编辑**：允许多人同时编辑同一文件（需 Pro 或 Business 计划）。
- **评论和反馈**：在代码中添加注释，方便团队沟通。

具体设置需参考 官方文档。

### 5.4 版本控制

Cursor IDE 集成 Git，支持以下操作：

- **提交**：通过源控制面板提交更改，AI 可生成提交消息（点击“魔法棒”图标）。（插图）
- **分支管理**：创建、切换或合并分支。
- **冲突解决**：使用内置工具解决合并冲突。

此外，AI 驱动的“错误查找”功能（通过 Ctrl/Cmd + Shift + P 输入 bug finder）可比较更改与主分支，识别潜在错误。

---

## 6. 最佳实践

### 6.1 提高开发效率的技巧

- **利用 Tab 补全**：在编写重复性代码时，优先使用 Tab 接受 AI 建议。
- **善用聊天功能**：遇到复杂问题时，通过聊天窗口快速获取解决方案。
- **使用 Composer 原型开发**：快速生成应用原型，验证想法。
- **定期更新索引**：确保代码库索引最新，以提高 AI 建议的准确性。
- **自定义规则**：通过 .cursorrules 文件优化 AI 的响应风格。

### 6.2 常见问题和解决方法

以下是一些常见问题及解决方法：

- **AI 建议不准确**：检查代码库索引是否启用，或调整 .cursorrules 文件。
- **安装失败**：确保系统满足最低要求，参考 安装指南。
- **扩展不兼容**：尝试更新扩展或联系支持。
- **AI 功能不可用**：检查网络连接或订阅状态。

详细解决方案请参考 故障排除指南。

---

## 注意事项

- **版本更新**：Cursor IDE 定期更新，建议保持最新版本以获取新功能和修复。
- **隐私模式**：启用隐私模式可确保代码不存储在远程服务器，适合敏感项目。
- **免费与付费**：免费用户受限于 2000 次 AI 建议，Pro 和 Business 计划提供无限使用和其他高级功能。

