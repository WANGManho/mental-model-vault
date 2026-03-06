# Vault Dashboard

Use this home page as your daily command center. Review quick stats, scan new material, and jump into model clusters or decision reviews.

## Quick Stats
```dataviewjs
const stats = [
  ["Principles", dv.pages("01_Principles").length],
  ["Mental Models", dv.pages("02_Mental_Models").length],
  ["Strategies", dv.pages("03_Strategies").length],
  ["Biases", dv.pages("04_Cognitive_Bias").length],
  ["Cases", dv.pages("05_Cases").length],
  ["Decisions", dv.pages("06_Decisions").where(p => !p.file.name.includes("Review")).length]
];
dv.table(["Collection", "Count"], stats);
```

## Latest Mental Models
```dataview
TABLE file.link AS Model, file.mtime AS Updated, file.tags
FROM "02_Mental_Models"
SORT file.mtime DESC
LIMIT 8
```

## Recently Updated Decisions
```dataview
TABLE file.link AS Decision, decision-date, status, review-date
FROM "06_Decisions"
WHERE file.name != "Decision Review"
SORT file.mtime DESC
LIMIT 5
```

## Decisions Requiring Review
```dataview
TABLE file.link AS Decision, decision-date, review-date, status
FROM "06_Decisions"
WHERE review-date <= date(today)
SORT review-date ASC
```

## Biases to Watch
```dataview
TABLE file.link AS Bias, file.tags
FROM "04_Cognitive_Bias"
SORT file.name
LIMIT 6
```

## Cluster Shortcuts
- [[Model Clusters]] — browse mental models grouped by discipline.
- [[Knowledge Dashboard Index]] — jump to MOCs, templates, and guides.
- [[07_MOC/Mental Models Map|Mental Models Map]] — explore the graph of core ideas.
- [[06_Decisions/Decision Review]] — run structured retrospectives.

Update this dashboard as your workflow evolves.
