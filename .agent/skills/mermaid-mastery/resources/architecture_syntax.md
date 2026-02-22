# Architecture Diagram Syntax

## Syntax
```mermaid
architecture-beta
    group api(cloud)[API]
    
    service db(database)[Database] in api
    service disk1(disk)[Storage] in api
    service server(server)[Server] in api

    db:L -- R:server
    disk1:T -- B:server
```

## Elements
- `group id(icon)[Label]`
- `service id(icon)[Label]`
- `in groupId`: Nesting
- `junction id`

## Icons
- `cloud`, `database`, `disk`, `internet`, `server`
- Extensible via icon packs

## Edges
- `id:Side -- Side:id` (Side: L, R, T, B)
- Arrows: `<` and `>` (e.g., `id:R --> L:id`)
