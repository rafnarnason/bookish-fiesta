```mermaid
sequenceDiagram
    autonumber
    Stofnanir->>Advania:skeyti
    Advania->>User-Notification:x-road message
    User-Notification-Service->Queue:creates message
    Workers->Queue:request
    Workers->>Firebase:request
    Firebase->island.is-user-client:request
    
    
   
```
