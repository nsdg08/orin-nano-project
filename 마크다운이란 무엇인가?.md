GitHub에서 사용하는 **마크다운(Markdown)**은 일반 텍스트 형식으로 작성하면서도 간단한 문법으로 서식을 지정할 수 있는 lightweight 마크업 언어입니다. GitHub에서는 이를 조금 확장한 **GitHub Flavored Markdown (GFM)**을 사용합니다.

✅ 마크다운이란?
텍스트 기반 서식 언어

.md 또는 .markdown 확장자를 가진 파일에 사용

README 파일, 이슈, 풀 리퀘스트 설명, Wiki, 댓글 등에 자주 사용됨

HTML로 변환 가능

🔹 GitHub 마크다운(GFM) 주요 문법 요약
기능	문법 예시	결과
제목	# 제목1
## 제목2	제목 크기 설정
굵은 글씨	**굵게** 또는 __굵게__	굵게
기울임	*기울임* 또는 _기울임_	기울임
코드 블록 (인라인)	`코드`	코드
코드 블록 (멀티라인)	<pre><br>코드<br></pre>여러 줄 코드 표시
링크	[OpenAI](https://openai.com)	OpenAI	
리스트 (순서 없음)	- 항목 또는 * 항목	• 항목
리스트 (순서 있음)	1. 첫째
2. 둘째	1. 첫째
2. 둘째
인용문	> 인용문	> 인용문
체크리스트	- [ ] 항목
- [x] 완료된 항목	☑ 체크리스트
표	| 헤더 |
|-----|
| 데이터 |	표 생성
취소선	~~취소~~	취소

💡 GitHub Flavored Markdown(GFM)의 특징
GitHub에서는 일반 마크다운에서 확장된 기능도 제공합니다:

✅ 체크박스

🎨 테이블(Table)

[✏️](https://upload.inven.co.kr/upload/2014/11/28/data/i1791089215.png) 이슈 및 PR 내에서 사용자 @멘션, #이슈번호, 커밋 참조

🔄 자동 링크 변환

📌 HTML 태그 일부 허용 (단, 제한 있음)

📁 사용 예시 파일
README.md: 저장소 소개

CONTRIBUTING.md: 기여 가이드

main.md: 문서화 파일

.github/ISSUE_TEMPLATE.md: 이슈 템플릿
