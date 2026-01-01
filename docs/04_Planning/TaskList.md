# Project Roadmap & Risks (Roadmap)

이 문서는 단순 작업 목록을 넘어, 프로젝트의 장기적인 방향성과 기술적 난제, 주의사항을 기록합니다.

## 🚧 Technical Debt & Risks (기술적 부채 및 위험)
- [ ] **Physics Determinism**: Matter.js는 부동소수점 연산으로 인해 브라우저/기기마다 미세하게 다른 물리 결과를 낼 수 있음. (경쟁 요소 도입 시 주의)
- [ ] **Garbage Collection**: 파티클이나 DOM 요소를 자주 생성/삭제하는 현재 방식은 모바일에서 GC Pausing을 유발할 수 있음. -> Object Pooling 고려 필요.
- [ ] **Canvas Resolution**: 고해상도(Retina) 디스플레이에서 캔버스가 흐릿하게 보일 수 있음. `devicePixelRatio` 대응 필요.

## 🔭 Future Roadmap (로드맵)
### Phase 7: Advanced Rendering
- **Pixi.js Migration**: 현재 Matter.Render(Debug용)와 DOM Overlay 방식을 WebGL 기반의 Pixi.js로 통합하여 퍼포먼스와 시각적 퀄리티 대폭 향상. (Shader Effect 등)

### Phase 8: Social & Competitive
- **Web Socket**: 실시간 1:1 대전 모드. (상대의 합체 충격이 나에게 넘어오는 등 뿌요뿌요 방식)
- **Leaderboard**: Backendless(Firebase) 또는 Custom Server를 통한 글로벌 랭킹.

### Phase 9: Content Expansion
- **Themes**: 계절별(크리스마스, 할로윈) 과일 스킨 및 배경.
- **New Modes**: 타임 어택, 제한된 횟수 내 최고 점수 내기 등.

## ⚠️ Known Issues (알려진 문제)
- 모바일 사파리(iOS)에서 오디오 컨텍스트가 탭 전환 시 중단되는 현상 (현재 `visibilitychange` 핸들러로 일부 대응).
- 아이템 사용 순간 물리 연산이 튀는 현상 (Force application tuning 필요).
