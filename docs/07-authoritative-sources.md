# 07. 가장 많이 쓰이면서 권위 있는 원어 오픈 소스

> 조사일 2026-10-07. 라이선스는 **각 저장소의 LICENSE·README 원문을 직접 확인**했다(✔ 표시).
> "가장 많이 쓰인다"는 사용 통계가 공개되어 있지 않으므로, ① 만든 기관의 학문적 권위, ② 다른 주요 도구·데이터가 기반으로 삼는지(채택 범위), ③ 정리 목록(Nida Institute *Awesome Biblical Data*)에서의 위치로 판단했다.

## 0. 먼저 알아 둘 사실

학계에서 **가장 권위 있는 판본은 오픈 소스가 아니다.**

| 구분 | 학계 표준 판본 | 출판 | 오픈 여부 |
|---|---|---|---|
| 히브리어 구약 | BHS(비블리아 헤브라이카 슈투트가르텐시아), BHQ | 독일성서공회(DBG) | ❌ 저작권 보호 |
| 헬라어 신약 | NA28(네슬레-알란트 28판), UBS5 | 독일성서공회(DBG) | ❌ 저작권 보호 |

그래서 오픈 소스 쪽의 목표는 **"표준 판본과 같은 사본·같은 수준의 본문을 자유 라이선스로"** 얻는 것이다.

## 1. 히브리어 구약

| 순위 | 자료 | 권위(누가 만들었나) | 채택 범위 | 라이선스 |
|---|---|---|---|---|
| ★1 | **WLC (웨스트민스터 레닌그라드 사본)** + **OSHB 형태소** (`openscriptures/morphhb`) | 레닌그라드 사본 = **BHS와 같은 사본**. 본문은 웨스트민스터 히브리 연구소(J. Alan Groves Center) | 사실상 모든 오픈 히브리어 자료의 바탕. MACULA Hebrew·STEPBible TAHOT·Blue Letter Bible·eBible이 모두 이것을 씀 | 본문 PD, 원형·형태소 **CC BY 4.0** ✔ |
| ★2 | **UXLC** (tanach.us) | WLC의 후속 정밀판(최신 2.4, 2025-10). 사본 대조 수정 이력 공개 | MACULA Hebrew가 이 스냅샷을 사용 | "제한 없이 열람·복사 가능" (MACULA LICENSE에 인용) ✔ |
| ★3 | **STEPBible TAHOT** | **케임브리지 Tyndale House** 학자들 | STEPBible 사이트의 원어 데이터 | **CC BY 4.0** ✔ |
| 참고 | **ETCBC BHSA** | **암스테르담 자유대(VU) ETCBC**. 학술 연구용 히브리어 DB로는 가장 정교함(절·구·단어 구문) | 학술 연구(Text-Fabric, SHEBANQ)에서 가장 널리 쓰임 | **CC BY-NC 4.0** ✔ + 본문은 DBG 권리 → **상업화 불가** |

- TAHOT는 "OpenScriptures 경유 웨스트민스터 본문을 컬러 스캔으로 교정하고, 형태소는 ETCBC 분석을 OS 형식으로 변환"한 것 → **WLC 본문 + BHSA급 분석을 CC BY로** 얻는 길. ✔

## 2. 헬라어 신약

| 순위 | 자료 | 권위 | 채택 범위 | 라이선스 |
|---|---|---|---|---|
| ★1 | **SBLGNT** (`LogosBible/SBLGNT`) | **세계성서학회(SBL)** + Logos. 편집 **마이클 홈스**. 4개 비평본 비교로 확정, NA27과 다른 곳은 약 540곳 | 오픈 헬라어 신약의 표준. MorphGNT·MACULA Greek·STEPBible이 모두 포함 | **CC BY 4.0** ✔ (2022-12-19 변경. 그 전엔 자체 EULA였음) |
| ★2 | **MorphGNT** (`morphgnt/sblgnt`) | 제임스 토버(James Tauber). "최초의 고품질 오픈 GNT 형태소" | 형태소 분석의 사실상 표준(Parabible 등) | 형태소 **CC BY-SA 3.0** ✔ (본문은 SBLGNT 라이선스) |
| ★3 | **STEPBible TAGNT** | **케임브리지 Tyndale House** | **NA27/28·TR·SBLGNT·Tregelles·Byz·WH·THGNT의 모든 단어**를 담고, 단어마다 어느 판에 있는지 표시 | **CC BY 4.0** ✔ |
| ★4 | **MACULA Greek** | Clear Bible / Biblica | 구문 트리·형태소의 파이프라인 표준. Nestle1904·SBLGNT 기반 | **CC BY 4.0** ✔ (영어 뜻 BSB=PD) |

- **NA28 본문을 직접 쓸 수는 없지만**, TAGNT로 "NA28에 있는 단어인지"를 표시할 수 있다 → 학계 표준과의 차이를 보여 줄 수 있음.
- THGNT(Tyndale House GNT, 2017)는 본문 자체의 오픈 라이선스를 확인하지 못함 → TAGNT 안의 판본 표시로만 활용.

## 3. 결론: 1차 핵심 세트 (제안)

| 역할 | 히브리어 | 헬라어 |
|---|---|---|
| **본문(기준)** | WLC — OSHB `morphhb` | SBLGNT — `LogosBible/SBLGNT` |
| **형태·원형** | OSHB 형태소 | MorphGNT (또는 MACULA Greek) |
| **판본 차이·Strong 번호** | STEPBible TAHOT | STEPBible TAGNT (NA28 단어 표시) |
| **구문(나중)** | MACULA Hebrew | MACULA Greek |
| **제외** | BHSA (NC, 상업화 불가) | OGNT (NC) |

모두 **CC BY 4.0 / PD 중심**이라 출처 표시만 하면 나중에 상업화해도 문제가 없다. 예외: MorphGNT는 **CC BY-SA**(파생물도 같은 라이선스로 공개해야 함) → 상업화를 생각하면 MACULA Greek 형태소(CC BY)가 더 안전.

## 4. 이전 문서(06)와 달라진 점

- **SBLGNT 라이선스**: "CC BY 4.0"이 맞음을 원 저장소(`LogosBible/SBLGNT` README, v1.1 2022-12-19)로 확인. 일부 목록(Nida 등)에는 옛 EULA로 남아 있음.
- **OSHB 라이선스**: 일부 목록엔 MIT로 적혀 있으나, 실제 LICENSE.md는 **본문 PD + 원형·형태소 CC BY 4.0**.
- **MorphGNT**: CC BY-SA **3.0**으로 확인.

## 출처

- 직접 확인한 원문: [morphhb LICENSE](https://github.com/openscriptures/morphhb/blob/master/LICENSE.md) · [LogosBible/SBLGNT README](https://github.com/LogosBible/SBLGNT) · [morphgnt/sblgnt README](https://github.com/morphgnt/sblgnt) · [MACULA Greek LICENSE](https://github.com/Clear-Bible/macula-greek/blob/main/LICENSE.md) · [MACULA Hebrew LICENSE](https://github.com/Clear-Bible/macula-hebrew/blob/main/LICENSE.md) · [ETCBC BHSA README](https://github.com/ETCBC/bhsa) · [STEPBible-Data README](https://github.com/STEPBible/STEPBible-Data)
- [Nida Institute, Awesome Biblical Data](https://github.com/nida-institute/awesome-biblical-data)
- [sblgnt.com](https://sblgnt.com/) · [SBLGNT 소개](https://sblgnt.com/about/introduction) · [B-Greek 2010 (NA27과 542곳 차이)](https://www.ibiblio.org/bgreek/lists.ibiblio.org/2010-October/054698.html) · [hypotyposeis: SBLGNT 장치](https://hypotyposeis.org/weblog/thoughts-on-the-sblgnt-apparatus/)
- [eBible WLC 저작권](https://ebible.org/hboWLC/copyright.htm) · [Blue Letter Bible WLC](https://www.blueletterbible.org/wlc/2ch/5) · [tanach.us Supplements](https://tanach.us/Pages/Supplements.html)
- [Coding the Hebrew Bible (Roorda)](https://www.sciencedirect.com/org/science/article/pii/S2452366623000117) · [Parabible 리뷰](https://learnofchrist.com/resources/parabible)
