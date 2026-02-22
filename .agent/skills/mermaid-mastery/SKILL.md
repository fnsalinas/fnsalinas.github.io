---
name: mermaid-mastery
description: Comprehensive knowledge base and utilities for all Mermaid.js diagram types.
---

# Mermaid Mastery Skill

> **Purpose**: Provide expert knowledge on syntax, best practices, and generation of Mermaid diagrams.

## 📚 Resources

This skill includes detailed syntax guides for:

- **Flowcharts**: `resources/flowchart_syntax.md`
- **Sequence Diagrams**: `resources/sequence_syntax.md`
- **Class Diagrams**: `resources/class_syntax.md`
- **State Diagrams**: `resources/state_syntax.md`
- **Entity Relationship**: `resources/erd_syntax.md`
- **User Journey**: `resources/user_journey_syntax.md`
- **Gantt Charts**: `resources/gantt_syntax.md`
- **Pie Charts**: `resources/pie_syntax.md`
- **Quadrant Charts**: `resources/quadrant_syntax.md`
- **Requirement Diagrams**: `resources/requirement_syntax.md`
- **GitGraph**: `resources/gitgraph_syntax.md`
- **C4 Diagrams**: `resources/c4_syntax.md`
- **Mindmaps**: `resources/mindmap_syntax.md`
- **Timeline**: `resources/timeline_syntax.md`
- **ZenUML**: `resources/zenuml_syntax.md`
- **Sankey**: `resources/sankey_syntax.md`
- **XY Chart**: `resources/xychart_syntax.md`
- **Block Diagram**: `resources/block_syntax.md`
- **Packet Diagram**: `resources/packet_syntax.md`
- **Kanban**: `resources/kanban_syntax.md`
- **Architecture**: `resources/architecture_syntax.md`
- **Radar**: `resources/radar_syntax.md`
- **Treemap**: `resources/treemap_syntax.md`

## 💡 Best Practices

### Flowcharts
- Use `graph TD` for hierarchical structures.
- Use `graph LR` for timelines or processes.
- Use subgraphs to group related nodes.
- Use `classDef` to style nodes consistently.

### Sequence Diagrams
- Use `participant` to define order.
- Use `activate` and `deactivate` to show processing time.
- Use `loop`, `alt`, `opt` for control flow.

### General
- Always quote labels that contain special characters: `id["Label with (text)"]`.
- Use descriptive IDs for nodes (`loginBtn` instead of `A`).

## 🛠️ Common Commands

### Generate Image (MANDATORY)
Mermaid diagrams MUST always be exported to an image and embedded in the markdown file using a relative path (e.g., `![Diagram Name](diagram.png)`). Never leave the raw code block in the final output.

To generate an image from a mermaid file:

```bash
npx -y @mermaid-js/mermaid-cli -i input.mmd -o output.png -b transparent
```

### Background Options
To use a transparent background (if supported by theme) or set a specific background color, check `mmdc --help`.
