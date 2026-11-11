# League Coach

A Claude skill that gives League of Legends matchup, build, rune and draft
advice from live OP.GG data. Ask things like:

- "I'm playing Ahri into Zed mid, how should I play it?"
- "What do I build on Jinx against three tanks?"
- "What should I ban in top lane right now?"
- "Look at my last 10 games, Name#TAG on EUW, and tell me what to fix."

## Setup (two steps)

### 1. Connect OP.GG

The skill reads its data from OP.GG's public MCP server. No API key needed.

- **Claude desktop / web:** Settings → Connectors → Add custom connector →
  `https://mcp-api.op.gg/mcp`
- **Claude Code:**

  ```bash
  claude mcp add --transport http opgg https://mcp-api.op.gg/mcp
  ```

### 2. Install the skill

- **Claude Code and other coding agents:** one command:

  ```bash
  npx skills add jayPreak/league-coach --skill league-coach -g
  ```

- **Claude desktop / web:** Settings → Capabilities → Skills → Upload skill →
  choose `league-coach.zip`

Then start a new chat and ask a League question.

## Notes

- Advice is for champion select, drafting and reviewing games, not live
  in-game tracking.
- League Coach isn't endorsed by Riot Games or OP.GG and doesn't reflect the
  views or opinions of Riot Games or anyone officially involved in producing
  or managing Riot Games properties.
