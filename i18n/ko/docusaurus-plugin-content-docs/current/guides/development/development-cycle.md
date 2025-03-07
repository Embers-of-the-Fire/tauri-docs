---
sidebar_position: 2
---

import Command from '@theme/Command'

# 개발 주기

### 1. 개발 서버 시작

이제 모든 것이 설정되었으므로 UI 프레임워크 또는 번들러에서 제공하는 애플리케이션 개발 서버를 시작해야 합니다(물론, 둘 중 하나를 사용한다고 가정).

:::note

모든 프레임워크에는 자체 개발 도구가 있습니다. 모든 내용을 다루거나 최신 정보로 갱신하는 것은 이 문서의 범위를 밖입니다.
:::

### 2. Tauri 개발 윈도우 시작

<Command name="dev" />

이 명령을 처음 실행하면 Rust 패키지 관리자가 필요한 모든 패키지를 다운로드하고 빌드하는 데 몇 분이 소요됩니다. 이들은 캐시되기 때문에 코드만 재빌드하면 되므로 후속 빌드가 훨씬 더 빠릅니다.

Rust가 빌드를 완료하면 Webview가 열리고 웹 앱이 표시됩니다. 웹 앱을 변경할 수 있으며 도구에서 지원하는 경우, WebView는 브라우저처럼 자동으로 업데이트됩니다. Rust 파일을 변경하면 자동으로 다시 빌드되고 앱이 자동으로 다시 시작됩니다.

:::info Cargo.toml 및 소스 제어 정보

프로젝트 저장소에서 "src-tauri/Cargo.toml"과 함께 "src-tauri/Cargo.lock"을 git에 커밋해야 합니다. 왜냐하면 Cargo는 결정된 빌드를 제공하기 위해 잠금 파일을 사용하기 때문입니다. 따라서, 모든 애플리케이션의 Cargo.lock을 체크인하는 것이 좋습니다. 단, "src-tauri/target" 폴더 또는 그 내용을 커밋하면 안 됩니다.

:::
