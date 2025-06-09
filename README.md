## 📁 terraform-ui-runner (WIP)

> Terraform 명령을 UI에서 실행하고, 리소스 변경 내역을 시각적으로 확인하는 웹 기반 도구  
> 개발자 없이도 웹에서 인프라를 직접 관리할 수 있는 인터페이스 제공

### 🔧 기술스택
React, TypeScript, Node.js, Terraform, AWS Lambda, S3, GitHub Actions

### 🚀 주요 기능
- 🖥 Terraform 명령 실행 (plan/apply/destroy) 트리거 UI 제공
- 📄 상태 파일 관리 및 변경 내역 시각화
- 📋 입력 파라미터 기반 모듈 자동 매핑
- 🧪 로컬 개발 환경 + GitHub Actions 배포 환경 분리

### 🎯 핵심 성과
- Terraform 명령어 추상화 → 사용자 UI로 변환 설계
- 인프라 변경의 시각화 흐름을 웹 앱으로 구성
- 사내 DevOps 워크플로우에 바로 연동 가능한 구조 설계

### terraform-ui-runner 아키텍처
```
+-------------+       +----------------+
|   사용자    | <---> |  React UI      |
+-------------+       +----------------+
                             |
                             v
                   +----------------------+
                   | Node.js Command API  |
                   +----------------------+
                             |
                             v
                    +---------------------+
                    | Terraform CLI (로컬)|
                    +---------------------+
                             |
                             v
                 +-----------------------------+
                 | .tfstate 상태 → 변경 요약 UI |
                 +-----------------------------+
                             |
                             v
                    +------------------+
                    | GitHub Actions CI|
                    +------------------+
```

📌 특징 요약
사용자 UI → Terraform 명령 실행
plan, apply, destroy 버튼으로 조작
리소스 변경 시 차이(diff)를 UI에 시각화
GitHub Actions로 버전 관리 및 배포 자동화

### 🔗 링크
- [🔗 GitHub Repository](https://github.com/kenneth-kang/terraform-ui-runner)

