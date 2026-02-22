# ZenUML Syntax

## Syntax
```mermaid
zenuml
    Client->Service: Request
    Service->Database: Query
    Database->Service: Result
    Service->Client: Response
```

## Features
- `Participant: message`
- `A -> B: Sync message`
- `A ->> B: Async message`
- `new A`: Creation
- `// comment`
- `opt`, `loop`, `alt`, `try`, `catch`, `finally` block structures
- `group`
