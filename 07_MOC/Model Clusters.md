# Model Clusters

Clusters group mental models by discipline so you can explore adjacency and stack ideas faster. Use Dataview queries to surface relevant notes.

## Economics Cluster
```dataview
TABLE file.link AS Model, file.tags
FROM "02_Mental_Models"
WHERE contains(file.tags, "#economics")
SORT file.name
```

## Psychology Cluster
```dataview
TABLE file.link AS Model, file.tags
FROM "02_Mental_Models"
WHERE contains(file.tags, "#psychology")
SORT file.name
```

## Physics Cluster
```dataview
TABLE file.link AS Model, file.tags
FROM "02_Mental_Models"
WHERE contains(file.tags, "#physics")
SORT file.name
```

## Biology Cluster
```dataview
TABLE file.link AS Model, file.tags
FROM "02_Mental_Models"
WHERE contains(file.tags, "#biology")
SORT file.name
```

## Systems Thinking Cluster
```dataview
TABLE file.link AS Model, file.tags
FROM "02_Mental_Models"
WHERE contains(file.tags, "#systems")
SORT file.name
```

## Decision Theory Cluster
```dataview
TABLE file.link AS Model, file.tags
FROM "02_Mental_Models"
WHERE contains(file.tags, "#decision-theory")
SORT file.name
```

Add more clusters (e.g., `#behavior`, `#risk`) as your vocabulary expands. Keep tags aligned with [[Tag Taxonomy]].
