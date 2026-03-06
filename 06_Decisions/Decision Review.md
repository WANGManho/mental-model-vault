# Decision Review

Run this review monthly to evaluate outcomes, reinforce learning, and update playbooks.

## Review Queue
```dataview
TABLE file.link AS Decision, decision-date, review-date, status, models-used
FROM "06_Decisions"
WHERE review-date <= date(today) OR status != "Closed"
SORT review-date ASC
```

## Recently Closed Decisions
```dataview
TABLE file.link AS Decision, decision-date, review-date
FROM "06_Decisions"
WHERE status = "Closed"
SORT review-date DESC
LIMIT 5
```

## Prompts
- Do referenced models still feel appropriate?
- Which biases showed up despite planning?
- What new cases or principles should be linked?
- Should any strategy or model templates be updated based on this outcome?

Tag completed reviews with `#review` for historical tracking.
