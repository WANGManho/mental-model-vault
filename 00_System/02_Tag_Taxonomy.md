# Tag Taxonomy

Use consistent tags so Dataview queries and graph filters stay meaningful.

## Core Tags
- `#mental-model` — all model notes in `02_Mental_Models`.
- `#principle` — foundational ideas in `01_Principles`.
- `#strategy` — playbooks and decision frameworks in `03_Strategies`.
- `#bias` — human biases and heuristics in `04_Cognitive_Bias`.
- `#case` — real-world examples stored in `05_Cases`.
- `#decision` — logs and reviews in `06_Decisions`.

## Discipline Tags
Add one or more discipline tags to each mental model for clustering:
- `#economics`
- `#psychology`
- `#physics`
- `#biology`
- `#systems`
- `#decision-theory`

## Workflow Tags
- `#moc` for Maps of Content and dashboards in `07_MOC`.
- `#inbox` for fleeting notes awaiting processing (use in `00_System`).
- `#review` for decisions or cases requiring follow-up.

## Dataview Examples
List all psychology models:

```dataview
TABLE file.link AS Model, file.mtime AS Updated
FROM "02_Mental_Models"
WHERE contains(file.tags, "#psychology")
SORT file.name
```

Queue of notes tagged for review:

```dataview
TASK
FROM #review
WHERE !completed
SORT due ASC
```

Keep this taxonomy updated whenever you introduce new tag families.
