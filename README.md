# AI-SOC

AI 기반 SOC 자동화 체계 연구 프로젝트

Splunk, n8n, LLM을 연계하여 **Alert Triage, Context Enrichment, 침해사고 분석 및 대응 자동화**를 연구합니다.

## Multi-Agent 기반 SOC

### Tech Stack

- **Workflow Orchestration:** n8n
- **SIEM:** Splunk REST API
- **LLM:** OpenAI GPT-4o
- **Notification:** Discord Webhook
- **Endpoint Telemetry:** Sysmon
- **Response Integration:** EDR / Firewall API
- **Dataset:** Splunk BOTS v3

### 프로젝트 진행 현황

- **현재:** Encoded PowerShell 시나리오 기반 Multi-Agent 침해사고 분석 PoC 구현
- **구현:** Triage → Investigation → Synthesis → Human-in-the-Loop 기반 대응 프로세스
- **보완:** PowerShell 중심 분석 구조를 다양한 Alert 유형에 적용 가능한 범용 구조로 확장
- **목표:** 다양한 보안 이벤트를 자율적으로 조사하고, 중요 대응은 분석가가 통제하는 SOC 자동화 체계 구축

## Development Roadmap

### Phase 1. Alert Triage & Context Enrichment

- Alert 유형 자동 분류
- 공격 유형별 Specialized Triage
- Host / User / IP / Process 기반 연관 로그 자동 조회
- TP / FP / Unknown 및 위험도 판단
- 판단 근거 및 추가 조사 항목 제공

```text
Splunk Alert
    ↓
Alert Classification
    ↓
Specialized Triage
    ↓
Context Enrichment
    ↓
Evidence Aggregation
    ↓
TP / FP / Unknown
    ↓
Analyst Review
```

### Phase 2. Incident Timeline Reconstruction

Endpoint, Network, Authentication 이벤트를 연계하여 **공격 행위를 시간 순서대로 자동 재구성**합니다.

### Phase 3. Attack Story Generation

Timeline과 분석 Evidence를 기반으로 **공격 경로, 주요 행위, 영향 범위를 Incident Story 형태로 생성**합니다.

## Goal

> **Alert 탐지부터 Context 수집, 분석, Incident Timeline 및 Attack Story 생성까지 이어지는 AI 기반 SOC 분석 자동화 체계 구축**

최종 대응은 **Human-in-the-Loop** 구조를 유지하여 분석가 승인 하에 수행합니다.
