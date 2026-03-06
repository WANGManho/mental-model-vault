# Knowledge Dashboard Index

Use these Dataview-powered slices to navigate every vault collection.

## Principles Index
```dataview
TABLE file.link AS Principle, file.mtime AS Updated
FROM "01_Principles"
SORT file.name
```

## Strategies Index
```dataview
TABLE file.link AS Strategy, file.tags
FROM "03_Strategies"
SORT file.name
```

## Bias Library
```dataview
TABLE file.link AS Bias, file.tags
FROM "04_Cognitive_Bias"
SORT file.name
```

## Case Index
```dataview
TABLE file.link AS Case, file.mtime AS Updated
FROM "05_Cases"
SORT file.name
```

## Mental Model Directory
```dataview
TABLE file.link AS Model, join(file.tags, ", ") AS Tags
FROM "02_Mental_Models"
SORT file.name
```

## Decision Log Index
```dataview
TABLE file.link AS Decision, decision-date, status, review-date
FROM "06_Decisions"
WHERE file.name != "Decision Review"
SORT decision-date DESC
```

## Template Quick Links
- [[Templates/Mental Model Template]]
- [[Templates/Principle Template]]
- [[Templates/Strategy Template]]
- [[Templates/Case Study Template]]
- [[Templates/Decision Log Template]]

Tag this page with `#moc` to keep it visible in the graph.

Tags: #moc #dashboard
