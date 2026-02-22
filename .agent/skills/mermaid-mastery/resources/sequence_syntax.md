# Sequence Diagram Syntax

## Participants
```mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>Bob: Hello Bob, how are you?
    Bob-->>Alice: I am good thanks!
```

## Messages
- `-> `: Solid line without arrow
- `-->`: Dotted line without arrow
- `->>`: Solid line with arrowhead
- `-->>`: Dotted line with arrowhead
- `-x`: Solid line with cross at end
- `--x`: Dotted line with cross at end

## Activations
```mermaid
sequenceDiagram
    Alice->>Bob: Hello Bob, how are you?
    activate Bob
    Bob-->>Alice: I am good thanks!
    deactivate Bob
```
Shortcut: `Alice->>+Bob: Hello` and `Bob-->>-Alice: Hi`

## Loops, Alt, Opt
```mermaid
sequenceDiagram
    loop Every day
        Alice->>Bob: Hello
    end
    alt is sick
        Bob-->>Alice: Not so good
    else is well
        Bob-->>Alice: Feeling fresh
    end
    opt Extra
        Bob-->>Alice: Thanks for asking
    end
```

## Notes
`Note right of Bob: Bob thinks`
`Note over Alice,Bob: A typical interaction`
