# ValUM

> **Official Forum / 官方论坛**: https://discord.gg/qslab

## Languages

[English](#en) · [中文](#zh)

<a id="en"></a>
## English

### Project Overview

`ValUM` is a compact Windows C++ project centered on a single primary source root: `Mirage/`.

The root stays minimal, while the project body, bundled support code, and dependency trees are grouped under `Mirage/`. Local build output also remains close to the source tree.

### What This Project Does

At a high level, `ValUM` organizes one native C++ project tree around three main concerns:

- runtime-facing logic under `Mirage/game/`
- overlay and UI-facing code under `Mirage/overlay/` and `Mirage/imgui/`
- support and dependency code under `Mirage/encryption/`, `Mirage/misc/`, and `Mirage/freetype/`

This makes the project useful as a compact example of how to keep:

- logic
- presentation
- utility code
- bundled dependencies

inside one predictable source root without splitting the repository into many top-level projects.

### High-Level Design

The project uses a simple layered organization inside one main tree:

1. `Mirage/game/` holds the main runtime-facing branches
2. `Mirage/overlay/` holds presentation-facing overlay code
3. `Mirage/imgui/` provides the immediate-mode UI support layer
4. `Mirage/encryption/` and `Mirage/misc/` provide support utilities
5. `Mirage/freetype/` provides bundled dependency support

The result is a compact source layout where the whole project can be understood by walking one main directory tree from logic to presentation to support layers.

### Root Directory Layout

The repository root contains:

- `Mirage/`
- `x64/`
- `README.md`

The project body starts inside `Mirage/`.

### `Mirage/` Top-Level Layout

The top-level directories inside `Mirage/` are:

- `encryption/`
- `freetype/`
- `game/`
- `imgui/`
- `misc/`
- `overlay/`

This single top-level tree defines the whole project structure.

### `Mirage/game/`

`Mirage/game/` is the main runtime-facing subtree.

Its visible first-level directories are:

- `memory/`
- `sdk/`
- `threads/`
- `unreal/`

This gives `Mirage/game/` an internal split between:

- memory-related code
- SDK-related code
- threading-related code
- the `unreal/` branch

### `Mirage/overlay/`

`Mirage/overlay/` is the overlay-facing subtree.

Its visible first-level directory is:

- `menu/`

Its visible second-level directory is:

- `menu/blur/`

This makes the overlay area more specific than a generic drawing folder. It includes a menu subtree and a deeper `blur/` branch inside that menu area.

### `Mirage/imgui/`

`Mirage/imgui/` is the bundled UI/rendering support subtree included directly with the project.

### `Mirage/encryption/`

`Mirage/encryption/` is a utility/support subtree kept separate from both the runtime logic area and the rendering/UI area.

### `Mirage/misc/`

`Mirage/misc/` is the general support subtree for code that does not belong to one core branch.

### `Mirage/freetype/`

`Mirage/freetype/` is the bundled font/rendering dependency subtree.

Its visible next-level structure includes:

- `include/`
- `win64/`

Inside `include/`, the visible nested directory includes:

- `freetype/`

This indicates that the project carries a locally embedded FreeType-style support tree directly in the repository.

### Project Organization

The project is easiest to read as one main source root with several functional layers:

- `Mirage/game/`: runtime logic
- `Mirage/overlay/`: overlay presentation
- `Mirage/imgui/`: UI support
- `Mirage/encryption/`: utility support
- `Mirage/misc/`: general helpers
- `Mirage/freetype/`: bundled dependency support

The single-root layout keeps the project compact and makes navigation predictable.

### Build and Output Footprint

The root-level `x64/` directory stores local native build output.

This keeps the project close to a working Windows C++ development tree instead of a source-only snapshot.

### Recommended Reading Order

Recommended reading order:

1. `Mirage/game/`
2. `Mirage/game/memory/`
3. `Mirage/game/sdk/`
4. `Mirage/game/threads/`
5. `Mirage/game/unreal/`
6. `Mirage/overlay/`
7. `Mirage/overlay/menu/`
8. `Mirage/overlay/menu/blur/`
9. `Mirage/imgui/`
10. `Mirage/encryption/`
11. `Mirage/misc/`
12. `Mirage/freetype/`
13. `Mirage/freetype/include/`
14. `Mirage/freetype/win64/`

### Summary

`ValUM` is a compact single-root Windows C++ project with:

- a main project body under `Mirage/`
- a `game/` subtree split into `memory/`, `sdk/`, `threads/`, and `unreal/`
- an `overlay/` subtree with `menu/` and `menu/blur/`
- bundled UI support under `imgui/`
- bundled dependency support under `freetype/`
- local native build output under `x64/`

<a id="zh"></a>
## 中文

### 项目概览

`ValUM` 是一个以单一主源码根 `Mirage/` 为中心的紧凑型 Windows C++ 项目。

根目录保持简洁，项目主体、内置支持代码和依赖树都集中放在 `Mirage/` 中，本地构建输出也保持在靠近源码的位置。

### 项目作用

从工程层面看，`ValUM` 把一个原生 C++ 项目树围绕三类主要内容组织起来：

- `Mirage/game/` 下的运行时逻辑
- `Mirage/overlay/` 和 `Mirage/imgui/` 下的 overlay / UI 代码
- `Mirage/encryption/`、`Mirage/misc/`、`Mirage/freetype/` 下的支持与依赖代码

这种结构适合用来展示，怎样在一个可预测的主源码根里同时放好：

- 逻辑代码
- 呈现代码
- 工具代码
- bundled 依赖

而不把仓库拆成很多互相分离的顶层工程。

### 整体原理

项目在一棵主树内部采用简单的分层组织：

1. `Mirage/game/` 放主要运行时逻辑分支
2. `Mirage/overlay/` 放面向呈现的 overlay 代码
3. `Mirage/imgui/` 提供即时模式 UI 支持层
4. `Mirage/encryption/` 和 `Mirage/misc/` 提供辅助工具
5. `Mirage/freetype/` 提供 bundled 依赖支持

最终形成的是一套紧凑源码布局，沿着一棵主目录树，就能从逻辑层一路读到呈现层和支持层。

### 根目录结构

仓库根目录包含：

- `Mirage/`
- `x64/`
- `README.md`

项目主体从 `Mirage/` 开始。

### `Mirage/` 顶层结构

`Mirage/` 下的顶层目录包括：

- `encryption/`
- `freetype/`
- `game/`
- `imgui/`
- `misc/`
- `overlay/`

整个项目结构都由这一棵主树定义。

### `Mirage/game/`

`Mirage/game/` 是主要的运行时逻辑子树。

其可见一级目录包括：

- `memory/`
- `sdk/`
- `threads/`
- `unreal/`

因此 `Mirage/game/` 内部继续拆分为：

- 内存相关代码
- SDK 相关代码
- 线程相关代码
- `unreal/` 分支

### `Mirage/overlay/`

`Mirage/overlay/` 是 overlay 呈现子树。

其可见一级目录为：

- `menu/`

其可见二级目录为：

- `menu/blur/`

因此 overlay 区域不仅仅是一个泛化绘制目录，还包含菜单子树以及菜单内部更深一层的 `blur/` 分支。

### `Mirage/imgui/`

`Mirage/imgui/` 是直接随项目内置的 UI / 渲染支持子树。

### `Mirage/encryption/`

`Mirage/encryption/` 是工具/支持子树，并且与运行时逻辑区和渲染/UI 区分开。

### `Mirage/misc/`

`Mirage/misc/` 是通用支持子树，用于放置不属于某个核心分支的辅助代码。

### `Mirage/freetype/`

`Mirage/freetype/` 是内置的字体/渲染依赖子树。

其可见下一层结构包括：

- `include/`
- `win64/`

在 `include/` 内部，可见的嵌套目录包括：

- `freetype/`

这说明项目把 FreeType 风格的支持树直接放进了仓库。

### 项目组织方式

整个项目最适合按“一棵主树 + 多个功能层”来理解：

- `Mirage/game/`：运行时逻辑
- `Mirage/overlay/`：overlay 呈现
- `Mirage/imgui/`：UI 支持
- `Mirage/encryption/`：工具支持
- `Mirage/misc/`：通用辅助
- `Mirage/freetype/`：内置依赖支持

单主树布局让整个项目保持紧凑，也让导航方式更稳定。

### 构建与输出痕迹

根目录中的 `x64/` 用于保存本地原生构建输出。

这让项目保持了真实 Windows C++ 开发工作树的形态，而不是只保留源码的快照。

### 阅读建议

推荐按下面顺序阅读：

1. `Mirage/game/`
2. `Mirage/game/memory/`
3. `Mirage/game/sdk/`
4. `Mirage/game/threads/`
5. `Mirage/game/unreal/`
6. `Mirage/overlay/`
7. `Mirage/overlay/menu/`
8. `Mirage/overlay/menu/blur/`
9. `Mirage/imgui/`
10. `Mirage/encryption/`
11. `Mirage/misc/`
12. `Mirage/freetype/`
13. `Mirage/freetype/include/`
14. `Mirage/freetype/win64/`

### 总结

`ValUM` 是一个紧凑的单主树 Windows C++ 项目，包含：

- 位于 `Mirage/` 下的主项目主体
- 拆分为 `memory/`、`sdk/`、`threads/`、`unreal/` 的 `game/` 子树
- 包含 `menu/` 与 `menu/blur/` 的 `overlay/` 子树
- 位于 `imgui/` 的内置 UI 支持
- 位于 `freetype/` 的内置依赖支持
- 位于 `x64/` 的本地原生构建输出
