# Specification Links

This document maps features in this repository to their source specifications
in the [specs repository](https://github.com/localstore-platform/specs).

**Spec Version:** [v1.1-specs](https://github.com/localstore-platform/specs/tree/v1.1-specs)

**Last Updated:** 2025-12-06

---

## How to Use This Document

1. When implementing a feature, find it in the table below
2. Click the spec link to view the authoritative specification
3. Use line number references to load only relevant sections
4. Follow the spec exactly for API contracts, schemas, and behaviors

---

## Core Specifications

### Architecture

- [GraphQL Schema](https://github.com/localstore-platform/specs/blob/v1.1-specs/architecture/graphql-schema.md)
  - Type definitions (lines 1-400)
  - Queries (lines 400-600)
  - Mutations (lines 600-800)
  - Real-time subscriptions (lines 800-900)

- [API Specification](https://github.com/localstore-platform/specs/blob/v1.1-specs/architecture/api-specification.md)
  - REST fallback endpoints (lines 80-1200)
  - WebSocket events (lines 1800-2000)
  - Dashboard-specific endpoints (lines 500-750)

- [Multi-Domain User Management](https://github.com/localstore-platform/specs/blob/v1.1-specs/architecture/multi-domain-user-management.md)
  - Multi-location access control
  - Role-based permissions

- [Database Schema](https://github.com/localstore-platform/specs/blob/v1.1-specs/architecture/database-schema.md)
  - Menu items schema (lines 250-350)
  - Categories schema (lines 200-250)
  - User/tenant relationships (lines 80-200)

### Design

- [Wireframes & UX Flow](https://github.com/localstore-platform/specs/blob/v1.1-specs/design/wireframes-ux-flow.md)
  - Admin dashboard views (lines 800-1200)
  - Menu management UI (lines 1200-1500)
  - Mobile owner dashboard (lines 400-800)
  - Onboarding flow (lines 50-150)

- [Flowchart](https://github.com/localstore-platform/specs/blob/v1.1-specs/design/flowchart.md)
  - Admin user flows (lines 300-500)
  - Menu CRUD operations (lines 500-700)

### Implementation

- [Implementation Roadmap](https://github.com/localstore-platform/specs/blob/v1.1-specs/planning/implementation-roadmap.md)
- [Sprint 1 Plan](https://github.com/localstore-platform/specs/blob/v1.1-specs/planning/sprint-1-implementation.md)
- [MVP Acceptance Criteria](https://github.com/localstore-platform/specs/blob/v1.1-specs/planning/mvp-acceptance-criteria.md)

---

## Cross-Cutting Concerns

### Localization

- [Communication Language Guidelines](https://github.com/localstore-platform/specs/blob/v1.1-specs/knowledge-base/communication-language-guidelines.md)
- [Glossary](https://github.com/localstore-platform/specs/blob/v1.1-specs/knowledge-base/glossary.md)
  - Vietnamese/English term translations
  - Standard terminology

### Market Context

- [Vietnam Market Strategy](https://github.com/localstore-platform/specs/blob/v1.1-specs/research/vietnam-market-strategy.md)
  - Mobile-first requirements
  - Payment integrations (MoMo, ZaloPay, VNPay)
  - Social platform integrations (Zalo, Facebook)
  - 4G performance targets (<2s TTI)
  - Currency formatting (75.000₫)

### Monitoring & Operations

- [Monitoring Runbook](https://github.com/localstore-platform/specs/blob/v1.1-specs/documentation/monitoring-runbook.md)
- [Launch Readiness Checklist](https://github.com/localstore-platform/specs/blob/v1.1-specs/documentation/LAUNCH-READINESS.md)

---

## Spec Update Protocol

When the specs repository releases a new version:

1. Review [SPEC_CHANGELOG.md](https://github.com/localstore-platform/specs/blob/master/SPEC_CHANGELOG.md)
2. Identify breaking changes affecting this repository
3. Update this file to reference new spec version
4. Implement required changes
5. Update repository version and tag release

---

## AI Context Loading

AI assistants should:

- Load specs **on-demand** using the links above
- Use line number ranges to minimize context
- Reference this spec version consistently
- Follow [AI Context Guide](https://github.com/localstore-platform/specs/blob/v1.1-specs/.github/AI_CONTEXT_GUIDE.md)

**Example:**

```text
semantic_search(
  repo: "https://github.com/localstore-platform/specs",
  query: "GraphQL dashboard queries"
)
```

Then read specific sections:

```text
read_file(
  "architecture/graphql-schema.md",
  lines: 400-600
)
```
