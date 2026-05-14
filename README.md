# ValUM

[中文](#中文说明) | [English](#english)

## 中文说明

`ValUM` 是一个以 `Mirage/` 为核心目录的反作弊研究工程样例，项目中包含内存访问、渲染界面、线程调度与功能模块组织等内容。

当前结构示例：

- `Mirage/game/`：游戏数据访问与 SDK 相关逻辑
- `Mirage/overlay/`：可视化与交互层
- `Mirage/imgui/`：UI 与渲染组件
- `Mirage/encryption/`：字符串与导入处理等基础能力
- `x64/`：构建产物目录（建议仅私有归档）

### 研究目标

- 研究线程化任务分工与渲染链路组织
- 研究内存访问封装与模块边界设计
- 研究大型头文件资源管理与工程可维护性

### 合规与边界

本项目仅用于防御研究与工程技术交流，不用于未授权用途。

**由于部分密钥、证书、可执行链路、绕过/注入成品等属敏感信息不方便在github上公开，需要或想交流的同伴可以联系我们官方discord进行深入探讨。**

---

## English

`ValUM` is an anti-cheat research project sample centered around the `Mirage/` directory, covering memory access, overlay/UI rendering, threading, and module organization.

Current structure example:

- `Mirage/game/`: game data access and SDK-related logic
- `Mirage/overlay/`: visualization and interaction layer
- `Mirage/imgui/`: UI and rendering components
- `Mirage/encryption/`: foundational utilities such as string/import handling
- `x64/`: build output directory (recommended for private archive only)

### Research Focus

- Threaded task organization and rendering pipeline structure
- Memory access abstraction and module boundary design
- Large-header asset management and maintainability

### Compliance & Boundaries

This project is for defensive research and engineering discussion only, and must not be used for unauthorized purposes.

**Some keys, certificates, executable chains, and bypass/injection deliverables are sensitive and are not suitable for public release on GitHub. If you need deeper discussion, please contact our official Discord.**


