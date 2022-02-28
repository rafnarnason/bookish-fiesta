```mermaid
sequenceDiagram
    autonumber
    Stofnanir->>Advania:sends message
    Advania->>User-Notification-Service:sends message
    User-Notification-Service->>User-Notification-Queue:creates queue message
    Notification-Workers->>User-Notification-Queue:request
    User-Profile-->Notification-Workers:checks settings
    User-Notification-Queue-->>Notification-Workers:response
    Workers->>Firebase:request
    Firebase->island.is-user-client:request
    
    
   
```
