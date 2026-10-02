# TimeBite Ecosystem

Master architecture, systems-design, integration, shared-contract, MCP, and cross-product orchestration repository for the TimeBite x Tagimata ecosystem.

This is the control-plane repository. It defines how the production iOS app, Meta interfaces, VR prototype, Tagimata fashion, purses, and interactive robotic charms connect through one shared TimeBite context layer.

It is not the production iOS app, fashion design repo, Meta glasses implementation repo, Unity repo, or embedded firmware repo.

## Source Of Truth

- [ARCHITECTURE.md](ARCHITECTURE.md) defines the ecosystem architecture.
- [docs/architecture/tech-stack.md](docs/architecture/tech-stack.md) maps the internal implementation stacks across child repositories.
- [ROADMAP.md](ROADMAP.md) defines the October 2026 through September 2027 implementation roadmap.
- [REPO-MAP.md](REPO-MAP.md) defines repository ownership boundaries.
- [docs/product/master-gantt.md](docs/product/master-gantt.md) is the master Gantt.
- [docs/product/milestones.md](docs/product/milestones.md) defines milestone gates.

## Design Principle

TimeBite provides intent, context, memory, and execution. Meta provides wearable and spatial interfaces. Tagimata provides fashion and physical expression. The interactive charm provides embodied interaction. This repository keeps those paths connected without turning them into six disconnected products.

## Repository Structure

```text
docs/
  architecture/    Ecosystem, software, hardware, Meta, MCP, data, AI design.
  product/         Roadmap, Gantt, milestones, critical path, costs, risks.
  fashion/         Initial looks and purse roadmap.
  hardware/        Charm, M5Stack, ESP32, manufacturing readiness.
  decisions/       Architecture decision records.

specs/
  actions/         Shared TimeBite action contracts.
  devices/         Device model and pairing contracts.
  events/          Cross-interface event model.
  data-model/      Canonical entities.

mcp/               MCP and connector hub design.
integrations/      Integration inventory and ownership.
codex/prompts/     Implementation prompts for child repositories.
```

## First Ecosystem Thesis

Prove one identity, one TimeBite context, and many interfaces:

1. The iOS app owns the production TimeBite experience.
2. Meta glasses and the charm invoke shared TimeBite actions.
3. Tagimata looks and purse make the technology physically coherent.
4. The VR prototype remains a bounded experiment.
5. The first robotic charm uses one M5Stack platform before any custom PCB work.
