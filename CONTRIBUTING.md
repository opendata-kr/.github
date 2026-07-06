# 기여 가이드

opendata-kr에 기여를 고려해 주셔서 고맙습니다. 작은 오타 수정부터 새 서비스 도구 추가까지 모두 환영합니다.

처음이라 확신이 서지 않아도 괜찮습니다. 그냥 물어보시거나, 일단 이슈나 PR을 올리셔도 됩니다. 최악의 경우라야 무언가를 고쳐 달라는 정중한 요청을 받는 정도입니다.

## 구조

opendata-kr은 data.go.kr 서비스마다 별도 리포로 도구를 관리합니다. 리포명과 패키지명은 `<service-slug>-mcp` 규약을 따릅니다. 예: `narajangteo-bid-mcp`, `@opendata-kr/narajangteo-bid-mcp`.

## 기여 유형별 경로

### 1. 기존 도구의 버그 수정, 문서 개선

해당 `<service>-mcp` 리포에서 진행합니다.

1. 리포를 포크하고 브랜치를 만듭니다.
2. 변경 후 테스트를 통과시킵니다.
3. PR을 엽니다. PR 템플릿의 항목을 채워 주세요.

### 2. 새 data.go.kr 서비스 도구 추가

1. 대상 서비스를 [Discussions](https://github.com/orgs/opendata-kr/discussions)에 먼저 제안하거나 기존 제안을 확인합니다(중복 방지).
2. 새 리포를 표준 구조로 시작합니다. 기존 도구 리포 하나를 참고 골격으로 삼으세요.
   - 루트 `server.json` 의 `name`, `description`, `packages`, `environmentVariables` 를 정확히 기술합니다.
   - 서비스키 같은 시크릿은 `isSecret: true`, `isRequired: true` 로 표기합니다.
   - 원본 data.go.kr API 문서 링크를 README에 남깁니다.
3. 최소 하나의 동작 예제와 테스트를 포함합니다.
4. 리포를 opendata-kr 조직에 만드는 것은 메인테이너가 도와드립니다. [Discussions](https://github.com/orgs/opendata-kr/discussions)로 알려주세요.

## 표준 규약 (반드시 지킬 것)

- 리포명, 패키지명: `<service-slug>-mcp`, `@opendata-kr/<service-slug>-mcp`. 예외 없음.
- 라이선스: 모든 코드 기여는 Apache-2.0 으로 제공됩니다. PR을 여는 것으로 이에 동의하는 것으로 봅니다.
- 커밋: 명확한 메시지. 하나의 PR은 하나의 논리적 변경.

## 개발 환경

- Node.js: 각 리포의 `.nvmrc` 버전 (`nvm use`)
- 패키지 매니저: pnpm

```bash
pnpm install
pnpm test
pnpm build
```

## 도움이 필요하면

[SUPPORT.md](SUPPORT.md) 를 참고하세요. 막히면 [Discussions](https://github.com/orgs/opendata-kr/discussions)에 편하게 질문해 주세요.
