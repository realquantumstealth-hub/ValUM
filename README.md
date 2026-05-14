# ValUM

## Languages

[English](#en) · [中文](#zh) · [日本語](#ja) · [한국어](#ko) · [Русский](#ru) · [Українська](#uk) · [Tiếng Việt](#vi)

<a id="zh"></a>
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

由于部分密钥、证书、可执行链路、绕过/注入成品等属敏感信息不方便在 GitHub 上公开，需要或想交流的同伴可以联系我们官方 Discord 进行深入探讨。

---

<a id="en"></a>
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

Some keys, certificates, executable chains, and bypass/injection deliverables are sensitive and are not suitable for public release on GitHub. For deeper discussion, please contact our official Discord.

---

<a id="ja"></a>
## 日本語

`ValUM` は `Mirage/` を中心に構成されたアンチチート研究プロジェクトです。メモリアクセス、オーバーレイ UI、スレッド管理、機能モジュール構成を含みます。

構成例：

- `Mirage/game/`：ゲームデータアクセスと SDK ロジック
- `Mirage/overlay/`：可視化・操作レイヤー
- `Mirage/imgui/`：UI と描画コンポーネント
- `Mirage/encryption/`：文字列・インポート処理などの基盤機能
- `x64/`：ビルド成果物（私有アーカイブ推奨）

### 研究目的

- スレッド分担と描画パイプラインの設計研究
- メモリアクセス抽象化とモジュール境界設計
- 大規模ヘッダー資産の保守性評価

### コンプライアンス

本プロジェクトは防御研究と技術交流のみを目的とします。

鍵・証明書・実行チェーン・バイパス/インジェクション成果物などの機微情報は GitHub で公開しません。詳細は公式 Discord へご連絡ください。

---

<a id="ko"></a>
## 한국어

`ValUM`은 `Mirage/` 디렉터리를 중심으로 구성된 안티치트 연구 프로젝트입니다. 메모리 접근, 오버레이 UI, 스레드 관리, 모듈 구성 등을 포함합니다.

구성 예시:

- `Mirage/game/`: 게임 데이터 접근 및 SDK 로직
- `Mirage/overlay/`: 시각화/상호작용 계층
- `Mirage/imgui/`: UI 및 렌더링 컴포넌트
- `Mirage/encryption/`: 문자열/임포트 처리 등 기반 기능
- `x64/`: 빌드 산출물 디렉터리(비공개 보관 권장)

### 연구 목표

- 스레드 작업 분리와 렌더링 파이프라인 구조 연구
- 메모리 접근 추상화 및 모듈 경계 설계
- 대형 헤더 자산 관리와 유지보수성 연구

### 준수 및 범위

본 프로젝트는 방어 연구 및 기술 교류 목적에 한해 사용됩니다.

키, 인증서, 실행 체인, 바이패스/인젝션 결과물 등 민감 정보는 GitHub에 공개하지 않습니다. 자세한 논의는 공식 Discord로 문의해 주세요.

---

<a id="ru"></a>
## Русский

`ValUM` — исследовательский anti-cheat проект, построенный вокруг каталога `Mirage/`. Включает доступ к памяти, overlay/UI, управление потоками и организацию модулей.

Пример структуры:

- `Mirage/game/`: доступ к игровым данным и SDK-логика
- `Mirage/overlay/`: слой визуализации и взаимодействия
- `Mirage/imgui/`: UI и компоненты рендеринга
- `Mirage/encryption/`: базовые утилиты (строки, импорт и т. д.)
- `x64/`: каталог сборочных артефактов (рекомендуется хранить приватно)

### Цели исследования

- Исследование потоковой организации задач и рендер-пайплайна
- Исследование абстракции доступа к памяти и границ модулей
- Исследование управляемости крупных header-ресурсов

### Соответствие и ограничения

Проект предназначен для defensive-исследований и инженерного обмена.

Ключи, сертификаты, исполняемые цепочки и готовые bypass/injection материалы не публикуются на GitHub. Для детального обсуждения используйте официальный Discord.

---

<a id="uk"></a>
## Українська

`ValUM` — це дослідницький anti-cheat проєкт, побудований навколо каталогу `Mirage/`. Містить доступ до пам’яті, overlay/UI, керування потоками та організацію модулів.

Приклад структури:

- `Mirage/game/`: доступ до ігрових даних і SDK-логіка
- `Mirage/overlay/`: шар візуалізації та взаємодії
- `Mirage/imgui/`: UI і компоненти рендерингу
- `Mirage/encryption/`: базові утиліти (рядки, імпорт тощо)
- `x64/`: каталог артефактів збірки (рекомендовано зберігати приватно)

### Мета дослідження

- Дослідження потокової організації задач і рендер-пайплайна
- Дослідження абстракції доступу до пам’яті й меж модулів
- Дослідження підтримуваності великих header-ресурсів

### Відповідність і межі

Проєкт призначено для defensive-досліджень та інженерного обміну.

Ключі, сертифікати, виконувані ланцюги та готові bypass/injection матеріали не публікуються на GitHub. Для детального обговорення використовуйте офіційний Discord.

---

<a id="vi"></a>
## Tiếng Việt

`ValUM` là dự án nghiên cứu anti-cheat xoay quanh thư mục `Mirage/`. Bao gồm truy cập bộ nhớ, overlay/UI, điều phối luồng và tổ chức mô-đun.

Ví dụ cấu trúc:

- `Mirage/game/`: truy cập dữ liệu game và logic SDK
- `Mirage/overlay/`: lớp hiển thị và tương tác
- `Mirage/imgui/`: UI và thành phần render
- `Mirage/encryption/`: tiện ích nền tảng (chuỗi, import, v.v.)
- `x64/`: thư mục output build (khuyến nghị lưu trữ riêng tư)

### Mục tiêu nghiên cứu

- Nghiên cứu tổ chức tác vụ theo luồng và pipeline render
- Nghiên cứu trừu tượng hóa truy cập bộ nhớ và ranh giới mô-đun
- Nghiên cứu khả năng bảo trì với tài nguyên header lớn

### Tuân thủ và phạm vi

Dự án chỉ phục vụ nghiên cứu phòng thủ và trao đổi kỹ thuật.

Một số khóa, chứng chỉ, chuỗi thực thi và sản phẩm bypass/injection là thông tin nhạy cảm nên không công khai trên GitHub. Nếu cần trao đổi sâu hơn, vui lòng liên hệ Discord chính thức của chúng tôi.
