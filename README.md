# Swagger API Specification
- [OpenAPI Specification](./OpenAPISpecification.json) - The API specification file
- [Swagger Editor](https://editor.swagger.io/) - View online
- [Swagger UI](http://localhost:4000/swagger-ui/index.html#/) - Interactive API for local

## Build status 
### Backend
![CI](https://github.com/hmcts/hmcts-dev-test-backend/actions/workflows/ci.yml/badge.svg)

### High level flow
```mermaid 
sequenceDiagram
    actor CW as Case Worker
    participant FE 
    participant API
    participant DB as H2
    
    CW->>FE: Create/View/Update/Delete Task
    FE->>API: HTTP Request
    API->>API: Validate Input & process
    API->>DB: Read/Write Data
    DB-->>API: Data Response
    API-->>FE: JSON + HATEOAS Links
    FE-->>CW: Display Result
```

## Performance/ improvements
## TODO 
