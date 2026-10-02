# Integrations

## Integration Inventory

| Integration | Preferred Path | Notes |
| --- | --- | --- |
| Apple Calendar | Native iOS first | MCP only for agent-side testing if needed |
| HealthKit | Native iOS | Do not route through MCP |
| Meta glasses | Meta-specific interface + TimeBite actions | Capability verification required |
| Unity/Quest | Prototype adapter | Mock most production services |
| Notion | MCP candidate | Useful for planning/docs/knowledge |
| AI providers | Provider adapter | Keep provider swappable |
| Charm | Device protocol + TimeBite actions | May start through local relay or simple API |

## Principle

Each integration is an adapter onto TimeBite actions, not a new product model.
