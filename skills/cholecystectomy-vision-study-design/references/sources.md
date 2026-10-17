# 출처와 검증 상태

PubMed 메타데이터로 확인한 것은 ✅, 웹 검색으로 존재만 확인한 것은 ☑️, 미확인은 `[VERIFY]`.

## 핵심 (Metrics Reloaded)
- ✅ Maier-Hein L, Reinke A, Godau P, et al. Metrics reloaded: recommendations for image analysis
  validation. *Nat Methods* 2024;21(2):195–212. doi:10.1038/s41592-023-02151-z · PMID 38347141 ·
  PMC11182665 · arXiv:2206.01653 (v8 = 출판본)
- ✅ Reinke A, Tizabi MD, Baumgartner M, et al. Understanding metric-related pitfalls in image analysis
  validation. *Nat Methods* 2024;21(2):182–194. doi:10.1038/s41592-023-02150-0 · PMID 38347140 ·
  PMC11181963
- 구현: https://github.com/Project-MONAI/MetricsReloaded · 도구: https://metrics-reloaded.dkfz.de `[VERIFY: 접근성]`

## 수술 데이터 과학
- ✅ Meireles OR, Rosman G, Altieri MS, et al. SAGES consensus recommendations on an annotation
  framework for surgical video. *Surg Endosc* 2021;35(9):4918–4929. doi:10.1007/s00464-021-08578-9 ·
  PMID 34231065
- ✅ Eckhoff JA, Rosman G, Altieri MS, et al. SAGES consensus recommendations on surgical video data
  use, structure, and exploration. *Surg Endosc* 2023;37(11):8690–8707. doi:10.1007/s00464-023-10288-3 ·
  PMID 37516693
- ✅ Funke I, Rivoir D, Speidel S. Metrics matter in surgical phase recognition. arXiv:2305.13961 (2023)
  — Cholec80 평가 불일치 정리; relaxed 지표 금지, 여러 seed·SD, 비디오별 vs 풀링 명시 권고.
- ✅ segmental F1@k: Lea C, et al. Temporal convolutional networks for action segmentation and detection. CVPR 2017
  (arXiv:1611.05267). Edit score는 Lea, Vidal, Hager 2016에서 유래(학회명 미확인).
- ✅ GoNoGoNet: Madani A, et al. *Ann Surg* 2022;276:363–369, doi:10.1097/SLA.0000000000004594
- ✅ 담낭절제 공개 데이터: Cholec80(doi:10.1109/TMI.2016.2593957), CholecT50(*Med Image Anal* 2022;78:102433),
  CholecSeg8k(arXiv:2012.12453), Endoscapes2023(*Sci Data* 2025;12:331, doi:10.1038/s41597-025-04642-4),
  HeiChole(*Med Image Anal* 2023;86:102770), CholecInstanceSeg(*Sci Data* 2025) — 상세는 범용 스킬 sources.md

## 보고 가이드라인
- ✅ Tejani AS, Klontzas ME, Gatti AA, et al. Checklist for Artificial Intelligence in Medical Imaging
  (CLAIM): 2024 Update. *Radiol Artif Intell* 2024;6(4):e240300. doi:10.1148/ryai.240300
- ✅ Collins GS, Moons KGM, Dhiman P, et al. TRIPOD+AI statement. *BMJ* 2024;385:e078378.
  doi:10.1136/bmj-2023-078378 (한국어 번역: *Ewha Med J* 2025;48(3):e48, doi:10.12771/emj.2025.00668)
- ✅ DECIDE-AI: Vasey B, et al. *Nat Med* 2022;28:924–933, doi:10.1038/s41591-022-01772-9 (동시 *BMJ* 2022;377:e070904)
- ✅ IDEAL: McCulloch P, et al. *Lancet* 2009;374:1105–12, doi:10.1016/S0140-6736(09)61116-8

## 인용 규칙
- Metrics Reloaded는 두 논문을 함께 인용.
- 원문 문장 장문 인용 금지, 의역.
- `[VERIFY]` 항목은 원고에 넣기 전 PubMed/원문으로 확인 후 표시 제거.
