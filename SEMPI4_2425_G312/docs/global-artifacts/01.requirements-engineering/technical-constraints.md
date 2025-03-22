# Supplementary Specification (NFR - FURPS+)

## Functionality

- NFR08 - The system must support user authentication and authorization.
- NFR11 - DSL files describing figures must be imported into the system.
- NFR08 - The system must validate show proposals and figure descriptions.
- NFR12 - Simulations must detect drone collisions in real time.
- NFR12 - Simulation reports must be generated and stored.
- NFR12 - Support for testing individual figures and full shows.

## Usability

- NFR02 - Documentation must be written in English.
- NFR02 - Diagrams should be created using PlantUML and exported in PNG format.
- NFR03 - Provide clear error messages and feedback to the user.
- NFR06 - Include a README file with instructions on how to build, deploy and run the system in repository root.

## Reliability

- NFR05 - The system must validate business rules during data entry and updates.
- NFR12 - Simulations must halt and report any detected collisions.
- NFR12 - The system must handle large-scale shows without crashing.
- NFR12 - Past drone positions must be tracked to help prevent future collisions.

## Performance

- NFR12 - The system must support simulation of hundreds of drones.
- NFR12 - Simulations must run step-by-step and allow synchronization between drones.
- NFR12 - Support for distributed simulations across multiple servers using shared memory and signals.

## Supportability

- NFR03 - The project must include unit tests.
- NFR01 - Code must be modular and maintainable.
- NFR06 - Scripts must exist to build and deploy on Linux and Windows.
- NFR07 - Support both in-memory and relational databases for persistence.
- NFR05 - Continuous integration (CI) must be configured using GitHub Actions.

## + Constraints

### Design Constraints

- NFR09 - Main language: Java.
- NFR12 - Simulation system: implemented in C with processes, threads, signals, pipes, shared memory, and semaphores.
- NFR11 - Use of ANTLR for DSL parsing and validation.
- NFR01 - Follow Scrum methodology for project management.
- NFR04 - Use GitHub for version control and project repository.

### Implementation Constraints

- NFR11 - Must support plugin-based architecture for DSL and drone language handling.
- NFR04 - Only one main branch (e.g., `main`) used for deployment.
- NFR07 - Data must be initialized via bootstrap when necessary.

### Interface Constraints

- NFR11 - DSL is created using external tools and imported into the system.
- NFR11 - Drone programming languages and validation logic must be supported via configurable plugins.
- NFR10 - Inter-process communication is required for simulation components.

### Physical Constraints

- NFR12 - Simulations may run on multiple machines and must support parallel execution across drone zones.
