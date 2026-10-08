# Diagrams

This directory is intended to contain the editable source files and exported versions of the technical diagrams used by GemeloIA and its project report.

## Current diagram set

The project report currently defines:

1. **Conceptual Entity-Relationship diagram**
   - Chen-style entities, attributes, named relationships and cardinalities
2. **Domain class diagram**
   - Java-oriented domain classes and relationships
3. **Layered architecture diagram**
   - Telegram presentation, application services, AI integration, JPA/Hibernate and PostgreSQL
4. **Use-case diagram**
   - user actions, Telegram participation and OpenAI API interaction
5. **Sequence diagram**
   - generation and persistence flow for a personalized recommendation
6. **Wireframes and Telegram mockups**
   - main conversational interaction flow

## Recommended files

When the editable diagrams are added, use clear names such as:

- `er-conceptual.drawio`
- `domain-classes.drawio`
- `layered-architecture.drawio`
- `use-cases.drawio`
- `recommendation-sequence.drawio`

Exports used in the report can be stored alongside them as PNG, SVG or PDF.

## Rule

The diagrams should reflect the implemented system rather than exist only as academic documentation. If the code architecture changes, the relevant diagram and the project report should be updated together.
