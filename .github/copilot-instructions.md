# GitHub Copilot Instructions – Dashboard

Extends the global instructions from [specs/.github/copilot-instructions.md](https://github.com/localstore-platform/specs/blob/v1.1-specs/.github/copilot-instructions.md).

## Repository Context

- **Repository:** dashboard
- **Type:** Next.js 14 Admin Dashboard
- **Tech Stack:** Next.js 14 + TypeScript, Apollo GraphQL Client, Tailwind CSS 3, Socket.io client (WebSocket)
- **Spec Version:** v1.1-specs
- **Spec Links:** See [docs/SPEC_LINKS.md](../docs/SPEC_LINKS.md)

## Specific Guidelines

### Code Style

- Use TypeScript strict mode for all code
- Follow Next.js 14 App Router conventions
- Use server components by default, client components only when necessary
- Prefer React Server Components for data fetching
- Use Tailwind CSS for styling, avoid inline styles
- Component naming: PascalCase for components, camelCase for utilities

### Architecture Patterns

- Feature-based folder structure under `src/`
- Shared components in `src/components/`
- GraphQL queries/mutations in `src/graphql/`
- Custom hooks in `src/hooks/`
- Utility functions in `src/lib/`
- Type definitions in `src/types/`

### Testing Requirements

- Unit tests for utility functions and hooks
- Component tests using React Testing Library
- E2E tests for critical user flows
- Test Vietnamese locale formatting (dates, currency)
- Minimum 80% coverage for critical paths

### Vietnamese Localization

- Default locale: `vi-VN`
- Currency format: VND with thousands separator (e.g., 75.000₫)
- Date format: `dd/MM/yyyy`
- Use next-intl or similar for i18n
- All user-facing strings must support Vietnamese

## Git Workflow

**IMPORTANT**: Follow the git workflow defined in [docs/GIT_WORKFLOW.md](../docs/GIT_WORKFLOW.md).

Key rules:

- **Never commit directly to main branch**
- If on main, create a new branch before committing
- Branch naming: `<type>/<short-description>` (e.g., `feat/add-menu-editor`)
- Commit changes logically (group related changes)
- After commits, create/update PR to main branch
- Use conventional commit messages

### Commit Granularity Principle

Each commit should answer ONE of these questions:

- "What single feature/fix does this add?"
- "What single purpose do these files serve together?"

**Rule of thumb:** If you need "and" to describe the commit, split it.

- ❌ `Add docs and config files` → Split
- ❌ `Update README and add environment template` → Split
- ✅ `Add GitHub PR template and CODEOWNERS` → OK (same purpose: GitHub config)
- ✅ `Add specification links documentation` → OK (single purpose)

## Common Tasks

### Adding a New Feature

1. Check SPEC_LINKS.md for relevant specifications
2. Load spec sections using semantic_search
3. Implement following spec exactly
4. Add tests matching spec examples
5. Update documentation

### Adding a New Dashboard Page

1. Create page in `src/app/(dashboard)/[route]/page.tsx`
2. Add GraphQL queries in `src/graphql/queries/`
3. Create components in `src/components/[feature]/`
4. Add to navigation in `src/components/layout/Sidebar.tsx`
5. Test responsive layout (mobile, tablet, desktop)

### Working with GraphQL

1. Define queries/mutations in `src/graphql/`
2. Use Apollo Client hooks (`useQuery`, `useMutation`)
3. Handle loading and error states
4. Implement optimistic updates for mutations
5. Use subscriptions for real-time updates

### Updating API Contracts

1. Ensure contracts repository is updated first
2. Update this repository to use new contract version
3. Run contract tests
4. Update API documentation

## Performance Guidelines

- Target <2s Time to Interactive (TTI) on 4G networks
- Use Next.js Image component for images
- Implement lazy loading for below-fold content
- Bundle size budget: <150KB initial JS
- Use dynamic imports for heavy components

## Related Documentation

- [Main Specs Repository](https://github.com/localstore-platform/specs)
- [AI Context Guide](https://github.com/localstore-platform/specs/blob/v1.1-specs/.github/AI_CONTEXT_GUIDE.md)
- [Spec Changelog](https://github.com/localstore-platform/specs/blob/v1.1-specs/SPEC_CHANGELOG.md)
