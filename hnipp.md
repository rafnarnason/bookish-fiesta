```mermaid
sequenceDiagram
    autonumber
    Stofnanir->>Advania:request
    Advania->User-Notification:x-road
    User-Notification->Queue:request
    Workers->Queue:request
    Workers->>Firebase:request
    Firebase->Island.is-client:request
    
    
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
```
