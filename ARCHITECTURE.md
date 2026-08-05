# Architecture

## System overview

```mermaid
flowchart TB
    N0["Flutter Mobile App"]
    N1["Web Dashboard"]
    N2["Node.js / Express API"]
    N3["PostgreSQL / MongoDB"]
    N0 --> N1
    N1 --> N2
    N2 --> N3
```

| Layer | Responsibility |
|---|---|
| Flutter Mobile App | Technician job view, status updates, signatures, photo capture |
| Web Dashboard | Dispatcher scheduling and job tracking |
| Node.js / Express API | Job and scheduling backend |
| PostgreSQL / MongoDB | Job, customer, and scheduling data |

## Job assignment flow

```mermaid
sequenceDiagram
    participant Dispatcher
    participant API
    participant Mobile App
    participant Technician
    participant Dashboard

    Dispatcher->>API: Create job + assign technician
    API->>Mobile App: Push job notification
    Technician->>Mobile App: Accept + update status
    Mobile App->>API: Sync status (Socket.IO)
    API-->>Dashboard: Real-time status update
```
