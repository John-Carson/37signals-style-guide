# Unofficial 37signals Coding Style Guide

Transferable Rails patterns and development philosophy extracted from analyzing 265 pull requests in 37signals' Fizzy codebase.

## What This Is

Fizzy is a kanban-style project management app built by 37signals. We analyzed both the final source code AND the process that led to it—pull requests, git commits, code review discussions, and iterations. This dual approach captures not just *what* 37signals builds, but *how* they build it: their decision-making, trade-offs, and evolution of ideas.

## What This Is Not

These are not Fizzy-specific implementation details. We deliberately skipped business logic unique to Fizzy and focused only on patterns you can apply to your own projects.

## Important Caveats

**LLM-Generated Content**: This guide was largely produced by an LLM (Claude) analyzing PR descriptions and code snippets. Given the volume of text and code involved, there may be hallucinations or inaccuracies. Take everything with a grain of salt and verify against actual implementations. That said, I've found it useful as a reference in my own projects.

**Code License**: The code examples extracted from Fizzy are licensed under the [O'Saasy License](https://osaasy.dev). Please review that license before using code snippets in your projects.

---

## Table of Contents

### Core Rails
- [Routing](routing.md) - Everything is CRUD, resource-based patterns, resolve helpers
- [Controllers](controllers.md) - Thin controllers, rich models, composable concerns catalog
- [Models](models.md) - Concerns, state as records, Current context, PORO patterns
- [Views](views.md) - Turbo Streams, partials, fragment caching, view helpers

### Frontend
- [Stimulus](stimulus.md) - Reusable controller catalog with copy-paste code
- [CSS](css.md) - Native CSS, cascade layers, OKLCH colors, modern features
- [Hotwire](hotwire.md) - Turbo Frames/Streams, morphing, drag & drop
- [Accessibility](accessibility.md) - ARIA patterns, keyboard navigation, screen readers
- [Mobile](mobile.md) - Responsive CSS, safe area insets, touch optimization

### Backend
- [Authentication](authentication.md) - Passwordless magic links without Devise
- [Multi-Tenancy](multi-tenancy.md) - Path-based tenancy, middleware, ActiveJob extensions
- [Database](database.md) - UUIDs, state as records, database-backed everything
- [Background Jobs](background-jobs.md) - Solid Queue patterns, tenant preservation, continuable jobs
- [Caching](caching.md) - HTTP caching, fragment caching, invalidation
- [Performance](performance.md) - Preloading, N+1 prevention, memoization

### Real-time & Communication
- [ActionCable](actioncable.md) - Multi-tenant WebSockets, broadcast scoping, Solid Cable
- [Notifications](notifications.md) - Time window bundling, user preferences, real-time
- [Email](email.md) - Multi-tenant mailers, timezone handling

### Features
- [Webhooks](webhooks.md) - SSRF protection, delinquency tracking, state machines
- [Workflows](workflows.md) - Event-driven state, undoable commands
- [Watching](watching.md) - Subscription patterns, toggle UI
- [Filtering](filtering.md) - Filter objects, URL-based state
- [AI/LLM Integration](ai-llm.md) - Command pattern, cost tracking, tool patterns

### Rails Components
- [Active Storage](active-storage.md) - Attachment patterns, variants
- [Action Text](action-text.md) - Sanitizer config, remote images

### Infrastructure & Testing
- [Security Checklist](security-checklist.md) - XSS, CSRF, SSRF, rate limiting, authorization
- [Testing](testing.md) - Minitest, fixtures over factories, integration tests
- [Configuration](configuration.md) - Environment config, Kamal deployment
- [Observability](observability.md) - Structured logging, Yabeda metrics

### Philosophy
- [Development Philosophy](development-philosophy.md)
