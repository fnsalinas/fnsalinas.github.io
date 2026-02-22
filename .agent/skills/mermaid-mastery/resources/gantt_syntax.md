# Gantt Chart Syntax

## Basic Structure
```mermaid
gantt
    title A Gantt Diagram
    dateFormat  YYYY-MM-DD
    section Section
    A task           :a1, 2014-01-01, 30d
    Another task     :after a1  , 20d
    section Another
    Task in sec      :2014-01-12  , 12d
    another task      : 24d
```

## Configuration
- `dateFormat`: e.g., `YYYY-MM-DD`
- `axisFormat`: e.g., `%m/%d`
- `excludes`: `weekends`, `sunday`

## Task States
- `done`: Completed task
- `active`: Currently active
- `crit`: Critical path
- `milestone`: Milestone (diamond shape)

## Dependencies
- `after id`: Starts after task `id`
- `until id`: Runs until task `id` starts
