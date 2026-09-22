# Agentic AI / AWS AI Notes

SAA 시험 범위를 넘어서는 AI 학습 내용을 별도로 관리합니다.

## Concept
단순 LLM 호출보다 실제 Agentic AI는 보통 다음과 같은 실행 계층을 포함합니다.

```text
User
 ↓
Application / Agent Runtime
 ├─ Prompt / Context
 ├─ Tools
 ├─ APIs
 ├─ Memory
 └─ Policies / Guardrails
 ↓
LLM
 ↓
Reasoning / Tool Selection / Response
```

LLM이 단순히 '말만 하는' 구성으로 한정되는 것은 아니며, Agent Runtime/서버가 외부 도구 실행과 상태 관리를 담당하고 LLM은 필요한 행동 선택과 결과 해석에 관여하는 구조가 일반적입니다.
