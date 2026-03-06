# Mental Model: Feedback Inhibition

## Definition
Feedback inhibition is a biochemical control mechanism where the end product of a process suppresses its own production when concentrations rise too high.

## Core Principle
Balancing loops prevent runaway reactions; monitoring outputs and throttling inputs maintains stability and prevents waste.

## When To Use
- Designing throttles for compute, spending, or hiring to avoid overproduction.
- Automating kill switches or rate limits based on downstream signals.

## Examples
- API rate limiting that slows noisy clients to protect infrastructure.
- Automated budget reviews triggered when burn rate exceeds thresholds.

## Related Models
[[Homeostasis]] · [[Buffering and Slack]] · [[Systems Thinking]]

## Opposite / Failure Cases
- Systems lacking sensors to detect saturation.
- Incentive structures rewarding throughput regardless of downstream impact.

## Sources
- Metabolic pathways such as end-product inhibition of enzymes.

Tags: #mental-model #biology #systems
