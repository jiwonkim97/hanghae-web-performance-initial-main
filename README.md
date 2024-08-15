# 성능 개선 사후 보고서
## 1. 성능 개선 작업 이유
### 1-1 개요
- 이번 성능 개선 작업은 사용자 경험을 최적화하고, 검색 엔진 최적화(SEO)를 강화하며, 전반적인 웹사이트의 성능을 향상시키기 위해 진행되었습니다. 웹페이지의 로딩 속도는 사용자 유지율에 직접적인 영향을 미치는 중요한 요소입니다. 사용자가 웹페이지 로딩 속도가 느리다고 느낄 경우, 이탈률이 급격히 증가하게 됩니다. 또한, 최근 검색 엔진 알고리즘은 웹페이지의 성능, 특히 모바일 환경에서의 성능을 중요한 순위 요소로 고려하고 있습니다.

- 또한, Lighthouse와 같은 도구를 통해 확인한 웹페이지 성능 지표에서 주요 항목들에 대해 볼충분한 퍼포먼스를 보이고 있기에, 개선이 필요하다는 결과가 나왔습니다. 이러한 이유로, 사용자 경험을 극대화하고, 비즈니스 성과를 높이며, 웹사이트의 SEO를 최적화하기 위해 성능 개선 작업을 추진하게 되었습니다.
### 1-2 초기 프로젝트 성능 지표
| 지표 | 초기 값 | 점수 등급 |
|-----|--------|----------|
| 성능 점수 | 60 | 중간 (50-89) |
| 접근성 | 82 | 중간 (50-89) |
| 권장사항 | 96 | 높음 (90-100) |
| 검색엔진 최적화 | 82 | 중간 (50-89) |

## 2. 개선 방법
- 이미지 최적화, 폰트 최적화, js구문 최적화의 영역에서 총 9가지 작업을 통해 성능 지표를 향상시킵니다.

| 개선 항목 | 개선 방법 | 커밋 해시 | 성능 점수 | 접근성 점수 | 권장사항 점수 | SEO 점수 |
|----------|----------|----------|------------|----------|----------|------------|
| 이미지 접근성 개선 | alt 속성 추가 | [커밋 링크](https://github.com/jiwonkim97/hanghae-web-performance/commit/5e771ef882f743ac7c7a49eebd610778db4aaee6) | 68 | 91 | 93 | 91 |
| 이미지 로딩 성능 개선 | jpg, png 형태의 이미지를 webp 형태로 변경 | [커밋 링크](https://github.com/jiwonkim97/hanghae-web-performance/commit/2ea30ada9e31021767fc295a141c7d67f30446d2) |75 | 91 | 93 | 91 | 
| Hero 이미지 로딩 최적화 | screen size에 맞는 이미지만 초기에 로딩하도록 변경 | [커밋 링크](https://github.com/jiwonkim97/hanghae-web-performance/commit/29d46af3fbbd72663d6de4fcdcf434fcf7f3a145) |78 | 91 | 93 | 91 | 
| 폰트 로딩 최적화 | 폰트 소스를 로컬로 이동 | [커밋 링크](https://github.com/jiwonkim97/hanghae-web-performance/commit/8f9a0e1887641fed5d7f059d9b9859145f4ea0f4) |97 | 91 | 93 | 91 | 
| 레이아웃 시프팅 방지 | 내부 이미지가 로딩되지 않더라도 container 수준에서 높이를 유지하도록 변경 | [커밋 링크](https://github.com/jiwonkim97/hanghae-web-performance/commit/35914537aa25a06e8d0c7055eb22dde7c53fb5a6) |98 | 91 | 93 | 91 | 
| 명시적 이미지 크기 제공 | 모든 이미지에 width와 height 속성 추가 | [커밋 링크](https://github.com/jiwonkim97/hanghae-web-performance/commit/24cd9f26d08182ebd7f77ca16e221e30669f17fe) | 96 | 91 | 74 | 91 | 
| 레이지로딩 추가 | img 태그에 layout=lazy 속성 추가 | [커밋 링크](https://github.com/jiwonkim97/hanghae-web-performance/commit/33316e8e4a5259b762a24013710fc11dedd6f171) |96 | 91 | 74 | 91 | 
| 불필요한 js문 로딩 시점 변경 | 초기 렌더링 시에 불필요한 js 구문 실행 시점 뒤로 미루기 | [커밋 링크](https://github.com/jiwonkim97/hanghae-web-performance/commit/0545135d25b639f3c34e270f5c02e6d2c453d6e4) |99 | 95 | 74 | 91 | 
| 초기에 불필요한 js 실행시간 단축 | 초기 렌더링 시에 불필요한 js 구문 실행 시점 뒤로 미루기 | [커밋 링크](https://github.com/jiwonkim97/hanghae-web-performance/commit/11ceb71a15fb3c0d68874a18262905299e8ed4e4) | 98 | 94 | 74 | 91 | 

## 3. 개선 후 향상된 지표
## 4. 발전 가능성

낮음 (0-49)
중간 (50-89)
높음 (90-100)