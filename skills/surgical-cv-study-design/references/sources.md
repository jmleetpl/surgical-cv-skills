# 출처와 검증 상태 (2026-10-17 검증)

✅ = 1차 출처(PubMed·arXiv 원문·출판사·데이터 페이지)로 확인 · ☑️ = 검색 결과/2차 페이지로만 확인 · ❌ = 공개 데이터 없음/미확인.
원고에 넣기 전 ☑️ 항목은 원문으로 한 번 더 확인한다. 데이터셋 라벨 수·버전은 출처마다 다를 수 있으니
**사용한 버전을 명시**한다.

## 1. 핵심 방법론
- ✅ Maier-Hein L, Reinke A, et al. Metrics reloaded. *Nat Methods* 2024;21:195–212. doi:10.1038/s41592-023-02151-z (PMID 38347141)
- ✅ Reinke A, Tizabi MD, et al. Understanding metric-related pitfalls in image analysis validation. *Nat Methods* 2024;21:182–194. doi:10.1038/s41592-023-02150-0 (PMID 38347140)
- ✅ Funke I, Rivoir D, Speidel S. Metrics matter in surgical phase recognition. arXiv:2305.13961 (2023, 기술보고서).
  요지: Cholec80 지표 계산이 논문마다 달라 비교 불가 — 빠진 단계 처리, F1 계산법, relaxed boundary가 주원인.
  권고: 표준 split+별도 검증셋, 여러 seed와 SD, 평가 코드·비디오별 예측 공개, Jaccard 또는 F1 보고(단계별 F1
  평균 ≠ 평균 precision·recall의 조화평균 — 후자가 더 큼), **relaxed 지표 사용 금지**(널리 쓰인 MATLAB 스크립트
  버그로 precision/recall이 1을 넘을 수 있음), 이전 논문 수치 복사 시 계산 방식 확인·명시. 비디오별 평균 vs
  풀링은 어느 쪽도 권하지 않고 "서로 비교 불가"라고 함 → 어느 쪽인지 명시.
- ✅ Lea C, Flynn MD, Vidal R, Reiter A, Hager GD. Temporal convolutional networks for action segmentation and detection.
  CVPR 2017 (arXiv:1611.05267) — **segmental F1@k(k=10,25,50) 제안**. Edit score는 그 논문이 인용한 Lea, Vidal,
  Hager 2016(☑️ 학회명 미확인)에서 유래.

## 2. 보고·평가 가이드라인
- ✅ CLAIM 2024: Tejani AS, et al. *Radiol Artif Intell* 2024;6(4):e240300. doi:10.1148/ryai.240300
- ✅ TRIPOD+AI: Collins GS, et al. *BMJ* 2024;385:e078378. doi:10.1136/bmj-2023-078378 (한국어판 *Ewha Med J* 2025;48(3):e48)
- ✅ DECIDE-AI: Vasey B, et al. *Nat Med* 2022;28(5):924–933, doi:10.1038/s41591-022-01772-9 (PMID 35585198);
  동시 게재 *BMJ* 2022;377:e070904, doi:10.1136/bmj-2022-070904
- ✅ IDEAL: McCulloch P, et al. *Lancet* 2009;374:1105–12, doi:10.1016/S0140-6736(09)61116-8; 개정 Hirst A, et al.
  *Ann Surg* 2019;269:211–220, doi:10.1097/SLA.0000000000002794; 기기 확장 IDEAL-D Marcus HJ, et al. *Ann Surg*
  2022;275:73–79, doi:10.1097/SLA.0000000000004907
- ✅ SAGES 주석 합의: Meireles OR, et al. *Surg Endosc* 2021;35:4918–4929, doi:10.1007/s00464-021-08578-9
- ✅ SAGES 영상 데이터 합의: Eckhoff JA, et al. *Surg Endosc* 2023;37:8690–8707, doi:10.1007/s00464-023-10288-3

## 3. 공개 수술영상 데이터셋 (수술별)

| 수술 | 데이터셋 | 핵심 | 출처 | 상태 |
|---|---|---|---|---|
| 담낭절제 | Cholec80 | 80편, 7 phase, 7 기구 존재 | Twinanda, *IEEE TMI* 2017, doi:10.1109/TMI.2016.2593957 | ✅ CC BY-NC-SA |
| 담낭절제 | CholecT50 | 50편, 100 triplet | Nwoye, *Med Image Anal* 2022;78:102433 | ✅ |
| 담낭절제 | CholecSeg8k | 8,080 프레임, 13 클래스 | Hong, arXiv:2012.12453 | ✅ |
| 담낭절제 | Endoscapes2023 | 201편, CVS·bbox·분할 | *Sci Data* 2025;12:331, doi:10.1038/s41597-025-04642-4 (PubMed 1저자 Mascagni / arXiv 1저자 Murali) | ✅ 분할 프레임 수는 출처마다 다름 |
| 담낭절제 | HeiChole | 33편 3기관, phase·action·기구·술기 | Wagner, *Med Image Anal* 2023;86:102770 | ✅ |
| 담낭절제 | CholecInstanceSeg | 41.9k 프레임, 기구 instance | Alabi, *Sci Data* 2025, doi:10.1038/s41597-025-05163-w | ☑️ DOI |
| 담낭절제 | GoNoGoNet (데이터 비공개) | Go/No-Go 영역 | Madani, *Ann Surg* 2022;276:363–369, doi:10.1097/SLA.0000000000004594 | ✅ |
| 간절제 | P2ILF | 간 랜드마크·2D–3D 정합 | Ali, *Med Image Anal* 2025;99:103371 | ✅ |
| 간절제 | PmLR50 | 50편, phase + Pringle 효과 | Guo, AAAI 2025, arXiv:2408.10538 | ✅ 논문 / ❌ 공개 미확인 |
| 대장 | HeiCo (ROBUST-MIS) | 30편, phase·기구·instance 분할 | Maier-Hein, *Sci Data* 2021;8:101, doi:10.1038/s41597-021-00882-2 | ✅ |
| 직장(로봇) | DSAD | 32편, 11 구조(요관·IMA 등) 마스크 | Carstens, *Sci Data* 2023;10:3, doi:10.1038/s41597-022-01719-2 | ✅ |
| 비만(RYGB) | Bypass40 | 40편 phase·step | Ramesh, *IJCARS* 2021, doi:10.1007/s11548-021-02388-z | ✅ 논문 / 공개 여부 ❌ |
| 비만(RYGB) | MultiBypass140 | 140편 2기관, 12 phase·46 step·부작용 | Lavanchy, *IJCARS* 2024, doi:10.1007/s11548-024-03166-3 | ✅ CC BY-NC-SA |
| 자궁절제 | AutoLaparo | 21편, phase·카메라 동작·분할 | Wang, MICCAI 2022, arXiv:2208.02049 | ✅ 신청제 |
| 전립선(로봇) | SAR-RARP50 | 50 봉합 구간, gesture·분할 | Psychogyios, arXiv:2401.00496 | ✅ |
| 전립선(로봇) | GraSP | 13편, phase·step·기구 분할 | Ayobi, arXiv:2401.11174 | ✅ 데이터 라이선스 불명 |
| 로봇(돼지) | EndoVis 2017 / 2018 | 기구·장면 분할 | Allan, arXiv:1902.06426 / 2001.11190 | ✅ |
| 충수 | Appendix300 | 330 영상, 염증 등급 | OPARA doi:10.25532/OPARA-1173 | ✅ 수량 출처마다 다름 |
| 백내장(현미경) | CATARACTS / Cataract-101 | 기구 존재 / phase | Al Hajj, *Med Image Anal* 2019;52:24–41; Schoeffmann, MMSys 2018 | ✅ |
| 뇌하수체(내시경) | PitVis | 25편 공개, 12 step·19 기구 | Das, arXiv:2409.01184 | ✅ |
| 개복(머리착용) | EgoSurgery-Phase / -Tool | 개복 phase·기구·손 | Fujii, MICCAI 2024 arXiv:2405.19644 / arXiv:2406.03095 | ✅ |
| 식도(RAMIE) | — | 27편 단계 연구 있음 | Li, arXiv:2412.04039 | ❌ 공개 미확인 |
| 위절제·갑상선·탈장·췌장 | — | 연구는 있으나 공개 데이터 미확인 | — | ❌ |
| 대규모 사전학습 | LEMON, SurgBench, SurgeNetXL, SurgVU(돼지) | 수백만 프레임 | arXiv:2503.19740 / 2506.07603 / 2501.09436 / 2501.09209 | ✅/☑️ 라이선스 확인 필요 |

## 인용 규칙
- Metrics Reloaded는 두 논문을 함께 인용, 원문 장문 인용 금지.
- 데이터셋은 사용 버전·라벨 수·라이선스를 명시. 비상업(NC) 라이선스는 상업적 모델 학습 제한.
