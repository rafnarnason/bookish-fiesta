```mermaid
sequenceDiagram
    autonumber
    Stofnanir->>Advania:skeyti
    Advania->>User-Notification-Service:xroad skeyti
    User-Notification-Service->>AWS SQS:creates queue message
    Notification-Workers->>AWS SQS:request
    AWS SQS-->>Notification-Workers:response
    Notification-Workers-->>User-Profile:enhancedFetch auto-auth :notification-settings
    User-Profile-->>Notification-Workers:return settings
    
    Notification-Workers->>Firebase:request
    Firebase->>island.is-user-client:hnipp
    
    
   
```
