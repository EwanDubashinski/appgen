# appgen

## General workflow

1. Determine the type of application you want to create:
    - Web application
    - Mobile application
    - Desktop application
    - API
    - Library
2. Choose the UI reference (if applicable):
    - Figma
    - Picture
    - DSL
    - Plain text
3. Clarify the high-level requirements:
    - Functional (by DDD and BDD)
    - Non-functional (applicable to each type of application)
4. Generate high-level architecture
5. Generate the project structure:
    - UI references directory
    - Frontend
        - Vite
        - Modules
    - Backend
        - Services
        - Generate project structure by gradle init or maven archetype
    - API
    - Documentation
6. Iterate over the modules and services and repeat the process from the step 3. Iterate until the requirements are clear for start in-detail implementation.
7. Generate contracts for the services and modules
8. Generate API specification
9. Generate contracts for smaller components
10. Generate the dependency trees for the modules and services
11. Generate code, bottom-up:
     - By the leaf-to-root documentation and the component contracts, identify the dependencies and generate mocks for the dependencies
     - Generate unit-tests for the components, using the mocks
     - Generate the implementation of the components
     - Ensure that the implementation is covered by the tests and the tests are green
     - *Optionally* Criticize the implementation and the tests and iterate over the implementation and the tests
12. Generate the integration tests for services and modules
13. Generate the integration tests for the whole application