# Learning Mermaid

- [Learning Mermaid](#learning-mermaid)
  - [What is mermaid diagram](#what-is-mermaid-diagram)
    - [Flowchart](#flowchart)
      - [Top Down](#top-down)
      - [Left Right](#left-right)
      - [Right Left](#right-left)
      - [Adding labels](#adding-labels)
      - [Adding conditions](#adding-conditions)
    - [Sequence diagram](#sequence-diagram)
    - [Gantt diagram](#gantt-diagram)
    - [Class diagram](#class-diagram)
    - [Git graph](#git-graph)
    - [Entity Relationship Diagram](#entity-relationship-diagram)
    - [User Journey Diagram](#user-journey-diagram)

## What is mermaid diagram

It is a JavaScript based diagramming and charting tool that renders Markdown-inspired text definitions to create and modify diagrams dynamically.

- Flowchart
- Sequence diagram
- Gantt diagram
- Class diagram
- Git graph
- Entity Relationship Diagram
- User Journey Diagram

### Flowchart

#### Top Down

~~~txt
  ```mermaid
  graph TD
  A --> B;
  A --> C;
  C --> D;
  B --> E;
  D --> F;
  E --> F;
  ```
~~~

__Output:__

```mermaid
graph
A --> B;
A --> C;
C --> D;
B --> E;
D --> F;
E --> F;
```

#### Left Right

~~~txt
  ```mermaid
  graph LR
  A --> B;
  A --> C;
  C --> D;
  B --> E;
  D --> F;
  E --> F;
  ```
~~~

__Output:__

```mermaid
graph LR
  A --> B;
  A --> C;
  C --> D;
  B --> E;
  D --> F;
  E --> F;
```

#### Right Left

~~~txt
  ```mermaid
  graph RL
  A --> B;
  A --> C;
  C --> D;
  B --> E;
  D --> F;
  E --> F;
  ```
~~~

__Output:__

```mermaid
graph RL
A --> B;
A --> C;
C --> D;
B --> E;
D --> F;
E --> F;
```

#### Adding labels

To add Labels on a flowchart we simply use brackets `[]`

~~~txt
  ```mermaid
  graph LR
  A[Start] --> B[Input value];
  B --> C[Process values];
  C --> D[Finish];
  ```
~~~

__Output:__

```mermaid
graph LR
A[Start] --> B[Input value];
B --> C[Process values];
C --> D[Finish];
```

#### Adding conditions  

To add conditions to the flowchart we use curly braces `{}` and to add response we use pipes `||`

~~~txt
  ```mermaid
  graph TD
  A[Start] --> B[Input value];
  B --> C{Value is over 18?};
  C --> |Yes| D[Retrieve data];
  C --> |No| E[Decline access];
  ```
~~~

__Output:__

```mermaid
graph TD
A[Start] --> B[Input value];
B --> C{Value is over 18?};
C --> |Yes| D[Retrieve data];
C --> |No| E[Decline access];
```

### Sequence diagram

### Gantt diagram

### Class diagram

### Git graph

### Entity Relationship Diagram

### User Journey Diagram
