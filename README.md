# brief

국회 보고서 두 편을 문서별 **근거표**와 짧은 **보고 메모**로 정리하는 Claude Code 교육용 스킬입니다. 쉽게 읽을 수 있도록 스킬 원문은 저장소 루트의 [SKILL.md](SKILL.md)에 둡니다.

## 실습 시작

```bash
git clone https://github.com/mskim8717/brief.git
cd brief
mkdir -p .claude/skills/assembly-report-brief output
cp SKILL.md .claude/skills/assembly-report-brief/SKILL.md
claude
```

Claude Code 입력창에서 `/assembly-report-brief`를 입력합니다. 결과는 `output/보고서_근거표.md`에 저장됩니다. `input/`의 A·B 텍스트 두 편은 강사가 원본 PDF에서 **PDF쪽 표시를 붙여 미리 추출한 자료**입니다. 스킬은 이 텍스트를 읽으며 PDF 자체를 추출하지 않습니다. `sources/`의 PDF 두 편은 생성된 숫자·조문·쪽수를 사람이 대조할 때 사용합니다.

## 자료 출처와 이용조건

- [국회예산정책처 NABO Focus 제171호](https://www.nabo.go.kr/ko/periodical/focusView.do?key=2507040015&idx=9385), 「지역 자율형 연구개발사업의 주요 내용과 향후 과제」(2026). 원본 PDF: `sources/nabo-focus-171-regional-rnd.pdf`.
- [국회입법조사처 이슈와 논점 제2519호](https://www.nars.go.kr/report/view.do?cmsCode=CM0043&brdSeq=49532), 「인공지능 및 데이터 기반 행정 활성화에 관한 법률」 시행 관련 보고서(2026). 원본 PDF: `sources/nars-issue-2519-ai-data-admin-act.pdf`.

두 기관의 상세 페이지에는 **공공누리 제1유형(출처표시)**이 표시돼 있습니다. 이 저장소는 각 기관을 출처로 밝히고 원본 PDF를 수정하지 않은 채 제공합니다. PDF 무결성 값은 `sources/SHA256SUMS`에 있습니다. 입력 텍스트는 같은 PDF에서 실습용으로 추출한 파생 자료입니다.

## 결과 검토

A의 **26조 2,175억원(PDF 1쪽)**, B의 **제3조제5항(PDF 1쪽)**부터 원본과 대조하세요. `예정`·`계획`을 확정 사실로 바꾼 문장이 없는지도 확인합니다. 확실하지 않은 정보는 `확인 필요`로 남기는 것이 스킬의 규칙입니다.
