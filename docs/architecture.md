# Proposed AWS architecture

| Service | Role |
|---|---|
| S3 and Lambda | Shift records and rota exports stored per provider and checked as they arrive |
| SageMaker AI | Workload forecasts per role, retrained weekly |
| ECS/Fargate | The rota service that matches shifts to staff availability |
| DynamoDB | Staff, shifts, recommendations and the approval log |

One AWS account per customer, encrypted at rest and in transit. The public demo calls none of these services.
