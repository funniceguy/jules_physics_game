# AGENTS.md for Antigravity Client

## 🧠 Context Knowledge
Please read the following documents in the `docs/` directory before planning any tasks:
1. ‘docs/01_Requirements/PRD.md’ :  PRD, 로드맵 저장
2. ‘docs/02_Architecture/TechSpec_Antigravity.md’ : 기술문서, 시스템 구조, 데이터 흐름, 물리 엔진, 핵심 로직(중력 제어 등) 명세
3. ‘docs/04_Planning/TaskList.md’ : 할 일 관리 (Sprint, Backlog)
4. ‘docs/06_UI/01_UI_Design_System.md’ : UI 디자인 및

## 🛡️ Coding Standards
- **Language:** JavaScript.
- **Style:** Functional programming preferred over OOP where possible.
- **Testing:** Every new feature must include a Jest unit test file.
- **Comments:** Write JSDoc for all exported functions.


## 🚫 Constraints
- Do NOT use `any` type in JavaScript.
- Do NOT modify `package.json` dependencies without explicit permission.
