# Pi-lean fork

This fork preserves context-mode behavior while reducing Pi's always-on prompt cost.

Pi-specific changes:

- Replace verbose MCP tool descriptions with concise selection cues.
- Remove prose-only JSON Schema annotations while preserving validation keywords.
- Bound descriptions for future MCP tools to 240 characters.
- Reduce the per-turn routing anchor.
- Advertise only the main `context-mode` skill to Pi; maintenance tools remain callable.

The upstream MCP descriptions remain unchanged for other clients.

Measured against v1.0.169's 11-tool surface:

- Original Pi tool metadata: 27,750 characters
- Fork Pi tool metadata: 4,370 characters
- Reduction: 23,380 characters (84%), approximately 5,845 tokens
