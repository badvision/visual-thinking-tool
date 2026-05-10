# Visual Thinking Tool

**Map goals, challenges, and the forces between them.**

🔗 **[Try it live → badvision.github.io/visual-thinking-tool](https://badvision.github.io/visual-thinking-tool)**

---

Nodes represent ideas, goals, or realities. Edges represent the relationship between them — whether they **attract** (pull together) or **repel** (push apart). The physics engine shows you where equilibrium actually lands.

Great for exploring team dynamics, competing priorities, organizational forces, or any system where things pull toward or away from each other.

## See it in action

Click **Sample** in the toolbar to load a pre-built graph of a team navigating two competing norms. Watch how the practices on each side pull the Team node toward the norm they reinforce — then start connecting the Team to different practices to see how the balance shifts.

## Quick Start

| Action | How |
|--------|-----|
| **Add a node** | Double-click empty canvas |
| **Connect nodes** | Shift+drag from one node to another, or use Connect Mode in the toolbar |
| **Set edge type** | Select an edge — choose Attract or Repel in the properties panel |
| **Adjust force strength** | Drag the weight slider (stronger = shorter for attract, farther for repel) |
| **Edit / delete** | Click to select, then edit in the panel or press Delete |
| **Undo / redo** | Cmd+Z / Cmd+Shift+Z |
| **Pan** | Drag canvas, or right/middle-click drag |
| **Zoom** | Scroll wheel; use Fit to frame everything |
| **Save / Load** | Saves a JSON file you can reload later |

## How it works

Nodes and edges form a physics simulation using [D3-force](https://github.com/d3/d3-force). Each edge has a **weight** (0–1) and a **type**:

- **Attract** — higher weight pulls nodes closer together (shorter resting distance)
- **Repel** — higher weight pushes nodes further apart (longer resting distance)

Edge color encodes force strength: **red** = strong, **blue** = weak. Repel edges are shown as dashed lines.

The Team node in the sample has no direct connection to either norm — only to the practices the team currently exhibits. The physics shows where that puts them, and you can explore "what if we also adopted X?" by drawing new connections.

## Running locally

No build step required. Just open `index.html` in a browser:

```bash
git clone https://github.com/badvision/visual-thinking-tool.git
cd visual-thinking-tool
open index.html
```

All dependencies (D3 v7) are inlined — works fully offline.
