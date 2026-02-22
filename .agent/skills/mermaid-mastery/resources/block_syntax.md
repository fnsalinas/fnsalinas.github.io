# Block Diagram Syntax

## Syntax
```mermaid
block-beta
  columns 3
  a:3
  block:group1:2
    b
    c
  end
  d
  a --> b
```

## Features
- `columns <N>`: Set number of columns (default 1)
- `block:id` ... `end`: Group blocks
- `id:width`: Set block width (spanning columns)
- `space`: Skip a cell
- `space:width`: Skip multiple cells
- Arrows: `-->`, `-- text -->`
