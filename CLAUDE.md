# AI 입문자를 위한 교육 자료 제작 프로젝트

## 프로젝트 개요
IT 기업 신입사원 대상 AI 교육 자료 제작. ChatGPT 이후 AI 변화의 흐름, 기술 원리, 최신 트렌드를 체계적으로 다루는 종합 교육 문서.

## 하네스 구성
- **에이전트**: `.claude/agents/` (6개)
  - ai-historian, model-analyst, trend-researcher, devpractice-expert, content-assembler, fact-checker
- **스킬**: `.claude/skills/` (6개)
  - web-research, timeline-builder, tech-explainer, glossary-builder, content-formatter, ai-edu-orchestrator
- **오케스트레이터**: `ai-edu-orchestrator` 스킬이 전체 워크플로우 관리

## 실행 방법
1. `ai-edu-orchestrator` 스킬을 참조하여 Phase 1~4 순서대로 실행
2. Phase 1: 4개 리서치 에이전트 병렬 실행 (Agent 도구, run_in_background: true)
3. Phase 2: content-assembler로 통합
4. Phase 3: fact-checker로 검증
5. Phase 4: 최종본 `output/AI-Education-Complete.md` 생성

## 산출물
모든 산출물은 `output/` 디렉토리에 저장.

## 작성 원칙
- 정확한 정보 + 출처 명시
- 출시 시기 명시
- 비즈니스 효과 포함
- 어려운 개념은 풀어서 설명
- 커밋 메시지는 한글로
