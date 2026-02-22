# Treemap Diagram Syntax

## Syntax
```mermaid
treemap
    "Root"
        "Category A"
            "Item 1": 10
            "Item 2": 20
        "Category B"
            "Item 3": 15
```

## Structure
- Hierarchy defined by indentation
- Leaf nodes have values: `"Name": value`
- Parent nodes just have names: `"Name"`
- CSS classes with `:::className`
