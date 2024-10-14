# UML Cheatsheet

## 1. **Class Diagram**

- **Class**: Represents a blueprint for objects.
  - **Syntax**:

    ```plaintext
    +---------------------+
    |       ClassName     |
    +---------------------+
    | - attribute1: Type  |
    | - attribute2: Type  |
    +---------------------+
    | + method1(): Return |
    | + method2(): Return |
    +---------------------+
    ```

- **Visibility**:
  - `+` Public
  - `-` Private
  - `#` Protected
  - `~` Package

- **Relationships**:
  - **Association**: A line connecting two classes.
  - **Inheritance**: A line with a hollow triangle pointing to the parent class.
  - **Aggregation**: A line with a hollow diamond pointing to the whole.
  - **Composition**: A line with a filled diamond pointing to the whole.
  - **Dependency**: A dashed line with an arrow pointing to the dependent class.

## 2. **Use Case Diagram**

- **Actors**: Represented by stick figures.
- **Use Cases**: Represented by ovals.
- **System Boundary**: A rectangle that contains use cases.
- **Relationships**:
  - **Association**: A line connecting actors to use cases.
  - **Include**: A dashed arrow pointing to the included use case.
  - **Extend**: A dashed arrow pointing to the extended use case.

## 3. **Sequence Diagram**

- **Lifeline**: Represented by a vertical dashed line.
- **Activation**: Represented by a thin rectangle on a lifeline.
- **Messages**: Represented by arrows between lifelines.
  - **Synchronous**: Solid arrowhead.
  - **Asynchronous**: Open arrowhead.
  - **Return**: Dashed arrow.

## 4. **Activity Diagram**

- **Start Node**: Filled circle.
- **End Node**: Filled circle with a border.
- **Activity**: Rounded rectangle.
- **Decision**: Diamond.
- **Merge**: Diamond.
- **Fork/Join**: Thick horizontal or vertical bar.
- **Flow**: Arrow connecting activities.

## 5. **State Diagram**

- **State**: Rounded rectangle.
- **Transition**: Arrow connecting states.
- **Initial State**: Filled circle.
- **Final State**: Filled circle with a border.

## 6. **Component Diagram**

- **Component**: Rectangle with two smaller rectangles on the side.
- **Interface**: Circle or lollipop notation.
- **Dependency**: Dashed arrow.

## 7. **Deployment Diagram**

- **Node**: 3D box.
- **Artifact**: Rectangle.
- **Communication Path**: Line connecting nodes.
