# Search Algorithm Visualizer

시작~목표 노드 사이 경로를 다양한 서치 알고리즘으로 찾아 실시간으로 보여주는 단일 HTML 프로토타입.

## 실행
```bash
open "index.html"
```
빌드/서버 불필요, 브라우저에서 바로 실행.

## 기능
- 노드 24개 그래프 자동 생성 (`New graph`로 재생성)
- `Set start` / `Set goal` 클릭 후 노드 클릭으로 시작·목표 지정
- 각 노드 위 회색 숫자 = h(n) (goal까지 남은 추정 거리, 작을수록 좋음)
- 탐색 중 frontier(주황) / 방문(파랑) / 최종 경로(빨강) 색으로 진행 과정 표시
- 사이드바에 Enqueuings / Extensions / Queue size / Path elements / Path length 실시간 갱신

## 지원 알고리즘 (Type)
| 종류 | 방식 |
|---|---|
| Depth-first | 스택(LIFO), 한 방향으로 끝까지 파고들다 백트랙 |
| Breadth-first | 큐(FIFO), 가까운 순서로 층층이 탐색 |
| British Museum | 모든 단순 경로를 전부 확인 후 최적 선택 (항상 최적이지만 매우 느림 — 예산 초과 시 "so far" 최선 경로 표시) |
| Beam search | h값 기준 상위 N개(폭)만 남기고 탐색 |
| Hill climbing | 매 순간 h값이 가장 낮은 이웃 하나로만 이동, 되돌아가기 없음 |

`extended-list filtering` 체크박스로 이미 방문한 노드 재확장 허용/차단 전환 (British Museum엔 해당 없음, 자동 숨김).

## 저장소
[github.com/HynKxrea/Opt-algorithm](https://github.com/HynKxrea/Opt-algorithm)
