# Architecture Overview (High Level)

Conceptual view only — no implementation, hosting, or security details.

```mermaid
flowchart LR
    M[Alliance members] --> D[Discord]
    L[Alliance leadership] --> W[Web Command Center]
    L --> D
    D <--> B[Bot service]
    W <--> A[Platform API]
    B <--> A
    A --> S[(Tenant data store)]
    A --> AI[AI providers]
    A --> N[Scheduling and notifications]
    N --> D
```

- **Per-alliance tenancy:** each customer alliance has its own configuration and data boundary.
- **Discord as delivery channel:** the platform is the system of record; Discord carries notifications and commands.
- **Guarded AI usage:** AI calls pass through cost and access controls.
