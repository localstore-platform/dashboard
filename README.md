# LocalStore Dashboard

🎛️ Operations dashboard for LocalStore Platform - Next.js web portal for restaurant owners and staff. Menu management, sales tracking, and analytics. Powers `{tenant}.localstoreplatform.com` operations domains with GraphQL + real-time updates.

## Tech Stack

- **Framework:** Next.js 14 (App Router)
- **Language:** TypeScript 5
- **Styling:** Tailwind CSS 3
- **Data Fetching:** Apollo GraphQL Client
- **Real-time:** Socket.io client (WebSocket)
- **Deployment:** Vercel

## Quick Start

### Prerequisites

- Node.js 18+
- pnpm (recommended) or npm

### Installation

```bash
# Clone the repository
git clone https://github.com/localstore-platform/dashboard.git
cd dashboard

# Install dependencies
pnpm install

# Copy environment variables
cp .env.example .env.local

# Start development server
pnpm dev
```

Open <http://localhost:3000> to view the dashboard.

## Documentation

- [Specification Links](docs/SPEC_LINKS.md) - Links to relevant specs
- [Git Workflow](docs/GIT_WORKFLOW.md) - Branch and commit conventions

## Specifications

This repository implements features defined in the [LocalStore Platform Specs](https://github.com/localstore-platform/specs) repository.

**Current Spec Version:** [v1.1-specs](https://github.com/localstore-platform/specs/tree/v1.1-specs)

Key specifications:

- [GraphQL Schema](https://github.com/localstore-platform/specs/blob/v1.1-specs/architecture/graphql-schema.md)
- [API Specification](https://github.com/localstore-platform/specs/blob/v1.1-specs/architecture/api-specification.md)
- [Wireframes & UX Flow](https://github.com/localstore-platform/specs/blob/v1.1-specs/design/wireframes-ux-flow.md)

## Project Structure

```text
dashboard/
├── .github/              # GitHub configuration
│   ├── copilot-instructions.md
│   ├── CODEOWNERS
│   └── pull_request_template.md
├── docs/                 # Documentation
│   ├── SPEC_LINKS.md
│   └── GIT_WORKFLOW.md
├── src/                  # Source code (to be created)
│   ├── app/              # Next.js App Router pages
│   ├── components/       # React components
│   ├── graphql/          # GraphQL queries/mutations
│   ├── hooks/            # Custom React hooks
│   ├── lib/              # Utility functions
│   └── types/            # TypeScript types
├── .env.example          # Environment variables template
├── LICENSE               # AGPL-3.0 License
└── README.md             # This file
```

## Localization

- **Primary Locale:** Vietnamese (vi-VN)
- **Currency:** VND (e.g., 75.000₫)
- **Target Market:** Vietnamese small businesses (restaurants, street food vendors)

## Contributing

1. Follow the [Git Workflow](docs/GIT_WORKFLOW.md) guidelines
2. Create a feature branch from `main`
3. Make changes following the spec
4. Submit a PR using the template

## License

This project is licensed under the [AGPL-3.0 License](LICENSE).
