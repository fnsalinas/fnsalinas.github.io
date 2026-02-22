# Flowchart Syntax

## Nodes
- **Default**: `id`
- **Text**: `id[Text]`
- **Round**: `id(Text)`
- **Circle**: `id((Text))`
- **Stadium**: `id([Text])`
- **Subroutine**: `id[[Text]]`
- **Cylindrical**: `id[(Text)]`
- **Asymmetric**: `id>Text]`
- **Rhombus**: `id{Text}`
- **Hexagon**: `id{{Text}}`

## Links
- **Arrow**: `A --> B`
- **Open**: `A --- B`
- **Text**: `A -- Text --> B` or `A -->|Text| B`
- **Dotted**: `A -.-> B`
- **Thick**: `A ==> B`

## Direction
- `TD` or `TB`: Top-Down
- `LR`: Left-Right

## Subgraphs
```mermaid
graph TB
    c1-->a2
    subgraph one
    a1-->a2
    end
    subgraph two
    b1-->b2
    end
    subgraph three
    c1-->c2
    end
```

## Styling
```mermaid
graph LR
    id1(Start)-->id2(Stop)
    style id1 fill:#f9f,stroke:#333,stroke-width:4px
    style id2 fill:#bbf,stroke:#f66,stroke-width:2px,color:#fff,stroke-dasharray: 5 5
```
