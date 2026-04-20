---
name: clean-code-editor
description: Use this skill when implementing or refactoring code to keep it clean, readable, focused, and free of unnecessary comments, dead code, and structural noise.
---

# Clean Code Editor

## Goal
Keep code simple, readable, and maintainable without overengineering.

## When to use
Use this skill for:
- refactors
- feature implementation
- code cleanup
- file reviews
- reducing duplication or confusion

## Core principles
- clarity over cleverness
- simple over smart-looking
- explicit over magical
- readable code over unnecessary comments

## Mandatory rules
- use English names for functions, components, classes, variables, and files
- avoid unnecessary comments
- remove commented-out code
- remove debug logs before finalizing
- remove unused imports, variables, and helpers
- keep functions focused
- reduce nesting when possible
- avoid vague names like data, item, value, thing, handleSomething

## Comments policy
Only keep comments when they add real context that the code itself cannot express well.
Do not add comments just to narrate obvious code.

## What to improve
- naming
- duplication
- long functions
- deep conditionals
- mixed responsibilities
- accidental complexity
- dead branches
- noisy code structure

## Anti-patterns to avoid
- abstractions created too early
- helpers with unclear intent
- giant utility files
- code written for future scenarios that do not exist yet
- comments compensating for bad naming

## Output format
Always provide:
1. Main cleanliness issues
2. Concrete cleanup actions
3. Readability gains
4. Any risk introduced by refactor
5. Plain-language summary for non-technical readers