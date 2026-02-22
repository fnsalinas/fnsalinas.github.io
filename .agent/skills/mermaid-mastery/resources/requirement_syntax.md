# Requirement Diagram Syntax

## Syntax
```mermaid
requirementDiagram

    requirement test_req {
    id: 1
    text: the test requirement
    risk: high
    verifymethod: test
    }

    element test_entity {
    type: simulation
    }

    test_entity - satisfies -> test_req
```

## Elements
- `requirement`: id, text, risk, verifymethod
- `element`: type, docref

## Relationships
- `contains`
- `copies`
- `derives`
- `satisfies`
- `verifies`
- `refines`
- `traces`
