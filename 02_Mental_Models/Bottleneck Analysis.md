# Mental Model: Bottleneck Analysis

## Definition
Bottleneck analysis identifies the constraint that most limits throughput in a system and focuses improvements there before expanding elsewhere.

## Core Principle
A chain is only as strong as its weakest link; optimizing non-bottleneck steps wastes effort until the constraint is relieved.

## When To Use
- Manufacturing, supply chain, or software pipelines with uneven flow.
- Process improvement initiatives where resources are scarce.

## Examples
- Database locks throttling an entire web service despite idle compute.
- Legal review queues slowing product launches regardless of upstream speed.

## Related Models
[[Diminishing Returns]] · [[Stock and Flow]] · [[Pareto Principle]]

## Opposite / Failure Cases
- Systems with multiple interacting constraints requiring holistic redesign.
- Environments where demand rather than throughput is limiting.

## Sources
- Theory of Constraints by Eliyahu Goldratt.

Tags: #mental-model #systems #operations
