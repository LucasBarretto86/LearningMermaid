# Learning Mermaid

- [Learning Mermaid](#learning-mermaid)
  - [What is mermaid diagram](#what-is-mermaid-diagram)
  - [Flowchart](#flowchart)
    - [Orientation](#orientation)
      - [Default (Top Bottom / Top Down)](#default-top-bottom--top-down)
      - [Left Right](#left-right)
      - [Right Left](#right-left)
    - [Shapes](#shapes)
    - [Arrows and Links](#arrows-and-links)
      - [Arrow](#arrow)
      - [Thicker Arrow](#thicker-arrow)
      - [Open link](#open-link)
      - [Dotted arrow](#dotted-arrow)
    - [Adding labels](#adding-labels)
    - [Adding conditions](#adding-conditions)
  - [Sequence diagram](#sequence-diagram)
  - [Gantt diagram](#gantt-diagram)
  - [Class diagram](#class-diagram)
  - [Git graph](#git-graph)
  - [Entity Relationship Diagram](#entity-relationship-diagram)
  - [User Journey Diagram](#user-journey-diagram)
  - [References](#references)

## What is mermaid diagram

It is a JavaScript based diagramming and charting tool that renders Markdown-inspired text definitions to create and modify diagrams dynamically.

- Flowchart
- Sequence diagram
- Gantt diagram
- Class diagram
- Git graph
- Entity Relationship Diagram
- User Journey Diagram

## Flowchart

### Orientation

- TB - top to bottom
- TD - top-down/ same as top to bottom
- BT - bottom to top
- RL - right to left
- LR - left to right

#### Default (Top Bottom / Top Down)

~~~txt
  ```mermaid
  graph TD
    A --> B
    A --> C
    C --> D
    B --> E
    D --> F
    E --> F
  ```
~~~

__Output:__

```mermaid
graph
A --> B
A --> C
C --> D
B --> E
D --> F
E --> F
```

#### Left Right

~~~txt
  ```mermaid
  graph LR
    A --> B
    A --> C
    C --> D
    B --> E
    D --> F
    E --> F
  ```
~~~

__Output:__

```mermaid
graph LR
  A --> B
  A --> C
  C --> D
  B --> E
  D --> F
  E --> F
```

#### Right Left

~~~txt
  ```mermaid
  graph RL
    A --> B
    A --> C
    C --> D
    B --> E
    D --> F
    E --> F
  ```
~~~

__Output:__

```mermaid
graph RL
  A --> B
  A --> C
  C --> D
  B --> E
  D --> F
  E --> F
```

### Shapes

```mermaid
graph
  A[Process]
```

```mermaid
graph
  A(Alternate Process)
```

```mermaid
graph
  A((Start))
  B((End))
```

```mermaid
graph
  A([Terminal])
```

```mermaid
graph
  A[[Routine or Predefined Process]]
```

```mermaid
graph
  A{Decision}
```

```mermaid
graph
  A[(Database)]
```

```mermaid
graph
  A>Ribbon]
```

```mermaid
graph
  A{{Preparation}}
```

```mermaid
graph
  A[/Input/]
```

```mermaid
graph
  A[/Manual Operation\]
```

### Arrows and Links

#### Arrow

~~~txt
  ```mermaid
  graph LR
    A-->B
  ```
~~~

__Output:__

```mermaid
graph LR
  A-->B
```

#### Thicker Arrow

~~~txt
  ```mermaid
  graph LR
    A==>B
  ```
~~~

__Output:__

```mermaid
graph LR
  A==>B
```

#### Open link

~~~txt
  ```mermaid
  graph LR
    A --- B
  ```
~~~

__Output:__

```mermaid
graph LR
  A --- B
```

#### Dotted arrow

~~~txt
  ```mermaid
  graph LR
    A -.-> B
  ```
~~~

__Output:__

```mermaid
graph LR
  A -.-> B
```

### Adding labels

To add Labels on a flowchart we simply use brackets `[]`

~~~txt
  ```mermaid
  graph LR
    A[Start] --> B[Input value]
    B --> C[Process values]
    C --> D[Finish]
  ```
~~~

__Output:__

```mermaid
graph LR
  A[Start] --> B[Input value]
  B --> C[Process values]
  C --> D[Finish]
```

### Adding conditions  

To add conditions to the flowchart we use curly braces `{}` and to add response we use pipes `||`

~~~txt
  ```mermaid
  graph TD
    A[Start] --> B[Input value]
    B --> C{Value is over 18?}
    C --> |Yes| D[Retrieve data]
    C --> |No| E[Decline access]
    D --> F[Finish]
    E --> F[Finish]
  ```
~~~

__Output:__

```mermaid
graph TD
  A[Start] --> B[Input value]
  B --> C{Value is over 18?}
  C --> |Yes| D[Retrieve data]
  C --> |No| E[Decline access]
  D --> F[Finish]
  E --> F[Finish]
```

## Sequence diagram

## Gantt diagram

## Class diagram

## Git graph

## Entity Relationship Diagram

## User Journey Diagram

## References

- [Mermaid Documentation](https://mermaid-js.github.io/mermaid/#/)
