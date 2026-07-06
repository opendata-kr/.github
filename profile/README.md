<!--
  이 파일은 opendata-kr 조직의 공개 프로필입니다.
  경로 규칙(GitHub 공식): 반드시 `<org>/.github` 리포의 `profile/README.md` 여야 org Overview 탭에 렌더됩니다.
  링크는 절대 URL을 씁니다. 프로필 README의 상대경로는 렌더 위치에 따라 깨질 수 있습니다.
  배너 이미지를 넣으려면 아래 주석을 해제하고 profile/images/banner.png 를 추가하세요.
-->
<!-- <p align="center"><img src="images/banner.png" alt="opendata-kr" width="640"></p> -->

<h1 align="center">opendata-kr</h1>

<p align="center">
  <strong>공공데이터포털(data.go.kr) OpenAPI를 위한 표준 AI 도구 모음</strong><br>
  <em>Standardized AI tools for Korea's public data OpenAPIs.</em>
</p>

<p align="center">
  <a href="https://www.npmjs.com/org/opendata-kr"><img alt="npm" src="https://img.shields.io/badge/npm-%40opendata--kr-CB3837?logo=npm"></a>
  <a href="https://github.com/opendata-kr/.github/blob/main/LICENSE"><img alt="license" src="https://img.shields.io/badge/license-MIT-blue"></a>
  <a href="https://github.com/opendata-kr/.github/discussions"><img alt="discussions" src="https://img.shields.io/badge/community-Discussions-5865F2?logo=github"></a>
</p>

> [!NOTE]
> opendata-kr은 공공데이터포털(data.go.kr)과 무관한 독립 오픈소스 프로젝트입니다.
> 정부기관이 운영하지 않으며, data.go.kr의 공개 OpenAPI를 커뮤니티가 표준 도구로 감쌉니다.

---

## 무엇을 하나요

data.go.kr에는 수천 개의 공공 OpenAPI가 있지만 스펙, 인증, 응답 포맷이 서비스마다 제각각입니다.
opendata-kr은 각 서비스를 하나의 표준 AI 도구 규격(MCP 서버, `server.json`)으로 통일해, AI 에이전트와 개발자가 바로 쓰게 합니다.

## 시작하기

```bash
npx -y @opendata-kr/<service>-mcp
```

전체 도구는 [조직 리포 목록](https://github.com/orgs/opendata-kr/repositories)에서 찾을 수 있습니다.

## 리포지토리 구조

각 data.go.kr 서비스는 **별도의 리포지토리**입니다. 이름만 알면 리포를 바로 찾을 수 있도록, 네이밍 규약은 `<service-slug>-mcp` 하나로 고정합니다.

- 예: [opendata-kr/narajangteo-bid-mcp](https://github.com/opendata-kr/narajangteo-bid-mcp) (나라장터 입찰공고정보서비스)

패키지는 `@opendata-kr/<service-slug>-mcp` 로 발행합니다. 각 도구 리포는 루트에 [`server.json`](https://modelcontextprotocol.io/registry/about)을 두어 자기 자신을 표준 기술하며, 서비스키 같은 시크릿은 `environmentVariables` 에 `isSecret: true` 로 표기합니다.

## 왜 opendata-kr인가

- 일관성: 서비스마다 다시 파악할 필요 없이 같은 규약으로 씁니다.
- AI 네이티브: 표준 MCP 도구라 Claude 같은 에이전트에 바로 연결됩니다.
- 투명성: 모든 코드가 공개되어 있어, 도구가 어떤 원본 API를 호출하는지 추적할 수 있습니다.

## 함께하기

- 마음에 드는 도구 리포에 Star를 눌러주세요
- 버그, 제안: 각 도구 리포의 이슈, 전체 논의는 [Discussions](https://github.com/opendata-kr/.github/discussions)
- 기여 방법: [CONTRIBUTING](https://github.com/opendata-kr/.github/blob/main/CONTRIBUTING.md), [행동 강령](https://github.com/opendata-kr/.github/blob/main/CODE_OF_CONDUCT.md), [거버넌스](https://github.com/opendata-kr/.github/blob/main/GOVERNANCE.md)

## 라이선스

MIT. 각 리포의 `LICENSE` 를 참조하세요.
보안 취약점은 공개 이슈 대신 [SECURITY](https://github.com/opendata-kr/.github/blob/main/SECURITY.md) 절차로 신고해 주세요.
