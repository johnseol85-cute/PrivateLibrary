# 08. CLAUDE.md 조사: 무엇을 넣는가, 인문·신학 연구자들은 무엇을 올렸나

> 조사일 2026-10-08. 각 저장소의 CLAUDE.md 원문을 직접 내려받아 목차와 핵심 절을 읽었다. 별(★) 수는 같은 날 GitHub 페이지 기준.

## 1. CLAUDE.md의 일반 원칙

CLAUDE.md는 **매 세션 시작 때 Claude가 통째로 읽는 파일**이다. 그래서:

| 원칙 | 이유 |
|---|---|
| **짧게** (200줄 이하 권장, 60줄 수준으로 유지하는 팀도 있음) | 매번 읽으므로 길수록 토큰을 쓰고, 지시를 지키는 정도도 떨어짐 |
| **코드를 봐서는 알 수 없는 것만** | 폴더 구조·명령은 코드에서 알 수 있지만, "왜 이렇게 하는지"와 금지 사항은 알 수 없음 |
| **규칙마다 이유를 붙임** | 이유가 없으면 무시되기 쉬움 |
| **금지 사항엔 "대신 이렇게"를 같이** | "하지 마라"만 있으면 엉뚱한 대안을 고름 |
| **세부는 다른 문서로 연결** | 긴 내용은 `docs/`에 두고 CLAUDE.md에는 링크만 |
| **진행 중 할 일 목록은 넣지 않음** | 자주 바뀌는 것은 별도 문서(진행 현황)로 |

## 2. 인문·신학 분야 저장소 사례

| 저장소 | ★ | 성격 | CLAUDE.md에서 배울 점 |
|---|---:|---|---|
| [pedrohcgs/claude-code-my-workflow](https://github.com/pedrohcgs/claude-code-my-workflow) | 1.6k | 에모리대 경제학 교수의 학술 작업 템플릿(인문 아님, 학술용으로 가장 유명) | **범위 규율**: "요청한 것만 한다. 그 밖의 것은 끝에 제안으로만." / 계획 먼저, 작업 후 검증 / 기억은 대화가 아니라 저장소 문서에 |
| [worlyung/exegete](https://github.com/worlyung/exegete) | 23 | **한국어** Claude 성경 주해 도구 (STEPBible TAGNT·TAHOT, 개역한글) | **환각 방지 철칙**: 본문은 데이터에서만 인용, 기억으로 인용 금지 / 원어·스트롱 번호가 불확실하면 `[확인 필요]` / 저작권 본문(개역개정·NA28)은 넣지 않음 / 히브리어(오른쪽→왼쪽)는 고정폭 도표에 넣지 않음 |
| [authenticwalk/mybibletoolbox-code](https://github.com/authenticwalk/mybibletoolbox-code) | — | AI용 성경 주석 데이터 구축 | **문제 정의를 명시**: "AI는 잘 안 알려진 본문에서 정확도보다 자신감이 앞선다" → 그래서 데이터에 근거하게 함 / 신학 관점을 명시 / 계획은 `plans/` 폴더에 |
| [davebream/claude-of-alexandria](https://github.com/davebream/claude-of-alexandria) | 7 | 개혁주의 성경 연구 플러그인 | **신학적 안전장치 표**(위반 사례 → 대신 할 일) / "흔한 핑계" 표로 지름길 차단. 다만 430줄로 길다 |
| [leiverkus/research-superpowers](https://github.com/leiverkus/research-superpowers) | 2 | 신학·성서고고학·디지털 인문학 연구 흐름 | 해석학적 연구와 정량 연구를 구분 / 출처 검증으로 "기억으로 쓴 인용" 차단 |
| [ronanguilloux/skill-theo](https://github.com/ronanguilloux/skill-theo) | — | 가톨릭 주해 스킬 | 방법론별(PaRDeS, 알터, 메이네)로 스킬을 분리해 섞이지 않게 함 |

**공통점**: 신학·원어 분야 저장소는 모두 **"본문과 원어 정보는 반드시 데이터에서, 기억으로 쓰지 않는다"**를 가장 강한 규칙으로 둔다. AI가 성경 구절·원어 뜻을 그럴듯하게 지어내는 것이 이 분야의 가장 큰 위험이기 때문이다.

## 3. 이 프로젝트 CLAUDE.md에 넣을 항목 (제안)

| 항목 | 내용 | 현재 |
|---|---|---|
| 프로젝트 한 줄 정의 | 개인용 성경 원전 탐구 라이브러리 | ✅ 있음 |
| 작업 규칙 | 기획 먼저, 한국어, 범위 확대 금지, 단계마다 보고 | ✅ 있음 |
| **본문 정확성 철칙** | 성경 본문·원어 정보는 데이터에서만. 기억으로 쓰지 않음. 불확실하면 `[확인 필요]` | ❌ 추가 필요 |
| **라이선스 철칙** | 수집 전에 LICENSE 원문 확인, NC 자료와 저작권 본문(개역개정·NA28·BHS) 제외 | △ 일부 있음 |
| 데이터 기준 | 본문 기준 = WLC(OSHB)·SBLGNT, 좌표 = OSIS | ❌ 추가 필요 (07 링크) |
| 원어 표기 | 히브리어 RTL 처리, 유니코드 정규화 등 | ❌ 구현 시작 때 |
| 폴더 구조·명령 | 수집·정제·빌드 명령 | ❌ 구현 시작 때 |
| 진행 보고 형식 | 한 일 / 생긴 것 / 확인할 것 | ❌ 추가 필요 |
| 효율 규칙 | 단계마다 새 대화, 진행 상황은 문서에 남김 | ❌ 추가 필요 |
| 문서 지도 | `docs/` 링크 목록 | ✅ 있음 |

길이는 **100줄 이내**로 유지하고, 세부는 `docs/`로 연결한다.

## 출처

- CLAUDE.md 일반 원칙: [techsy.io](https://techsy.io/en/blog/claude-md-best-practices) · [lowcode.agency](https://www.lowcode.agency/blog/claude-md-guide) · [dsebastien.net](https://www.dsebastien.net/claude-code-memory/) · [shanraisshan/claude-code-best-practice](https://github.com/shanraisshan/claude-code-best-practice/blob/main/CLAUDE.md)
- 학술 템플릿: [ericluo04/claude-academic-workflow](https://github.com/ericluo04/claude-academic-workflow) · [flonat/flonat-research](https://github.com/flonat/flonat-research)
- 신학: [GitHub topic: biblical-studies](https://github.com/topics/biblical-studies) · [cys-claude-sermon-skills](https://github.com/choiyoungwan1207-star/cys-claude-sermon-skills)
