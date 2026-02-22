# Kanban Diagram Syntax

## Syntax
```mermaid
kanban
  todo[To Do]
    task1[Create Database]
    task2[Design UI]
  doing[In Progress]
    task3[Implement API]
  done[Done]
    task4[Setup Server]
```

## Metadata
- `task@{ ticket: "PROJ-123", priority: "High", assigned: "Alice" }`
- Global config: `ticketBaseUrl`

## Structure
- `columnId[Title]`
  - Indented `taskId[Description]`
