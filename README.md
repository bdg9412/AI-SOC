# AI-SOC
AI 기반 SOC 체계 연구

## Multi-Agent 기반 SOC
### Tech Stack

- **Workflow Orchestration:** n8n

- **SIEM:** Splunk REST API

- **LLM:** OpenAI GPT-4o

- **Notification:** Discord Webhook

- **Endpoint Telemetry:** Sysmon

- **Response Integration:** EDR / Firewall API
### 프로젝트 진행 현황

- **현재**: Encoded PowerShell 시나리오를 기반으로 Splunk, n8n, LLM을 연계한 멀티 에이전트 침해사고 분석 PoC를 구현.
- **보완점**: 이벤트 정규화, 시나리오 자동 분류, 공격 유형별 플레이북 및 다양한 보안 솔루션 연동 필요
- **목표**: 특정 탐지에 한정되지 않고 다양한 보안 이벤트를 자율적으로 조사하며, 중요 대응은 분석가가 통제하는 범용 SOC 자동화 체계 구축
