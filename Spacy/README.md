```mermaid
graph TD;
    A[User Query] -->|Check Retrieval Quality| B{Decision Layer};
    B -->|Context is Sufficient| C[Generate Response with LLM];
    B -->|Context is Insufficient| D[Search Internal Documents];
    D --> E[Retrieve Additional Context];
    E --> C;
    C --> F[Final Response to User];

