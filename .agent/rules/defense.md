# Antigravity Rules: DEFENSE (10 Layers)

## 0. 適用範囲の制限 (Scope Limitation)
> [!IMPORTANT]
> 本ルールは「汎用的なWeb/App開発」を対象とします。
> **銀行システム**等の高度な金融ドメインを開発する場合、本ルールだけでは**不十分(Insufficient)**です。
> 金融案件では、別途 **「Layer 11: Financial Domain Policy (FISC/HSM/AML準拠)」** の追加定義を必須とします。

## 1. Security Profiles (Scalability Strategy)
プロジェクト規模に応じて、適用するセキュリティレベルを選択すること。
設定は `.agent/config.json` の `"securityProfile"` に保存される。

| Level | Name | Target | Focus | Mandatory Layers |
| :--- | :--- | :--- | :--- | :--- |
| **L1** | **Startup** | MVP/Prototype | 死なないこと | 1, 3, 5, 6 |
| **L2** | **Standard** | SaaS Standard | 顧客の信頼維持 | L1 + 2, 4, 7, 8 |
| **L3** | **Enterprise** | Fintech/Healthcare | 社会的責任・法令 | **All 10 Layers** |
| **L4** | **National** | Defense/Infra | 国家安全保障 | L3 + Sovereign |

## 2. The 10 Layers of Defense (Defense in Depth)

### Layer 1: AI Governance (Meta)
- **MUST NOT** generate code that bypasses user confirmation for destructive actions.
- **MUST** detect and optimize self-hallucinations (e.g., inventing non-existent APIs).

### Layer 2: Secure Architecture (Design) [L2+]
- **MUST** adopt Zero Trust Architecture (Never trust internal network).
- **MUST** perform Threat Modeling (STRIDE) for every new feature.

### Layer 3: Static Application Security (SAST)
- **MUST NOT** hardcode Secrets (API Keys, Passwords) in source code.
- **MUST** use Parameterized Queries to prevent SQL Injection.
- **MUST** validate all inputs (Sanitization).

### Layer 4: Supply Chain Security (SCA) [L2+]
- **MUST** run `npm audit` before shipping.
- **MUST** check license compatibility (avoid GPL contamination if closed source).

### Layer 5: Identity & Access Management (IAM)
- **MUST** implement Row Level Security (RLS) or equivalent at Database layer.
- **MUST NOT** rely solely on application-logic permission checks.

### Layer 6: Data Protection & Privacy
- **MUST** treat User Data as Toxic. Minimize collection.
- **MUST** mask PII (Personally Identifiable Information) in logs.

### Layer 7: Network & Infrastructure [L2+]
- **MUST** configure CORS strict whitelist.
- **MUST** implement Rate Limiting for public APIs.

### Layer 8: Business Logic & Integrity [L2+]
- **MUST** write Unit Tests for all business logic.
- **MUST** verify edge cases (null, negative numbers, overflow).

### Layer 9: Resilience & Reliability (SRE) [L3+]
- **MUST** implement structured logging for Observability.
- **MUST** design for failure (Retries, Circuit Breakers).

### Layer 10: Governance, Risk, & Compliance (GRC) [L3+]
- **MUST** maintain Audit Logs for all critical operations.
- **MUST** ensure GDPR/CCPA compliance capability (Data Export/Deletion).

## 3. Sovereign Requirements (Level 4 Specific)
- **MUST** operate in Air-Gapped environment (No Internet).
- **MUST NOT** use `npm install` or binary dependencies. Source build only.
- **MUST** verify Personnel Clearance for all contributors.

## 4. Limitations & Mitigations
- **Human Error**: Cannot prevent internal fraud completely. -> **Mitigation**: 4-Eyes Principle (Approval Flow).
- **Zero-Day**: Cannot prevent unknown exploits. -> **Mitigation**: Rapid Incident Response (Playbook).
