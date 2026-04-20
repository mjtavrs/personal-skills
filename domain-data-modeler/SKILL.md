---
name: domain-data-modeler
description: Use this skill when modeling entities, tables, relationships, statuses, domain rules, constraints, and data lifecycles in backend or database changes.
---

# Domain Data Modeler

## Goal
Design and review data models that are clear, consistent, scalable, and safe to evolve.

## When to use
Use this skill for:
- new entities
- new tables
- schema changes
- relationship design
- status fields
- workflow state modeling
- domain rules that affect stored data

## Core principles
- model the domain, not just the screen
- prefer clarity over shortcuts
- keep naming consistent across code and database
- protect data integrity from the start
- think about future evolution before freezing the schema

## Always verify
- entity purpose is clear
- names are in English and descriptive
- relationships and cardinality are correct
- required vs optional fields are intentional
- uniqueness and constraints are defined where needed
- status fields have valid, limited states
- audit fields are present when useful
- soft delete is used only when it makes sense
- indexes match likely access patterns
- duplicated or redundant data is avoided

## Questions to answer
- What is the source of truth?
- What fields are mandatory?
- What can change over time?
- What should never be nullable?
- What should be unique?
- What data must be historically traceable?
- What would break if this model grows 10x?

## Anti-patterns to avoid
- generic names like data, info, type, value
- storing unrelated concerns in one table/entity
- status fields with vague meanings
- duplication without justification
- optional fields that are actually required by the business
- schema shaped only for one screen or one temporary flow

## Output format
Always provide:
1. Model summary
2. Main entities and relationships
3. Integrity and constraint recommendations
4. Evolution risks
5. Plain-language summary for non-technical readers