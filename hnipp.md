```mermaid
sequenceDiagram
    autonumber
    Stofnanir->>Advania:skeyti
    Advania->>User-Notification-Service:xroad skeyti
    User-Notification-Service->>User-Notification-Queue:creates queue message
    Notification-Workers->>User-Notification-Queue:request
    User-Notification-Queue-->>Notification-Workers:response
    Notification-Workers-->>User-Profile:auto-auth get settings
    User-Profile-->>Notification-Workers:return settings
    
    Notification-Workers->>Firebase:request
    Firebase->>island.is-user-client:hnipp
    
    
   
```
