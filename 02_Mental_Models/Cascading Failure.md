# Mental Model: Cascading Failure

## Definition
Cascading failure occurs when the failure of one component triggers subsequent failures, rapidly collapsing an interconnected system.

## Core Principle
Tightly coupled systems lack buffers, so local issues propagate widely; designing isolation and redundancy reduces cascade risk.

## When To Use
- Infrastructure, finance, or supply chains with dependencies.
- Organizational change where teams rely heavily on each other.

## Examples
- Power grids tripping sequentially after a single line overloads.
- Software outages propagating through microservices without circuit breakers.

## Related Models
[[Buffering and Slack]] · [[Stock and Flow]] · [[Systems Thinking]]

## Opposite / Failure Cases
- Loosely coupled architectures with graceful degradation.
- Systems with clear firebreaks and throttles that contain issues.

## Sources
- Reliability engineering and network theory.

Tags: #mental-model #systems #risk
