# SmartQueue---Adaptive-Load-Shedding-Fair-Queuing-Gateway-for-SaaS-APIs

Designed a multi-tenant API gateway that replaces static rate limits with adaptive weighted fair queuing,
dynamically reallocating capacity from learned per-tenant traffic patterns and priority decay for tenants exceeding
their fair share.
• Implemented Redis-backed token accounting for sub-millisecond fairness decisions and BullMQ-based request
queuing, deferring excess traffic instead of hard-rejecting it during load spikes.
• Built a synthetic load-generation and chaos-testing mode simulating multi-tenant traffic spikes to validate fairness
guarantees and recovery behavior under sustained overload.
• Developed a real-time React dashboard over WebSockets visualizing per-tenant throttling decisions, queue depth,
and capacity allocation for full traffic transparency.
• Provisioned multi-tenant infrastructure (ECS Fargate, ALB) with Terraform and shipped a Jenkins CI/CD pipeline
with Prometheus and Grafana dashboards tracking latency and fairness metrics.