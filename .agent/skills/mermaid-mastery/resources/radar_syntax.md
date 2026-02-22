# Radar Diagram Syntax

## Syntax
```mermaid
radar-beta
    title "Team Skill Analysis"
    axis knowledge [Knowledge], coding [Coding], soft [Soft Skills]
    
    curve alice [Alice] { knowledge: 80, coding: 90, soft: 70 }
    curve bob [Bob] { knowledge: 60, coding: 70, soft: 90 }
```

## Configuration
- `showLegend true|false`
- `max <value>`, `min <value>`
- `graticule circle|polygon`
- `ticks <number>`

## Data
- `axis id [Label]`
- `curve id [Label] { axis: value, ... }`
