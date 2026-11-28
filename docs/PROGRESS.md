# Project Atlas — Progress

## Current Status

- Phase: Month 1 — Foundations
- Week: 1
- Stage: Customer Discovery
- Started: 2026-11-26

## Completed

- [x] Establish master project specification
- [x] Initialize local Git repository
- [x] Verify Python 3.13.2
- [x] Install and verify uv
- [x] Verify Docker and Docker Compose
- [x] Verify GitHub CLI and authentication
- [x] Verify AWS CLI installation
- [x] Configure VS Code and Codex
- [x] Establish AGENTS.md
- [x] Establish CLAUDE.md
- [x] Configure .gitignore
- [x] Initialize pyproject.toml
- [x] Create Python virtual environment
- [x] Pin Python version
- [x] Generate uv.lock
- [x] Populate persistent project documentation
- [x] Create GitHub repository at `schradermade/atlas`
- [x] Push initial commit `a7f87d6`
- [x] Verify local `main` and `origin/main` are synchronized
- [x] Complete project initialization
- [x] Complete ATL-003 — Repository and Environment
- [x] Start ATL-001 — Customer Discovery
- [x] Draft `docs/architecture/001-customer-discovery.md`

## Technical Decisions

- Python 3.13.2
- uv for dependency and environment management
- Docker for local infrastructure
- GitHub for version control
- VS Code as primary development environment
- Codex as the primary Atlas mentoring and workflow environment
- Local-first development
- Modular monolith as initial architecture
- Native implementations before higher-level abstractions
- Learning Mode as default AI collaboration mode
- Discovery deliverables should distinguish confirmed alignment, provisional targets, scope boundaries, and outstanding questions before architecture design begins
- V1 product scope boundaries should be documented separately from items out of scope for a discovery document
- GitHub remote established at `github.com/schradermade/atlas`
- Repository baseline captured in initial commit `a7f87d6`

## Deferred

- Claude Code installation
- AWS authentication and resource provisioning
- Application dependency installation
- Distributed infrastructure
- Production deployment

## Open Items

- Resolve pilot scope for ATL-001, including selected incident categories, low-complexity definition, and pilot users
- Confirm integration and security constraints, including accessible systems, auth/network controls, and API limitations
- Define evaluation and release criteria, including sample size, review method, and thresholds for progressing beyond discovery

## Known Technical Concerns

- Docker reports a non-default seccomp profile.
- Existing Docker containers may introduce port conflicts.
- Revisit both before infrastructure and security testing.

## Blockers

None currently identified.

## Next Assignment

ATL-001: Prepare follow-on technical discovery questions and complete customer discovery
