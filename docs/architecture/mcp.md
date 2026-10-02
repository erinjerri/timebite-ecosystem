# MCP And Connector Architecture

## Purpose

MCP is useful when TimeBite needs agent/tool style integration, external service connectors, repeatable automation, or cross-platform orchestration. It should not replace direct native APIs that are simpler and safer inside the production iOS app.

## Proposed Structure

```text
mcp/
  servers/
  clients/
  tools/
  connectors/

integrations/
  apple/
  meta/
  notion/
  calendar/
  health/
  ai-providers/

packages/
  timebite-actions/
  timebite-schema/
  device-protocol/
```

## MCP Candidates

Good MCP candidates:

- Notion/project knowledge ingestion
- agent-accessible TimeBite action tools
- integration test harnesses
- planner ingestion experiments
- cross-repo contract validation

Prefer direct native APIs:

- HealthKit
- iOS local notifications
- on-device SwiftData
- first-party calendar access inside the iOS app
- App Store auth flows

## Canonical Tool Surface

MCP tools, wearable calls, and device calls should map back to shared TimeBite actions. MCP should be an adapter, not a competing product model.
