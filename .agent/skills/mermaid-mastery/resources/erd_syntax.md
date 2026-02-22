# Entity Relationship Diagram Syntax

## Syntax
`FirstEntity [Relationship] SecondEntity : Label`

## Cardinality
- `|o` : Zero or one
- `||` : Exactly one
- `}o` : Zero or more
- `}|` : One or more

## Relationships
- `..` : Dashed
- `--` : Solid

## Example
```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```

## Attributes
```mermaid
erDiagram
    CUSTOMER {
        string name
        string custNumber
        string sector
    }
```
