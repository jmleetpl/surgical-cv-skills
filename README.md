# surgical-cv-skills

수술영상 컴퓨터비전(CV) 연구를 **데이터 수집·주석 전에** 설계하는 Claude 스킬 2종입니다.
*Claude skills for designing surgical-video computer-vision studies before data collection (skills are written in Korean).*

📘 **튜토리얼 (따라 하기):** https://jmleetpl.github.io/surgical-cv-skills/

| 스킬 | 언제 쓰나 |
|---|---|
| `surgical-cv-study-design` | 모든 외과 수술(간절제·간이식·췌장·위·대장·식도·탈장·충수·갑상선·비만·전립선·자궁·개복 등) |
| `cholecystectomy-vision-study-design` | 담낭절제술 전용 심화판(CVS, 담낭관, Go/No-Go 등) |

## 무엇을 하나

1. **수술 프로파일**: 표준 단계, 핵심 위험구조, 안전 확인지점, 줄이려는 합병증, 기구, 접근법별 영상 특성, 개인정보 위험, 관련 공개 데이터셋
2. **임상 질문 → CV 과제 → 문제유형** (image-level classification / semantic segmentation / object detection / instance segmentation)
3. **Metrics Reloaded** 원칙으로 problem fingerprint → 지표 선택 → 지표 적용(집계·NaN·CI·보고)
4. **데이터·주석·분할 계획** (환자 단위 분할, 이중주석 일치도, 빈 프레임 2층 평가, τ 도출 등)
5. **설계서** `study_design/<procedure>_cv_design.md` + 레드플래그 점검(RF0–RF18)

## 설치

### Claude Code — 플러그인 (권장)
```bash
claude plugin marketplace add jmleetpl/surgical-cv-skills
claude plugin install surgical-cv-skills@surgical-cv-skills
```

### Claude Code — 스킬 폴더에 직접 복사
macOS / Linux:
```bash
git clone https://github.com/jmleetpl/surgical-cv-skills.git
cp -R surgical-cv-skills/skills/* ~/.claude/skills/
```
Windows (PowerShell):
```powershell
git clone https://github.com/jmleetpl/surgical-cv-skills.git
Copy-Item -Recurse -Force .\surgical-cv-skills\skills\* "$HOME\.claude\skills\"
```

### claude.ai (웹)
[Releases](https://github.com/jmleetpl/surgical-cv-skills/releases)에서 zip 두 개를 받아
**설정 → 기능(Capabilities) → Skills → 추가 → Skill 업로드**로 올립니다.

## 사용 예
```
간절제 영상에서 간정맥 분할 연구를 설계해줘. 2개 기관, 로봇·복강경 180례.
```
```
단일공 로봇 담낭절제 CVS 판정 연구, 어떤 지표를 써야 해?
```

## 연계 스킬 (선택)
설계서는 `/model-assessment`, `/check-reporting`, `/calc-sample-size`, `/imaging-data`, `/design-ai-benchmarking`
(Aperivue/medsci-skills)으로 넘기도록 되어 있습니다. 설치돼 있지 않으면 Claude가 같은 역할을 직접 수행합니다.

## 근거와 한계
- 핵심 근거: Maier-Hein L, Reinke A, et al. *Nat Methods* 2024;21:195–212 (doi:10.1038/s41592-023-02151-z) 및
  Reinke A, et al. *Nat Methods* 2024;21:182–194 (doi:10.1038/s41592-023-02150-0). 원문을 의역·요약했으며 공식 프레임워크를 대체하지 않습니다.
- 수술 프로파일의 임상 내용(단계·위험구조·안전 확인지점)은 **초안**입니다. 연구팀 외과의가 확정해야 합니다.
- 공개 데이터셋·가이드라인 서지는 2026-10-17 기준 검증 상태를 `references/sources.md`에 표시했습니다.
- Metrics Reloaded가 다루지 않는 영역(시간적 phase 평가, 회귀, 추적, 3D, 다중관찰자 정답)은 범위 밖으로 명시합니다.
- 설계 보조 도구이며, 통계·임상 판단을 대신하지 않습니다.

## License
MIT © 2026 Jeong-Moo Lee (Ewha Womans University Seoul Hospital, Department of Surgery)
