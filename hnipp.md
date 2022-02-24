```mermaid
sequenceDiagram
    autonumber
    Stofnanir->>Advania:request
    Advania->User-Notification:x-road
    User-Notification->Queue:request
    Workers->Queue:request
    Workers->>Firebase:request
    Firebase->island.is-user-client:request
    
    
   
```
