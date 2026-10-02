# Device Contract

## Device Entity

```json
{
  "device_id": "DEVICE_ID",
  "type": "tagimata_charm",
  "name": "Flagship Charm Prototype",
  "paired_user_id": "USER_ID",
  "capabilities": ["audio_output", "simple_motion", "display", "wifi"],
  "paired_at": "2026-10-01T17:00:00Z",
  "last_seen_at": "2026-10-01T17:30:00Z"
}
```

## Device Types

- `ios_app`
- `meta_glasses`
- `tagimata_charm`
- `unity_vr`
- `development_agent`

## Pairing Principles

- Pairing should be explicit.
- Capabilities should be declared.
- Device permissions should be narrower than user permissions.
- Revocation must be possible before public release.
