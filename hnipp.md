```mermaid
sequenceDiagram
    autonumber
    Stofnanir->>Advania:sends message
    Advania->>User-Notification-Service:sends message
    User-Notification-Service->>User-Notification-Queue:creates message
    Workers->>User-Notification-Queue:request
    Workers->>Firebase:request
    Firebase->island.is-user-client:request
    
    
   
```
