# 보안 정책

## 취약점 신고

opendata-kr의 보안을 진지하게 생각합니다. 취약점을 발견하면 **공개 이슈로 올리지 말아 주세요.**

다음 경로로 비공개 신고해 주세요.

1. GitHub의 [Private vulnerability reporting](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability) 사용 (해당 리포 Security 탭)
2. 또는 이메일: joojinhyun00@gmail.com

신고에는 가능하면 다음을 포함해 주세요.

- 영향받는 패키지와 버전
- 재현 절차
- 예상되는 영향

접수 후 확인 회신을 드리고, 수정 일정을 공유합니다.

## 서비스키와 시크릿 관련 주의

opendata-kr 도구는 data.go.kr **서비스키**를 사용합니다. 다음을 지켜 주세요.

- 서비스키를 코드, 커밋, 이슈, PR에 절대 포함하지 마세요.
- 각 도구는 서비스키를 `server.json` 의 `environmentVariables` 에 `isSecret: true` 로 선언합니다. 실제 값은 환경변수로만 주입합니다.
- 실수로 키를 노출했다면 data.go.kr에서 즉시 재발급하세요.

키 노출이 의심되는 도구를 발견하면 위 절차로 신고해 주세요.

## 지원 범위

opendata-kr은 data.go.kr OpenAPI를 감싸는 클라이언트 도구입니다. 원본 API 서버나 data.go.kr 플랫폼 자체의 보안 문제는 이 프로젝트가 처리할 수 없습니다. 해당 사안은 공공데이터포털에 직접 문의하세요.
