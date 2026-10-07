# 06. 데이터 소스: 히브리어·헬라어·한국어 (기초 주해 최소 세트)

> 라이선스는 2026-10-07 웹 검색 결과 기준이며 일부는 2차 자료다. **수집 전에 각 저장소의 LICENSE 파일과 파일 헤더로 재확인**한다.
> **2026-10-07 갱신:** 권위·채택 범위 기준의 핵심 세트와 원 저장소 LICENSE 직접 확인 결과는 [07](07-authoritative-sources.md) 참고 (SBLGNT=CC BY 4.0 확인, MorphGNT=CC BY-SA 3.0 확인).
> 판단: ✅ 1차 수집 / △ 나중에·비교용 / ⏸ 보류 / ❌ 제외

## 히브리어 구약

| 자료 | 내용 | 라이선스 | 판단 |
|---|---|---|---|
| OSHB (openscriptures/morphhb) | 레닌그라드 사본(WLC) + 원형 + 형태소 (OSIS) | WLC 본문 PD, 형태소 CC BY 4.0 | ✅ 핵심 본문 |
| UXLC (tanach.us) | 레닌그라드 사본 정밀 XML (최신 2.4, 2025-10) | "제한 없이 복사 가능" | ✅ 정밀 대조 |
| MACULA Hebrew (Clear Bible) | 구문 트리(절·구), 단어별 영어 뜻 | CC BY 4.0 | ✅ 구조·세부 분석 |
| STEPBible TAHOT | 형태소 + 이문 정보 | CC BY 4.0 (파일별 확인) | ✅ |
| MAM (Miqra according to the Masorah) | 알레포 사본 기반 독자용 판 | CC BY-SA | △ 비교 판본 |
| BHSA (ETCBC) | 정교한 언어학 DB | CC BY-NC 4.0 (+ 본문 저작권 DBG) | ⏸ 상업화 불가 |

## 헬라어 신약

| 자료 | 내용 | 라이선스 | 판단 |
|---|---|---|---|
| SBLGNT + 비평장치 (jjmccollum/sblgnt-tei) | 학술 비평본 + 이문 (TEI) | CC BY 4.0 | ✅ 핵심 본문 |
| MACULA Greek (Clear Bible) | 구문 트리, 형태소, 의미 영역 | CC BY 4.0 (영어 뜻=BSB, 의미 영역=UBS MARBLE은 별도 확인) | ✅ |
| STEPBible TAGNT | 형태소 + 판본 간 이문 표시 | CC BY 4.0 | ✅ |
| MorphGNT | SBLGNT 형태소 | CC BY-SA (확인 필요) | △ |
| Nestle 1904 | 옛 비평본 | PD | △ 비교 |
| IGNTP 사본 전사 | 사본 350여 개 TEI 전사 | CC BY | ⏸ 본문비평 심화 |
| OGNT (Eliran Wong) | — | CC BY-NC-SA | ❌ |
| THGNT (Tyndale House GNT) | — | 라이선스 확인 못 함 | ❌ (확인 전) |

## 사전

| 자료 | 라이선스 | 판단 |
|---|---|---|
| Abbott-Smith (헬라어, 1922, TEI) | PD | ✅ |
| BDB (openscriptures/HebrewLexicon) | CC BY 4.0 (확인 필요), 일부 미완 | ✅ |
| STEPBible TBESH / TBESG (간편 사전) | CC BY 4.0 | ✅ 빠른 뜻 표시 |

## 칠십인역 (보류)

- 디지털 Rahlfs: TLG/CATSS 계통 제한이 얽혀 상태 불분명.
- Swete (First1KGreek): CC BY-SA → 나중에 검토.

## 한국어 — 가장 큰 공백

| 층 | 공개 자료 | 해결 방법 |
|---|---|---|
| 절 번역 | **개역한글(1961)** — 2012년 저작권 만료로 알려짐(위키문헌 등 2차 자료) | 대한성서공회 공식 확인 후 사용. 개역개정·새번역 등은 저작권 보호 중 → 수록 안 함 |
| 단어별 한국어 뜻(원어 대역) | **공개 자료 없음** | MACULA·STEPBible 영어 뜻 + 사전 기반으로 **직접 생성 후 검수** |
| 문법 설명 | 없음 | 형태소 코드 → 한국어 문법 용어 **변환표 직접 제작** |

→ 원어 → 한국어 단어 대역과 한국어 문법 설명이 **이 프로젝트 고유의 자산**이 된다.

## 출처

- [SBL Greek New Testament (Wikipedia)](https://en.wikipedia.org/wiki/SBL_Greek_New_Testament) · [sblgnt-tei](https://github.com/jjmccollum/sblgnt-tei)
- [MACULA Greek](https://github.com/Clear-Bible/macula-greek) · [NuBerea MACULA Hebrew](https://huggingface.co/datasets/NuBerea/macula-hebrew-syntax)
- [STEPBible-Data](https://github.com/STEPBible/STEPBible-Data)
- [IGNTP open data](https://www.birmingham.ac.uk/news/2017/igntp-releases-open-data) · [OpenGNT](https://github.com/eliranwong/OpenGNT)
- [OSHB morphhb (fork)](https://github.com/ReneNyffenegger/morphhb) · [tanach.us (UXLC)](https://tanach.us/Pages/About.html) · [MAM (Wikisource)](https://en.wikisource.org/wiki/User:Dovi/Miqra_according_to_the_Masorah)
- [ETCBC BHSA README](https://github.com/ETCBC/bhsa/blob/v1.1.0/README.md)
- [Abbott-Smith TEI](https://github.com/translatable-exegetical-tools/Abbott-Smith) · [openscriptures HebrewLexicon](https://github.com/openscriptures/HebrewLexicon)
- [NuBerea Septuagint](https://huggingface.co/datasets/NuBerea/septuagint-analysis) · [ibiblio LXX 라이선스 논의](https://www.ibiblio.org/bgreek/forum/viewtopic.php?p=5499)
- [개역한글판 (위키문헌)](https://ko.wikisource.org/wiki/%EA%B0%9C%EC%97%AD%ED%95%9C%EA%B8%80%ED%8C%90) · [Mozilla discourse](https://discourse.mozilla.org/t/copyright-violation-issues-on-korean-sentences/122870)
